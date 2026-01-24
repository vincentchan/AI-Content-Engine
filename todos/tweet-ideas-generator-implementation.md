# Tweet Ideas Generator Implementation

## Overview

Implementation checklist for the `/tweet-ideas-generator` command based on the spec at `/specs/tweet-ideas-generator-command-spec.md`.

---

## Tasks

### 1. Create Output Folder

- [x] Create `/tweet-ideas/` directory for storing generated tweet ideas

### 2. Create Command File

- [x] Create `/.claude/skills/tweet-ideas-generator/SKILL.md`

**Command file must include:**

| Section | Content |
|---------|---------|
| **Role Definition** | Social Media Short Statement Generator specializing in Twitter content |
| **File Locations** | Output path: `/tweet-ideas/tweets-{timestamp}.md` |
| **Workflow Diagram** | 5-step visual workflow |
| **Step 1: Collect Input** | Prompt for reference material (content drafts, URLs, notes) |
| **Step 2: Deep Analysis** | Extract transformation promise, value props, pain points, big ideas |
| **Step 3: Generate 50 Categorized** | 10 statements per category across 5 categories |
| **Step 4: Generate 10 Wildcards** | Creative tweets based on direct response marketing |
| **Step 5: Save Output** | Timestamp format and file path |
| **Psychological Triggers** | Time-bound, transformation, exclusivity, status elevation |
| **Contrasting Elements** | Modest inputs → dramatic outputs, unexpected combinations |
| **Constraints** | 280 chars, distinct, no plagiarism, polarizing |
| **Output Format** | Full markdown template with sources and explanations |
| **Error Handling** | No input, URL failures, insufficient content |

### 3. Implement 5 Categories

Each category needs 10 statements with examples:

#### Category 1: Harsh Life Advice
- [x] Uncomfortable truths delivered with conviction
- [x] Advice people need but avoid
- [x] Example prompts and tone guidance

#### Category 2: Most Impactful Quotes
- [x] Direct quotes from reference material
- [x] Paraphrased wisdom that stands alone
- [x] Source attribution guidance

#### Category 3: Core Problems/Pain Points
- [x] Statements that name the struggle
- [x] Make readers feel seen and understood
- [x] Problem-awareness language

#### Category 4: Counterintuitive Truths
- [x] Paradoxical insights
- [x] Challenge conventional wisdom
- [x] "Opposite of expected" framing

#### Category 5: Key Insights/Wisdom/Big Ideas
- [x] Core transformational concepts
- [x] Essence of the content distilled
- [x] Big-picture thinking

### 4. Implement Psychological Triggers

- [x] Time-bound promises ("In 30 days...", "This week...")
- [x] Transformation language ("Become...", "Transform...", "Unlock...")
- [x] Exclusivity framing ("Most people won't...", "The 1% know...")
- [x] Status elevation ("Level up...", "Separate yourself...")

### 5. Implement Contrasting Elements

- [x] Modest inputs → Dramatic outputs ("10 minutes a day → different life")
- [x] Unexpected combinations ("Laziness is a skill")
- [x] Counterintuitive approaches ("Work less, earn more")

### 6. Implement Creative Wildcards Section

- [x] 10 statements based on direct response marketing
- [x] No category constraints
- [x] Model tweets that already work
- [x] Most engaging possible

### 7. Implement Output Format

- [x] 60 numbered tweets organized by category
- [x] Source attribution for each tweet (when available)
- [x] Brief explanation for each tweet
- [x] Analysis notes section:
  - [x] Psychological triggers applied
  - [x] Structural formulas used
  - [x] Content themes extracted
  - [x] Recommendations

### 8. Implement Constraints

- [x] Character limit check (under 280 when possible)
- [x] Distinctness validation (no repeated formulas)
- [x] Core idea fidelity (maintain reference essence)
- [x] Tone guidance (polarizing, high conviction, hyperbolic)
- [x] Category flexibility (skip if content doesn't fit)

### 9. Update CLAUDE.md

- [x] Add `/tweet-ideas-generator` to Commands section
- [x] Add output folder to Architecture diagram
- [x] Add to specs and todos in Architecture

**Documentation to add:**

```markdown
### /tweet-ideas-generator

Generates 60 high-impact tweet ideas from reference content.

**Usage:** Run `/tweet-ideas-generator` to:
1. Provide reference material (content drafts, newsletters, URLs, notes)
2. Extract key takeaways and compelling concepts
3. Generate 50 categorized statements across 5 categories
4. Generate 10 creative wildcard tweets
5. Save all 60 ideas with sources and explanations

**Location:** `/.claude/skills/tweet-ideas-generator/SKILL.md`

**Output Folder:** `/tweet-ideas/`

**Key Files:**
- `/tweet-ideas/tweets-{timestamp}.md` - Generated tweet ideas
```

### 10. Update README.md

- [x] Add `/tweet-ideas-generator` to appropriate stage section
- [x] Add to Getting Started examples
- [x] Add `/tweet-ideas/` to output folders list
- [x] Add to Project Structure

### 11. Test the Command

- [ ] Run `/tweet-ideas-generator` with sample content
- [ ] Verify all 5 categories generate 10 statements each
- [ ] Verify 10 creative wildcards are generated
- [ ] Verify statements are under 280 characters
- [ ] Verify sources are attributed correctly
- [ ] Verify explanations are included
- [ ] Verify output file saves with correct timestamp
- [ ] Verify analysis notes section is complete
- [ ] Test with URL input
- [ ] Test error handling with insufficient content

---

## File Locations

| File | Purpose |
|------|---------|
| `/specs/tweet-ideas-generator-command-spec.md` | Full specification |
| `/.claude/skills/tweet-ideas-generator/SKILL.md` | Command implementation |
| `/tweet-ideas/tweets-{timestamp}.md` | Generated outputs |
| `/todos/tweet-ideas-generator-implementation.md` | This file |

---

## Categories Quick Reference

| Category | Focus | Tone |
|----------|-------|------|
| **Harsh Life Advice** | Uncomfortable truths | Direct, no-nonsense |
| **Most Impactful Quotes** | Extracted wisdom | Quotable, memorable |
| **Core Problems/Pain Points** | Name the struggle | Empathetic, relatable |
| **Counterintuitive Truths** | Paradoxes | Surprising, thought-provoking |
| **Key Insights/Big Ideas** | Core concepts | Transformational, expansive |
| **Creative Wildcards** | Best of the best | Maximum engagement |

---

## Psychological Triggers Checklist

- [x] Time-bound promises applied across ideas
- [x] Transformation language incorporated
- [x] Exclusivity framing where appropriate
- [x] Status elevation triggers included

---

## Output Structure Reference

### Per Tweet Format
```
1. "[TWEET TEXT]" [SOURCE: if available]
   - *[Brief explanation of why this works]*
```

### Analysis Notes Format
```
### Psychological Triggers Applied
- Time-bound promises: Ideas #X, #Y, #Z
- Transformation language: Ideas #X, #Y, #Z
- Exclusivity framing: Ideas #X, #Y, #Z
- Status elevation: Ideas #X, #Y, #Z

### Structural Formulas Used
- [Formula]: [How applied]

### Content Themes Extracted
- [Theme 1]
- [Theme 2]

### Recommendations
[Engagement potential notes]
```

---

## Constraints Checklist

- [x] All statements under 280 characters (when possible)
- [x] Each statement is distinct (no formula repetition)
- [x] No verbatim plagiarism
- [x] Maintains core idea from reference
- [x] Polarizing and high conviction tone
- [x] Categories skipped if content doesn't fit
