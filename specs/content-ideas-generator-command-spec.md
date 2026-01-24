# Content Ideas Generator Command Specification

## Overview

A social media post outline generator that extracts compelling concepts from reference materials and transforms them into structured outlines for engaging, wisdom-style social posts. The system identifies paradoxical truths, transformational narratives, and powerful insights—producing outlines that users can develop into full posts themselves.

## Components

### 1. `/content-ideas-generator` Skill

**Location:** `/.claude/skills/content-ideas-generator/SKILL.md`

**Purpose:** Generate 5 distinct, structured post outlines from user-provided reference material, focusing on counterintuitive truths, transformation arcs, and emotionally resonant insights.

---

## File Structure

```
/AI-Content-Engine/
├── /.claude/
│   └── /skills/
│       └── content-ideas-generator/
│           └── SKILL.md
├── /content-ideas/
│   └── ideas-{timestamp}.md            # Generated post outlines
└── /specs/
    └── content-ideas-generator-command-spec.md
```

### File Naming Convention

- Generated outlines: `ideas-{YYYY-MM-DD-HHmmss}.md`
- Example: `ideas-2026-01-20-143052.md`

---

## Workflow

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         /content-ideas-generator                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  Step 1: Collect reference material                                         │
│       → Newsletters, scripts, notes, journal entries, or other content     │
│       ↓                                                                     │
│  Step 2: Deep analysis                                                      │
│       → Extract themes, paradoxes, pain points, insights, metaphors        │
│       ↓                                                                     │
│  Step 3: Develop 5 post concepts                                            │
│       → Apply development process for each concept                          │
│       ↓                                                                     │
│  Step 4: Structure each outline                                             │
│       → Core paradox, transformation arc, examples, objections, steps      │
│       ↓                                                                     │
│  Step 5: Apply language techniques                                          │
│       → Second-person, imperatives, absolutes, visual metaphors            │
│       ↓                                                                     │
│  Step 6: Save output                                                        │
│       → Save to /content-ideas/ideas-{timestamp}.md                         │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Step-by-Step Behavior

### Step 1: Collect Reference Material

Prompt the user:
> "Please share your reference material (newsletters, scripts, notes, journal entries, or other content). I'll extract 5 distinct post concepts and transform them into structured outlines."

Accept any of the following:
- Newsletters or articles
- Video scripts or transcripts
- Personal notes or journal entries
- Raw ideas or brainstorms
- URLs to fetch and analyze

If the user provides a URL, use WebFetch to retrieve the content.

### Step 2: Deep Analysis

Thoroughly analyze the reference material to identify:

| Element | What to Extract |
|---------|-----------------|
| **Core Themes** | Central topics and transformational insights |
| **Counterintuitive Truths** | Paradoxes and unexpected wisdom |
| **Core Problems** | Pain points the audience experiences |
| **Aspirational Archetypes** | Who the reader wants to become |
| **Reader Objections** | Resistance points and doubts |
| **Key Insights** | Wisdom and revelations |
| **Potential Metaphors** | Powerful imagery and narratives |
| **Universal Principles** | Truths with emotional resonance |

### Step 3: Develop 5 Post Concepts

For each of the 5 concepts, follow this development process:

1. **Choose a counterintuitive truth** from the reference material
2. **Frame it as an absolute principle** (no hedging or qualifiers)
3. **Generate short, practical examples** that illustrate the truth
4. **Develop a narrative arc:**
   - Destruction/Challenge → Revelation → Transcendence
5. **Craft a memorable closing insight** that ties everything together

### Step 4: Structure Each Outline

For each post outline, extract and organize:

| Component | Description |
|-----------|-------------|
| **Core Paradox** | The central counterintuitive truth or tension that creates interest |
| **Key Quotes** | Direct quotes from the reference material for the given outline |
| **Big Idea** | The transformational concept that forms the post's foundation |
| **Core Problems** | 2-3 short, tangible, relatable pain points in the archetype's personal life |
| **Aspirational Statement** | The what and why behind traits/skills to develop |
| **Key Examples** | 2-3 short, concrete illustrations that support the big idea |
| **Reader Objections** | 2-3 short, relevant, unique objections written as the reader would say them |
| **Transformation Arc** | How the narrative progresses from challenge to revelation to transcendence |
| **Actionable Steps** | Staccato-style steps that align with the transformation arc and aspirational statement |
| **Memorable Closing Insight** | A one-sentence insight that ties everything together |

