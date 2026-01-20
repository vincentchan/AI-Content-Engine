# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

AI-Content-Engine - A system for analyzing high-performing content to study structure, psychological patterns, and ideas. The engine deconstructs content from URLs and compiles insights into a continuously refined swipe file document.

## Commands

### /swipe-file-generator

Analyzes high-performing content from URLs and builds a swipe file.

**Usage:** Run `/swipe-file-generator` to:
1. Check `/swipe-file/swipe-file-sources.md` for URLs to process
2. Identify new URLs that haven't been digested yet
3. Fetch and analyze each URL using the content-deconstructor subagent
4. Append analyses to `/swipe-file/swipe-file.md`

**Location:** `/.claude/commands/swipe-file-generator.md`

### /content-draft-generator

Generates new content drafts based on reference content analysis.

**Usage:** Run `/content-draft-generator` to:
1. Provide up to 5 reference content URLs
2. Analyze and deconstruct reference content
3. Generate a comprehensive content anatomy guide
4. Create context questions for content creation
5. Generate and execute a meta prompt for draft creation
6. Produce 3 variations of your new content

**Location:** `/.claude/commands/content-draft-generator.md`

**Output Folders:**
- `/content-breakdown/` - Deconstructed reference content
- `/content-anatomy/` - Synthesized content guides
- `/content-context/` - Context requirements
- `/content-meta-prompt/` - Generated meta prompts
- `/content-draft/` - Final content draft variations

### /youtube-title-generator

Generates compelling YouTube title ideas from content concepts.

**Usage:** Run `/youtube-title-generator` to:
1. Provide a content idea, newsletter concept, or reference material
2. Analyze input for transformation promise, value props, and audience benefits
3. Generate 20 structured titles using proven formulas and psychological triggers
4. Generate 10 creative titles based on direct response marketing principles
5. Save all 30 titles with analysis to timestamped file

**Location:** `/.claude/commands/youtube-title-generator.md`

**Output Folder:** `/youtube-title/`

**Key Files:**
- `/youtube-title/reference-titles.md` - Editable reference examples (add your own)
- `/youtube-title/titles-{timestamp}.md` - Generated title outputs

### /content-ideas-generator

Generates structured post outlines from reference materials for wisdom-style social posts.

**Usage:** Run `/content-ideas-generator` to:
1. Provide reference material (newsletters, scripts, notes, journal entries)
2. Extract 5 distinct post concepts with paradoxes and transformation arcs
3. Generate structured outlines with examples, objections, and actionable steps
4. Save outlines to timestamped file

**Location:** `/.claude/commands/content-ideas-generator.md`

**Output Folder:** `/content-ideas/`

**Key Files:**
- `/content-ideas/ideas-{timestamp}.md` - Generated post outlines

### /creative-thought-partner

A conversational creative thought partner that reveals hidden brilliance in your ideas through critical observations and paradox hunting.

**Usage:** Run `/creative-thought-partner` to:
1. Share a topic or idea you want to explore
2. Engage in guided conversation using four breakthrough drivers
3. Discover paradoxes, patterns, and unnamed concepts in your thinking
4. Crystallize and name your unique frameworks
5. Export full session with narrative arc and transcript

**Location:** `/.claude/commands/creative-thought-partner.md`

**Output Folder:** `/creative-thoughts/`

**Key Files:**
- `/creative-thoughts/session-{timestamp}.md` - Session transcripts with breakthroughs

### /tweet-ideas-generator

Generates 60 high-impact tweet ideas from reference content across 5 categories.

**Usage:** Run `/tweet-ideas-generator` to:
1. Provide reference material (content drafts, newsletters, URLs, notes)
2. Extract key takeaways and compelling concepts
3. Generate 50 categorized statements across 5 categories (harsh advice, quotes, pain points, counterintuitive truths, key insights)
4. Generate 10 creative wildcard tweets
5. Save all 60 ideas with sources and explanations

**Location:** `/.claude/commands/tweet-ideas-generator.md`

**Output Folder:** `/tweet-ideas/`

**Key Files:**
- `/tweet-ideas/tweets-{timestamp}.md` - Generated tweet ideas

## Subagents

### content-deconstructor

Analyzes individual pieces of content to extract recreatable patterns and insights.

**Location:** `/.claude/subagents/content-deconstructor.md`

**Analyzes:**
- Structural breakdown (hooks, flow, organization, CTA)
- Psychological patterns (persuasion, emotions, biases)
- Writing mechanics (headlines, formatting, storytelling)
- Content strategy (audience, positioning, objections)
- Recreatable templates and frameworks

### content-anatomy-generator

Synthesizes multiple content breakdowns into a comprehensive guide.

**Location:** `/.claude/subagents/content-anatomy-generator.md`

**Generates:**
- Core structure blueprint
- Psychological playbook
- Hook library
- Pacing & flow guide
- Fill-in-the-blank templates

### content-context-generator

Analyzes content guides to determine required user context.

**Location:** `/.claude/subagents/content-context-generator.md`

**Generates:**
- Essential context questions (topic, audience, goals, voice)
- Optional context suggestions
- Context gathering guidance

### meta-prompt-generator

Creates well-structured, verifiable prompts for content creation.

**Location:** `/.claude/subagents/meta-prompt-generator.md`

**Features:**
- Task decomposition
- Expert persona coordination
- Hallucination minimization
- Iterative verification

## Architecture

```
/AI-Content-Engine/
├── /.claude/
│   ├── /commands/
│   │   ├── swipe-file-generator.md
│   │   ├── content-draft-generator.md
│   │   ├── youtube-title-generator.md
│   │   ├── content-ideas-generator.md
│   │   ├── creative-thought-partner.md
│   │   └── tweet-ideas-generator.md
│   └── /subagents/
│       ├── content-deconstructor.md
│       ├── content-anatomy-generator.md
│       ├── content-context-generator.md
│       └── meta-prompt-generator.md
├── /swipe-file/
│   ├── swipe-file.md
│   ├── swipe-file-sources.md
│   └── .digested-urls.json
├── /content-breakdown/                  # Reference content analysis
├── /content-anatomy/                    # Synthesized content guides
├── /content-context/                    # Context requirements
├── /content-meta-prompt/                # Generated meta prompts
├── /content-draft/                      # Final content draft variations
├── /content-ideas/                      # Post outline generation
│   └── ideas-{timestamp}.md
├── /youtube-title/                      # YouTube title generation
│   ├── reference-titles.md
│   └── titles-{timestamp}.md
├── /creative-thoughts/                  # Creative thought partner sessions
│   └── session-{timestamp}.md
├── /tweet-ideas/                        # Tweet ideas generation
│   └── tweets-{timestamp}.md
├── /specs/
│   ├── swipe-file-generator-command-spec.md
│   ├── content-draft-generator-command-spec.md
│   ├── youtube-title-generator-command-spec.md
│   ├── content-ideas-generator-command-spec.md
│   ├── creative-thought-partner-command-spec.md
│   └── tweet-ideas-generator-command-spec.md
└── /todos/
    ├── swipe-file-generator-implementation.md
    ├── content-draft-generator-implementation.md
    ├── youtube-title-generator-implementation.md
    ├── content-ideas-generator-implementation.md
    ├── creative-thought-partner-implementation.md
    └── tweet-ideas-generator-implementation.md
```

## Key Files

| File | Purpose |
|------|---------|
| `/swipe-file/swipe-file-sources.md` | Add URLs here for analysis |
| `/swipe-file/swipe-file.md` | Master swipe file with all analyses |
| `/swipe-file/.digested-urls.json` | Tracks which URLs have been processed |
