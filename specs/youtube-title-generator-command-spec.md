# YouTube Title Generator Command Specification

## Overview

A YouTube title generation system that transforms content ideas, newsletter concepts, or reference materials into compelling, click-worthy YouTube title ideas using proven structural formulas and psychological patterns from high-performing videos.

## Components

### 1. `/youtube-title-generator` Slash Command

**Location:** `/.claude/commands/youtube-title-generator.md`

**Purpose:** Generate 30 distinct, compelling YouTube title ideas (20 structured + 10 creative) based on user-provided content ideas or reference material.

---

## File Structure

```
/AI-Content-Engine/
├── /.claude/
│   └── /commands/
│       └── youtube-title-generator.md
├── /youtube-title/
│   ├── reference-titles.md              # Editable reference examples
│   └── titles-{timestamp}.md            # Generated title outputs
└── /specs/
    └── youtube-title-generator-command-spec.md
```

### File Naming Convention

- Generated titles: `titles-{YYYY-MM-DD-HHmmss}.md`
- Example: `titles-2026-01-20-143052.md`

---

## Workflow

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         /youtube-title-generator                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  Step 1: Collect user input                                                 │
│       → Content idea, newsletter concept, or reference material             │
│       ↓                                                                     │
│  Step 2: Analyze input                                                      │
│       → Identify core transformation, value props, audience benefits        │
│       ↓                                                                     │
│  Step 3: Load reference titles                                              │
│       → Read /youtube-title/reference-titles.md for patterns                │
│       ↓                                                                     │
│  Step 4: Generate 20 structured titles                                      │
│       → Apply structural formulas and psychological triggers                │
│       ↓                                                                     │
│  Step 5: Generate 10 creative titles                                        │
│       → Based on direct response marketing principles                       │
│       ↓                                                                     │
│  Step 6: Save output                                                        │
│       → Save to /youtube-title/titles-{timestamp}.md                        │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Step-by-Step Behavior

### Step 1: Collect User Input

Prompt the user:
> "Please share your content idea, newsletter concept, or reference material. I'll transform it into 30 compelling YouTube title ideas."

Accept any of the following:
- A basic content idea or topic
- A newsletter or article to extract ideas from
- A URL to fetch and analyze
- Multiple concepts or themes

### Step 2: Analyze Input

Analyze the user's content to identify:

| Element | Description |
|---------|-------------|
| **Core Transformation Promise** | Wealth, skills, productivity, life change, etc. |
| **Key Value Propositions** | Unique angles and differentiators |
| **Target Audience Benefits** | What the viewer gains |
| **Potential Timeframes** | Realistic timeframes for results |
| **Compelling Big Ideas** | The most powerful concepts from the reference |

### Step 3: Load Reference Titles

Read the reference titles from `/youtube-title/reference-titles.md` to:
- Understand proven patterns and structures
- Extract psychological triggers that work
- Ensure generated titles align with successful examples

### Step 4: Generate 20 Structured Titles

Apply the following framework:

#### Structural Formulas

| Formula | Pattern | Example |
|---------|---------|---------|
| **Bold Statement** | [Bold Claim] + ([Supporting Detail/Method]) | The One-Person Business Model (How To Productize Yourself) |
| **How To** | [How To] + [Desirable Outcome] + ([Mechanism/Approach]) | How To Get Ahead Of 99% Of People In 6-12 Months |
| **Time-Bound** | [Time Element] + ([What To Focus On]) | Change Your Life In 365 Hours (The New Rich Focus On These Tasks) |

#### Psychological Triggers

| Trigger | Implementation | Example |
|---------|----------------|---------|
| **Time-Bound Promises** | Specify timeframes like "6-12 months," "365 hours," "2-4 hours" | "In 6-12 Months," "Working 2-4 Hours A Day" |
| **Transformation Language** | Use phrases that promise personal change | "won't be the same person," "change your life," "reinvent your life" |
| **Exclusivity Framing** | Create insider knowledge appeal | "what they don't tell you," "most people ignore," "the secret" |
| **Status Elevation** | Appeal to ambition and achievement | "get ahead of 99%," "high-income skill," "millionaire," "irreplaceable" |

#### Contrasting Elements

Create titles that:
- **Pair modest inputs with dramatic outputs** (e.g., "2-4 Hours A Day" → "$1 Million")
- **Create intrigue through unexpected combinations** (e.g., "Life Into A Video Game")
- **Highlight counterintuitive approaches** (e.g., "Disappear And Come Back Unrecognizable")

### Step 5: Generate 10 Creative Titles

Generate additional titles that:
- Are based on creative intuition and direct response marketing principles
- Don't strictly follow the structural formulas above
- Draw inspiration from YouTube titles that already perform well
- Are the most clickable and relevant titles possible for the topic
- May use different hooks, formats, or psychological appeals

### Step 6: Save Output

Save the generated titles to `/youtube-title/titles-{timestamp}.md` with:
- All 30 numbered titles
- Brief explanation of psychological triggers and formulas applied
- Reference to the original input/concept

---

## Reference Titles File

**Location:** `/youtube-title/reference-titles.md`

**Purpose:** Store proven title examples that users can add to over time. The command reads this file to understand successful patterns.

### Initial Reference Titles