### Step 5: Apply Language Techniques

Apply these specific language techniques throughout:

| Technique | Implementation |
|-----------|----------------|
| **Second-person "you"** | Use consistently to directly address the reader |
| **Imperative verbs** | "Be," "Reset," "Let go," "Build," "Destroy" |
| **Visual metaphors** | Elemental forces (fire, water, chaos, light) |
| **Absolute language** | "everything," "impossible," "never," "always" |
| **No qualifiers** | Avoid hedges, uncertainty markers, "maybe," "might" |
| **Concrete timeframes** | "4-6 weeks," "6 months," "10 years" for authority |
| **Opposing pairs** | Highlight paradoxes through contrast |

### Step 6: Save Output

1. Generate timestamp in format: `YYYY-MM-DD-HHmmss`
2. Save the complete output to `/content-ideas/ideas-{timestamp}.md`
3. Report to user: "✓ Post outlines saved to /content-ideas/ideas-{timestamp}.md"

---

## High-Engagement Elements

Focus on elements with high engagement potential:

| Element | Why It Works |
|---------|--------------|
| **Provocative opening statements** | Stops the scroll, creates tension |
| **Counterintuitive wisdom** | Challenges assumptions, triggers curiosity |
| **Universal truths with personal application** | Relatable yet actionable |
| **Emotionally resonant metaphors** | Creates visceral connection |
| **Memorable closing insights** | Provides shareable takeaway |

### Structural Patterns to Extract

- Short, declarative statement possibilities
- Opportunities for parallel structure
- Places for imperative verbs
- Potential for absolute statements
- Visual metaphors involving elemental forces

---

## Knowledge Base: Example Phrasing

### Example 1: The Blank Slate

> The best way to 'get your spark back' is burning everything down. You have to reset your life. You have to reset your mind. You have to let go of everything you were, everything you had, every lie you told yourself. Then, something else can take their place. Only a few do it. They let go of years and decades, wins and failures, skills and pride-to go somewhere new. It's hard, but simple. You can restart any time you want. Any time you have the strength. There's no feeling like it. Beauty starts with a blank slate. And a blank slate starts with the fiery destruction of your entire existence. Eventually, that inferno turns from pain to warmth. You sit there for a while. Basking in it. Then, The Idea hits you. And you're never the same again.

### Example 2: The Paradox

> Be a paradox. Build one thing, but don't be one thing. Be an artist and a capitalist. Be a savage and saint. Treat business like a game. Treat fitness like meditation. Believe in God. Believe in yourself. War and art. Spirit and profit. Be an insatiable serial killer in work. Be a golden retriever in life. Do everything to the extreme. You should be easy to recognize, but impossible to label. You stand outside the boxes that the world is divided by. The paradox is where magic happens. You give the world something new, by becoming something new. It's a line, between two opposites, that most never touch. Chaos and simplicity. Genius and madness. Greatness doesn't come from sitting on that tightrope. It comes from sprinting on it.

### Example 3: The Isolation

> It takes 4-6 weeks of uncomfortable isolation to rediscover who you are. Vision is formed alone. You can't listen to friends. You can't listen to family. You can't listen to critics. What you're meant to do- is seen through your eyes only. Other eyes will filter them. To their dreams. To their desires. To their view of what's possible. Don't seek attention when you don't know yourself. That confusion is a gift. When you embrace it, everything changes. Your reality must break a few times before your path becomes clear.

---

## Constraints

| Constraint | Requirement |
|------------|-------------|
| **Outlines Only** | Generate outlines, not complete posts |
| **Depth Over Tactics** | Focus on emotional resonance over tactical advice |
| **Distinct Themes** | Each of the 5 outlines must have a distinct theme |
| **Quality Over Comprehensiveness** | Prioritize engagement potential |
| **Source Fidelity** | Don't add information not implied in the reference material |
| **Insufficient Content Handling** | If reference material lacks sufficient content, note this and extract what's possible |

---

## Output Format

### Generated Outlines File Structure

