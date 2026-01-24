# Swipe File Generator Command Specification

## Overview

A system for analyzing high-performing content to study structure, psychological patterns, and ideas. The system deconstructs content from URLs and compiles insights into a single, continuously refined swipe file document.

## Components

### 1. `/swipe-file-generator` Skill

**Location:** `/.claude/skills/swipe-file-generator/SKILL.md`

**Purpose:** Orchestrate the ingestion and analysis of content URLs, track processing state, and maintain the swipe file document.

#### Behavior

1. **URL Source Detection**
   - Check for URLs in designated source files (e.g., `/swipe-file/swipe-file-sources.md` or similar)
   - If no URLs found in files, prompt user to provide URLs directly
   - Accept URLs from user input at any time

2. **URL Tracking**
   - Maintain a registry of previously digested URLs (e.g., `/swipe-file/.digested-urls.json`)
   - On each run, compare source URLs against digested registry
   - Only process URLs that haven't been analyzed yet
   - Update registry after successful processing

3. **Content Processing Pipeline (Batch)**
   - Fetch all new URLs in parallel
   - Track fetch successes and failures separately
   - Combine all successfully fetched content into a single payload
   - Launch ONE `content-deconstructor` subagent call with all content
   - Receive combined analysis for all content pieces
   - Update registry with all processed URLs at once
   - Append all new insights into the master swipe file