```markdown
# YouTube Title Reference Examples

Add high-performing YouTube titles here as references for the generator.
These examples help establish patterns for structural formulas and psychological triggers.

## Reference Titles

1. The One-Person Business Model (How To Productize Yourself)
2. How To Create A Killer YouTube Video (To Blow Up Your Channel)
3. How To Get Ahead Of 99% Of People In 6-12 Months
4. The Daily Routine That Changed My Life (4 Habits Most People Ignore)
5. Disappear For 2-4 Hours A Day (The Millionaire Productivity Routine)
6. You Won't Be The Same Person In 6 Months (Master Anything, Fast)
7. The Death Of The Personal Brand (& The Future Of Creative Work)
8. How I Turned My Life Into A Video Game
9. The Future Of Work (Avoid Learning These Skills)
10. The Most Important High-Income Skill To Learn (In The Next 10 Years)
11. A Full Guide To Reinvent Your Life (In 6-12 Months)
12. Change Your Life In 365 Hours (The New Rich Focus On These Tasks)
13. Zero To $1 Million As A One-Person Business (Working 2-4 Hours A Day)
14. Disappear And Come Back Unrecognizable (12 Rules To Change Your Life)
15. This High Income Skill Will Make You Irreplaceable
16. How To Build An Audience With Zero Followers (What They Don't Tell You)
17. How To Learn 10x Faster Than Anyone With AI
18. You're Not Forgetful: A System To Remember Everything
19. How I Manage My Time - The Trident Calendar System
20. How To Actually Achieve Your Goals In 2025 (Evidence Based)

## Adding New References

To add new reference titles:
1. Find high-performing YouTube titles in your niche
2. Add them to the list above with a number
3. The generator will incorporate these patterns into future outputs
```

---

## Constraints

| Constraint | Description |
|------------|-------------|
| **Character Limit** | Keep titles under 70 characters when possible |
| **Distinctiveness** | Ensure titles are distinct from each other (don't repeat the same formula) |
| **No Plagiarism** | Never plagiarize existing titles verbatim |
| **Core Idea Preservation** | Maintain the essence of the provided content |
| **Conviction & Polarization** | Be polarizing, have high conviction, and be hyperbolic when applicable |

---

## Output Format

### Generated Titles File Structure

```markdown
# YouTube Title Ideas

**Generated:** {YYYY-MM-DD HH:mm:ss}
**Input Concept:** [Brief summary of user's input]

---

## Structured Titles (20)

1. [TITLE 1]
2. [TITLE 2]
3. [TITLE 3]
4. [TITLE 4]
5. [TITLE 5]
6. [TITLE 6]
7. [TITLE 7]
8. [TITLE 8]
9. [TITLE 9]
10. [TITLE 10]
11. [TITLE 11]
12. [TITLE 12]
13. [TITLE 13]
14. [TITLE 14]
15. [TITLE 15]
16. [TITLE 16]
17. [TITLE 17]
18. [TITLE 18]
19. [TITLE 19]
20. [TITLE 20]

---

## Creative Titles (10)

21. [TITLE 21]
22. [TITLE 22]
23. [TITLE 23]
24. [TITLE 24]
25. [TITLE 25]
26. [TITLE 26]
27. [TITLE 27]
28. [TITLE 28]
29. [TITLE 29]
30. [TITLE 30]

---

## Analysis

### Psychological Triggers Applied
- [Trigger 1]: Used in titles [X, Y, Z]
- [Trigger 2]: Used in titles [A, B, C]
- ...

### Structural Formulas Used
- [Formula 1]: Titles [X, Y, Z]
- [Formula 2]: Titles [A, B, C]
- ...

### Notes
[Any additional observations about the title generation]
```

---

## Example Workflow

```
User: /youtube-title-generator

System: Please share your content idea, newsletter concept, or reference material.
        I'll transform it into 30 compelling YouTube title ideas.

User: I want to create a video about how I use AI tools to write 10x faster
      and produce more content as a solo creator.

System: [Analyzes input]
        [Loads reference titles from /youtube-title/reference-titles.md]
        [Generates 20 structured titles using formulas + triggers]
        [Generates 10 creative titles based on direct response principles]
        [Saves to /youtube-title/titles-2026-01-20-143052.md]

        Here are 30 YouTube title ideas for your AI writing video:

        ## Structured Titles (20)

        1. How I Write 10x Faster Than Anyone (Using AI The Right Way)
        2. The AI Writing System That Changed Everything (For Solo Creators)
        3. You Won't Believe How Fast I Create Content Now (My AI Stack)
        ...

        ## Creative Titles (10)

        21. I Let AI Write For Me For 30 Days. Here's What Happened.
        22. The Lazy Creator's Guide To 10x Output
        ...

        ## Analysis

        ### Psychological Triggers Applied
        - Time-bound promises: Titles 1, 5, 12 ("10x faster," "in 30 days")
        - Transformation language: Titles 2, 8, 15 ("changed everything")
        ...

        ✓ Saved to /youtube-title/titles-2026-01-20-143052.md
```

---

## Implementation Checklist

### Files to Create

- [ ] `/.claude/commands/youtube-title-generator.md`
- [ ] `/youtube-title/reference-titles.md`

### Folders to Create

- [ ] `/youtube-title/`

### Updates Required

- [ ] Update `CLAUDE.md` with new command documentation

---

## Future Considerations

- A/B title variant generation (same concept, different angles)
- Thumbnail concept suggestions to pair with titles
- Title length optimization analysis
- Niche-specific reference title collections
- Integration with YouTube API to analyze actual performance data
- Competitor title analysis feature