```markdown
# Content Ideas - Post Outlines

**Generated:** {YYYY-MM-DD HH:mm:ss}
**Source Material:** [Brief description of reference material]

---

## POST OUTLINE 1

### Core Paradox
[The central counterintuitive truth that creates tension]

**Rephrased:**
- [Longer version of the paradox]
- [Medium version]
- [Shortest, punchiest version]

### Key Quotes
- "[Key quote 1 from reference material]"
- "[Key quote 2 from reference material]"
- "[Key quote 3 from reference material]"
- [Additional key quotes if relevant]

### Transformation Arc
[Brief description of how the narrative would progress: destruction/challenge → revelation → transcendence]

### Core Problems
- [Problem 1 - short, tangible, relatable]
- [Problem 2]
- [Problem 3]

### Key Examples
- [Example 1 - concrete illustration]
- [Example 2]
- [Example 3]

### Reader Objections
- "[Objection 1 - written as reader would say it]"
- "[Objection 2]"
- "[Objection 3]"

### Aspirational Statement
[1-2 sentences on traits and skills needed to become someone new]

### Actionable Steps
1. [Step 1 - staccato style]
2. [Step 2]
3. [Step 3]
4. [Additional steps as needed]

### Big Idea
[The transformational concept in 1-2 sentences]

### Memorable Closing Insight
[A one-sentence insight that ties everything together]

---

## POST OUTLINE 2

[Same structure as above]

---

## POST OUTLINE 3

[Same structure as above]

---

## POST OUTLINE 4

[Same structure as above]

---

## POST OUTLINE 5

[Same structure as above]

---

## Analysis Notes

### Themes Extracted
- [Theme 1]
- [Theme 2]
- [Theme 3]

### Language Patterns Applied
- Second-person "you": [Examples]
- Imperative verbs used: [List]
- Visual metaphors: [List]
- Absolute language: [Examples]

### Recommendations
[Any additional observations about the outlines, standout concepts, or suggestions for development]
```

---

## Example Workflow

```
User: /content-ideas-generator

System: Please share your reference material (newsletters, scripts, notes,
        journal entries, or other content). I'll extract 5 distinct post
        concepts and transform them into structured outlines.

User: [Pastes a newsletter about the power of strategic quitting and
       knowing when to walk away from projects]

System: [Analyzes reference material]
        [Extracts themes, paradoxes, pain points, insights]
        [Develops 5 distinct post concepts]
        [Structures each outline with all components]
        [Applies language techniques]
        [Saves to /content-ideas/ideas-2026-01-20-143052.md]

        Here are 5 post outlines extracted from your newsletter:

        ## POST OUTLINE 1

        ### Core Paradox
        Winners quit more than losers—they just quit the right things.

        **Rephrased:**
        - The most successful people aren't those who never give up—they're
          the ones who give up strategically on everything except what matters
        - Success comes from strategic quitting, not blind persistence
        - Quit more. Win more.

        ### Key Quotes
        - "The sunk cost fallacy keeps us chained to dead-end paths"
        - "Every 'yes' to the wrong thing is a 'no' to the right thing"
        ...

        [Continues with all 5 outlines]

        ✓ Post outlines saved to /content-ideas/ideas-2026-01-20-143052.md
```

---

## Error Handling

### No Input Provided
- If user provides no input, prompt them again with examples of acceptable reference material

### URL Fetch Failure
- If a URL fails to fetch, inform the user and ask for alternative input
- Offer to proceed with any text/description they can provide directly

### Insufficient Content
- If reference material lacks sufficient depth for 5 distinct outlines:
  - Note the limitation to the user
  - Generate as many quality outlines as the material supports
  - Suggest what additional context might help

---

## Implementation Checklist

### Files to Create

- [x] `/.claude/skills/content-ideas-generator/SKILL.md`

### Folders to Create

- [ ] `/content-ideas/`

### Updates Required

- [ ] Update `CLAUDE.md` with new command documentation

---

## Future Considerations

- Reference examples file (similar to youtube-title reference-titles.md)
- Post style presets (philosophical, tactical, story-driven)
- Platform-specific formatting (Twitter thread vs. LinkedIn vs. Instagram)
- Integration with content-draft-generator for full post development
- Engagement pattern analysis from user's past posts
- Voice/tone calibration based on user's writing samples