4. **Swipe File Management**
   - Output location: `/swipe-file/swipe-file.md`
   - If swipe file exists, merge new content intelligently (don't overwrite)
   - Organize content by categories, patterns, or content types
   - Include source URL references for each analyzed piece

#### Input Sources

| Source Type | Location | Format |
|-------------|----------|--------|
| URL list file | `/swipe-file/swipe-file-sources.md` | One URL per line |
| User input | Interactive prompt | URLs provided directly |
| Digested registry | `/swipe-file/.digested-urls.json` | JSON array with URL and metadata |

#### Digested URLs Registry Format

```json
{
  "digested": [
    {
      "url": "https://example.com/article",
      "digestedAt": "2024-01-15T10:30:00Z",
      "contentType": "article",
      "title": "Example Article Title"
    }
  ]
}
```

---

### 2. `content-deconstructor` Subagent

**Location:** `/.claude/skills/swipe-file-generator/subagents/content-deconstructor.md`

**Purpose:** Deep analysis of content pieces to extract recreatable patterns and insights.

#### Capabilities

- **Batch Processing:** Analyze multiple content pieces in a single request, returning separate analysis for each
- Analyze content from various sources:
  - Articles and blog posts
  - Tweets and social media threads
  - Video transcripts/descriptions
  - Landing pages and sales copy

#### Analysis Framework

For each piece of content, the subagent should identify and document:

1. **Structural Breakdown**
   - Opening hook technique
   - Content flow and transitions
   - Section organization
   - Closing/CTA structure
   - Length and pacing patterns

2. **Psychological Patterns**
   - Persuasion techniques used (scarcity, social proof, authority, etc.)
   - Emotional triggers and appeals
   - Cognitive biases leveraged
   - Trust-building elements
   - Engagement hooks and retention techniques

3. **Writing Mechanics**
   - Headline/title formula
   - Sentence structure patterns
   - Vocabulary and tone choices
   - Formatting techniques (lists, bold, whitespace)
   - Storytelling elements

4. **Content Strategy**
   - Target audience signals
   - Value proposition delivery
   - Objection handling
   - Unique angle or positioning

5. **Recreatable Template**
   - Step-by-step structure outline
   - Fill-in-the-blank framework
   - Key elements checklist

#### Output Format

The subagent should return a structured analysis that can be merged into the master swipe file:

```markdown
## [Content Title]
**Source:** [URL]
**Type:** [article/tweet/video/etc.]
**Analyzed:** [date]

### Why It Works
[Summary of effectiveness]

### Structure Breakdown
[Detailed structural analysis]

### Psychological Patterns
[Identified patterns and techniques]

### Recreatable Framework
[Template/checklist for recreation]

### Key Takeaways
[Bullet points of main lessons]
```

---

### 3. Folder Structure

```
/AI-Content-Engine/
├── /.claude/
│   └── /skills/
│       └── swipe-file-generator/
│           ├── SKILL.md                   # Skill instructions
│           └── subagents/
│               └── content-deconstructor.md   # Subagent instructions
└── /swipe-file/
    ├── swipe-file.md                  # Master swipe file document
    ├── swipe-file-sources.md          # Source URLs to process
    └── .digested-urls.json            # Registry of processed URLs
```

---

## Workflow

### First Run

```
1. User invokes /swipe-file-generator
2. Command checks /swipe-file/swipe-file-sources.md for URLs
3. If no URLs found, prompts user for URLs
4. Creates .digested-urls.json (empty registry)
5. Fetches ALL URLs in parallel, tracking successes and failures
6. Combines all successfully fetched content into single payload
7. Launches ONE content-deconstructor subagent with all content
8. Receives combined analysis for all content pieces
9. Updates digested registry with all processed URLs
10. Creates /swipe-file/swipe-file.md with all analyses
11. Reports summary to user (processed count, failures if any)
```

### Subsequent Runs

```
1. User invokes /swipe-file-generator
2. Command reads swipe-file-sources.md and .digested-urls.json
3. Identifies new URLs (in swipe-file-sources.md but not in registry)
4. If no new URLs, checks if user wants to add URLs manually
5. Fetches ALL new URLs in parallel, tracking successes and failures
6. Combines all successfully fetched content into single payload
7. Launches ONE content-deconstructor subagent with all content
8. Receives combined analysis for all content pieces
9. Updates digested registry with all processed URLs
10. Appends all new analyses to existing swipe-file.md
11. Reports summary of new additions to user (processed count, failures if any)
```

---

## Swipe File Document Structure

The master swipe file (`/swipe-file/swipe-file.md`) should be organized for easy reference:

```markdown
# Swipe File

> A collection of deconstructed high-performing content for study and recreation.

## Table of Contents

| # | Title | Type | Date |
|---|-------|------|------|
| 1 | [Content Title 1](#content-title-1) | article | 2026-01-19 |
| 2 | [Content Title 2](#content-title-2) | tweet | 2026-01-18 |

---

## Content Title 1
[Full analysis from content-deconstructor]

---

## Content Title 2
[Full analysis from content-deconstructor]
```

### Table of Contents Auto-Generation

The ToC is automatically generated/updated whenever the swipe file is modified:

1. **Source:** Read titles from `.digested-urls.json` registry
2. **Format:** Markdown table with columns: #, Title (linked), Type, Date
3. **Order:** Most recent first (matches content order in file)
4. **Links:** Title links to anchor (e.g., `[My Title](#my-title)`)

**Anchor Generation Rules:**
- Lowercase all characters
- Replace spaces with hyphens
- Remove special characters ($, ", ', (), etc.)
- Example: `"How to make $10M"` → `#how-to-make-10m`

---

## Technical Requirements

1. **URL Validation**
   - Validate URLs before attempting to fetch
   - Handle various URL formats (with/without protocol, trailing slashes)
   - Skip invalid or unreachable URLs with error logging

2. **Content Fetching**
   - Support for standard web pages (HTML)
   - Handle paywalled or inaccessible content gracefully
   - Extract main content (strip navigation, ads, etc.)

3. **Twitter/X URL Handling**

   Twitter/X URLs require JavaScript to render and cannot be fetched directly. Use the **FxTwitter API** instead.

   **Detection:** URL contains `twitter.com` or `x.com`

   **API Transformation:**
   ```
   Original: https://x.com/{username}/status/{id}
   API URL:  https://api.fxtwitter.com/{username}/status/{id}

   Original: https://twitter.com/{username}/status/{id}
   API URL:  https://api.fxtwitter.com/{username}/status/{id}
   ```

   **API Features:**
   - No authentication required
   - Returns JSON with full tweet data
   - Includes: text, author info, engagement metrics, media, quoted tweets
   - No strict rate limits for reasonable use

   **Response Fields:**
   | Field | Description |
   |-------|-------------|
   | `tweet.text` | Full tweet text |
   | `tweet.author.name` | Display name |
   | `tweet.author.screen_name` | @handle |
   | `tweet.likes` | Like count |
   | `tweet.retweets` | Retweet count |
   | `tweet.replies` | Reply count |
   | `tweet.media` | Attached media array |
   | `tweet.quote` | Quoted tweet object |

4. **State Persistence**
   - Digested URLs registry must persist between sessions
   - Handle concurrent modifications safely
   - Backup mechanism for swipe file

5. **Error Handling**
   - Continue processing remaining URLs if one fails
   - Report failures to user with actionable information
   - Don't mark failed URLs as digested

---

## Future Considerations

- Support for bulk URL import from bookmarks/exports
- Content categorization and tagging system
- Search functionality within swipe file
- Export to different formats (PDF, Notion, etc.)
- Scheduled automatic checking for new URLs
- Integration with read-later services (Pocket, Instapaper)
