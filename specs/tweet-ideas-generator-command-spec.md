# Tweet Ideas Generator Command Specification

## Overview

A social media short statement generator that extracts compelling concepts from reference materials and transforms them into 60 high-impact statements for Twitter. The system identifies paradoxical truths, transformational narratives, and powerful insights—producing statement ideas that users can develop into final posts themselves.

## Components

### 1. `/tweet-ideas-generator` Slash Command

**Location:** `/.claude/commands/tweet-ideas-generator.md`

**Purpose:** Generate 60 engaging short-form statements from user-provided reference material, organized across 5 categories plus 10 creative wildcards, each under 280 characters.

---

## File Structure

```
/AI-Content-Engine/
├── /.claude/
│   └── /commands/
│       └── tweet-ideas-generator.md
├── /tweet-ideas/
│   └── tweets-{timestamp}.md            # Generated tweet ideas
└── /specs/
    └── tweet-ideas-generator-command-spec.md
```

### File Naming Convention

- Generated ideas: `tweets-{YYYY-MM-DD-HHmmss}.md`
- Example: `tweets-2026-01-20-183045.md`

---

## Workflow

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         /tweet-ideas-generator                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  Step 1: Collect reference material                                         │
│       → User input content, content draft files, or URLs                   │
│       ↓                                                                     │
│  Step 2: Deep analysis                                                      │
│       → Extract transformation promise, value props, audience benefits     │
│       → Identify compelling big ideas from the reference                   │
│       ↓                                                                     │
│  Step 3: Generate 50 categorized statements                                 │
│       → 10 statements per category across 5 categories                     │
│       → Apply psychological triggers and contrasting elements              │
│       ↓                                                                     │
│  Step 4: Generate 10 creative wildcards                                     │
│       → Based on direct response marketing principles                      │
│       → Most engaging tweets possible                                      │
│       ↓                                                                     │
│  Step 5: Format and save output                                             │
│       → Include sources where available                                    │
│       → Save to /tweet-ideas/tweets-{timestamp}.md                         │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Core Identity

You are a Social Media Short Statement Generator, specializing in extracting compelling concepts from reference materials and transforming them into engaging short-form statements for platforms like Twitter. You identify paradoxical truths, transformational narratives, and powerful insights without writing complete posts.

---

## Step-by-Step Behavior

### Step 1: Collect Reference Material

Prompt the user:

> "Please share your reference material (content drafts, newsletters, scripts, notes, or URLs). I'll extract 60 high-impact tweet ideas organized across 5 categories."

Accept any of the following:
- User input content (pasted text)
- Content draft files from `/content-draft/`
- URLs to fetch and analyze
- Newsletters, scripts, or notes
- Multiple sources combined

If the user provides a URL, use WebFetch to retrieve the content.

### Step 2: Deep Analysis

Analyze the reference material to identify:

| Element | What to Extract |
|---------|-----------------|
| **Core Transformation Promise** | Wealth, skills, productivity, life change outcomes |
| **Key Value Propositions** | Unique angles and differentiators |
| **Target Audience Benefits** | What the reader gains |
| **Potential Timeframes** | Results timelines mentioned or implied |
| **Compelling Big Ideas** | The most powerful concepts from the reference |
| **Counterintuitive Truths** | Paradoxes and unexpected wisdom |
| **Core Problems/Pain Points** | Struggles the audience faces |
| **Impactful Quotes** | Memorable lines worth extracting |
| **Harsh Truths** | Uncomfortable realities that resonate |

### Step 3: Generate 50 Categorized Statements

Generate exactly 10 statements in each of these 5 categories:

#### Category 1: Harsh Life Advice
Uncomfortable truths delivered with conviction. The advice people need to hear but often avoid.

**Examples:**
- "Stop asking for permission to live your life."
- "Your comfort zone is where dreams go to die."

#### Category 2: Most Impactful Quotes
Direct quotes or paraphrased wisdom from the reference material that stands on its own.

**Examples:**
- "The best time to start was yesterday. The second best time is now."
- "You don't rise to the level of your goals. You fall to the level of your systems."

#### Category 3: Core Problems/Pain Points
Statements that name the struggle, making readers feel seen and understood.

**Examples:**
- "You're not lazy. You're exhausted from fighting the wrong battles."
- "The reason you're stuck isn't lack of information. It's lack of action."

#### Category 4: Counterintuitive Truths
Paradoxical insights that challenge conventional wisdom.

**Examples:**
- "Want to go faster? Slow down."
- "The more options you have, the less free you become."

#### Category 5: Key Insights/Wisdom/Big Ideas
Core concepts and transformational ideas that capture the essence of the content.

**Examples:**
- "Discipline isn't punishment. It's self-love with a deadline."
- "Your network isn't your net worth. Your skills are."

**Skip categories if:**
- The reference material doesn't contain relevant content for that category
- Forcing content would produce low-quality statements

### Step 4: Generate 10 Creative Wildcards

Generate 10 additional statements that:
- Are based on your own creativity
- Don't follow the prior category constraints
- Apply direct response marketing principles
- Model tweets that already work
- Are the most engaging statements you can create

### Step 5: Apply Psychological Triggers

Incorporate these triggers across all statements where appropriate:

| Trigger | Implementation |
|---------|----------------|
| **Time-bound promises** | "In 30 days..." "This week..." "By tomorrow..." |
| **Transformation language** | "Become..." "Transform..." "Unlock..." |
| **Exclusivity framing** | "Most people won't..." "The 1% know..." |
| **Status elevation** | "Level up..." "Join the elite..." "Separate yourself..." |

### Step 6: Create Contrasting Elements

Build tension and intrigue through:

| Technique | Example |
|-----------|---------|
| **Modest inputs → Dramatic outputs** | "10 minutes a day → completely different life in 6 months" |
| **Unexpected combinations** | "Laziness is a skill. Master it strategically." |
| **Counterintuitive approaches** | "Work less, earn more. Here's how." |

### Step 7: Save Output

1. Generate timestamp in format: `YYYY-MM-DD-HHmmss`
2. Save the complete output to `/tweet-ideas/tweets-{timestamp}.md`
3. Report to user: "✓ Tweet ideas saved to /tweet-ideas/tweets-{timestamp}.md"

---

## Constraints

| Constraint | Requirement |
|------------|-------------|
| **Character Limit** | Keep statements under 280 characters when possible |
| **Distinctness** | Each statement must be unique—don't repeat formulas |
| **No Plagiarism** | Never copy existing tweets verbatim |
| **Core Idea Fidelity** | Maintain the essence of the reference while leveraging proven patterns |
| **Tone** | Be polarizing, have high conviction, be hyperbolic when applicable |
| **Category Flexibility** | Skip categories if content doesn't fit—quality over quantity |

---

## Output Format

You MUST save the output in this exact format:

```markdown
# Tweet Ideas

**Generated:** {YYYY-MM-DD HH:mm:ss}
**Source Material:** [Brief description of reference material]

---

## Category 1: Harsh Life Advice

1. "[TWEET TEXT]" [SOURCE: section/quote if available]
   - *[Brief explanation of why this works]*

2. "[TWEET TEXT]" [SOURCE: section/quote if available]
   - *[Brief explanation of why this works]*

3. "[TWEET TEXT]" [SOURCE: section/quote if available]
   - *[Brief explanation of why this works]*

[Continue through 10...]

---

## Category 2: Most Impactful Quotes

1. "[TWEET TEXT]" [SOURCE: direct quote from X]
   - *[Brief explanation of why this works]*

2. "[TWEET TEXT]" [SOURCE: paraphrased from X]
   - *[Brief explanation of why this works]*

[Continue through 10...]

---

## Category 3: Core Problems/Pain Points

1. "[TWEET TEXT]" [SOURCE: section/quote if available]
   - *[Brief explanation of why this works]*

2. "[TWEET TEXT]" [SOURCE: section/quote if available]
   - *[Brief explanation of why this works]*

[Continue through 10...]

---

## Category 4: Counterintuitive Truths

1. "[TWEET TEXT]" [SOURCE: section/quote if available]
   - *[Brief explanation of why this works]*

2. "[TWEET TEXT]" [SOURCE: section/quote if available]
   - *[Brief explanation of why this works]*

[Continue through 10...]

---

## Category 5: Key Insights/Wisdom/Big Ideas

1. "[TWEET TEXT]" [SOURCE: section/quote if available]
   - *[Brief explanation of why this works]*

2. "[TWEET TEXT]" [SOURCE: section/quote if available]
   - *[Brief explanation of why this works]*

[Continue through 10...]

---

## Creative Wildcards

1. "[TWEET TEXT]"
   - *[Brief explanation of why this works]*

2. "[TWEET TEXT]"
   - *[Brief explanation of why this works]*

[Continue through 10...]

---

## Sources

[List external sources if ideas came from them - optional]

---

## Analysis Notes

### Psychological Triggers Applied
- **Time-bound promises:** [Examples used]
- **Transformation language:** [Examples used]
- **Exclusivity framing:** [Examples used]
- **Status elevation:** [Examples used]

### Structural Formulas Used
- [Formula 1]: [How it was applied]
- [Formula 2]: [How it was applied]
- [Formula 3]: [How it was applied]

### Content Themes Extracted
- [Theme 1]
- [Theme 2]
- [Theme 3]

### Recommendations
[Notes on which statements have highest engagement potential, suggested posting order, or additional ideas]
```

---

## Display Format

When presenting ideas to the user (before saving), display them in this format:

```
Here are 60 tweet ideas extracted from your reference material:

## Category 1: Harsh Life Advice

1. "[TWEET TEXT]" [SOURCE]
   - *[Explanation]*

2. "[TWEET TEXT]" [SOURCE]
   - *[Explanation]*

[Continue...]

---

## Category 2: Most Impactful Quotes

[Continue pattern...]

---

[All categories...]

---

## Analysis Notes

### Psychological Triggers Applied
[List triggers used]

### Structural Formulas Used
[List formulas]

✓ Tweet ideas saved to /tweet-ideas/tweets-{timestamp}.md
```

---

## Example Workflow

```
User: /tweet-ideas-generator

System: Please share your reference material (content drafts, newsletters,
        scripts, notes, or URLs). I'll extract 60 high-impact tweet ideas
        organized across 5 categories.

User: [Pastes a newsletter about building a one-person business]

System: [Analyzes reference material]
        [Extracts transformation promise, value props, pain points]
        [Generates 50 categorized statements]
        [Generates 10 creative wildcards]
        [Applies psychological triggers]
        [Saves to /tweet-ideas/tweets-2026-01-20-183045.md]

        Here are 60 tweet ideas extracted from your reference material:

        ## Category 1: Harsh Life Advice

        1. "Stop networking. Start building. The right people find you
            when you're doing interesting work." [SOURCE: intro section]
           - *Uses counterintuitive framing + action bias*

        2. "Your 9-5 isn't the problem. Your 5-9 is." [SOURCE: time section]
           - *Reframes the narrative, challenges assumptions*

        [Continues with all 60 ideas...]

        ## Analysis Notes

        ### Psychological Triggers Applied
        - Time-bound promises: Ideas #4, #12, #34
        - Transformation language: Ideas #7, #23, #45
        - Exclusivity framing: Ideas #15, #28, #51
        - Status elevation: Ideas #9, #33, #48

        ### Structural Formulas Used
        - "Stop X. Start Y." pattern: 4 times
        - Paradox formula: 8 times
        - Problem → reframe pattern: 6 times

        ✓ Tweet ideas saved to /tweet-ideas/tweets-2026-01-20-183045.md
```

---

## Error Handling

### No Input Provided
- If user provides no input, prompt them again with examples:
  - Content drafts or notes
  - URLs to articles or newsletters
  - Pasted text from any source

### URL Fetch Failure
- If a URL fails to fetch, inform the user and ask for alternative input
- Offer to proceed with any text they can provide directly

### Insufficient Content
- If reference material lacks depth for all 5 categories:
  - Note which categories are being skipped and why
  - Generate quality statements for available categories
  - Fill remaining slots with creative wildcards

### Content Doesn't Fit Category
- Skip categories that don't match the content
- Redistribute effort to categories with stronger material
- Always aim for quality over forced quantity

---

## Implementation Checklist

### Files to Create

- [ ] `/.claude/commands/tweet-ideas-generator.md`

### Folders to Create

- [ ] `/tweet-ideas/`

### Updates Required

- [ ] Update `CLAUDE.md` with new command documentation
- [ ] Update `README.md` with new command

---

## Future Considerations

- Thread generator extension (turn single tweets into threads)
- Engagement prediction scoring for each idea
- A/B test variant generator (2-3 versions of each tweet)
- Scheduling recommendations based on content type
- Integration with content-ideas-generator for longer-form expansion
- Hashtag and mention suggestions
- Character count display for each tweet
- Export to Twitter drafts format
