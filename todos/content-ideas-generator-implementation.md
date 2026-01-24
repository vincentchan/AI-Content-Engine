# Content Ideas Generator Implementation

## Overview

Implementation checklist for the `/content-ideas-generator` command based on the spec at `/specs/content-ideas-generator-command-spec.md`.

---

## Tasks

### 1. Create Output Folder

- [ ] Create `/content-ideas/` directory for storing generated outlines

### 2. Create Command File

- [ ] Create `/.claude/skills/content-ideas-generator/SKILL.md`

**Command file must include:**

| Section | Content |
|---------|---------|
| **Role Definition** | Social Media Post Outline Generator specializing in wisdom-style posts |
| **File Locations** | Output path: `/content-ideas/ideas-{timestamp}.md` |
| **Workflow Diagram** | 6-step visual workflow |
| **Step 1: Collect Input** | Prompt for reference material (newsletters, scripts, notes, etc.) |
| **Step 2: Deep Analysis** | Extract themes, paradoxes, problems, archetypes, objections, insights, metaphors, principles |
| **Step 3: Develop Concepts** | 5-step development process per concept |
| **Step 4: Structure Outlines** | 11 components per outline |
| **Step 5: Language Techniques** | 7 specific techniques to apply |
| **Step 6: Save Output** | Timestamp format and file path |
| **Knowledge Base** | 3 example phrasing samples |
| **Constraints** | Outlines only, distinct themes, source fidelity, quality over quantity |
| **Output Format** | Full markdown template |
| **Error Handling** | No input, URL failures, insufficient content |

### 3. Update CLAUDE.md

- [ ] Add `/content-ideas-generator` to Commands section
- [ ] Add output folder to Architecture diagram
- [ ] Add to Key Files table if needed

**Documentation to add:**

```markdown
### /content-ideas-generator

Generates structured post outlines from reference materials.

**Usage:** Run `/content-ideas-generator` to:
1. Provide reference material (newsletters, scripts, notes, journal entries)
2. Extract 5 distinct post concepts with paradoxes and transformation arcs
3. Generate structured outlines with examples, objections, and actionable steps
4. Save outlines to timestamped file

**Location:** `/.claude/skills/content-ideas-generator/SKILL.md`

**Output Folder:** `/content-ideas/`
```

### 4. Test the Command

- [ ] Run `/content-ideas-generator` with sample newsletter content
- [ ] Verify all 5 outlines are generated with correct structure
- [ ] Verify output file is saved with correct timestamp format
- [ ] Verify language techniques are applied correctly
- [ ] Test error handling with insufficient content

---

## File Locations

| File | Purpose |
|------|---------|
| `/specs/content-ideas-generator-command-spec.md` | Full specification |
| `/.claude/skills/content-ideas-generator/SKILL.md` | Command implementation |
| `/content-ideas/ideas-{timestamp}.md` | Generated outputs |
| `/todos/content-ideas-generator-implementation.md` | This file |

---

## Outline Structure Reference

Each of the 5 post outlines must include:

1. **Core Paradox** + 3 rephrased versions (progressively shorter)
2. **Key Quotes** (3+ from reference material)
3. **Transformation Arc** (challenge → revelation → transcendence)
4. **Core Problems** (3 tangible pain points)
5. **Key Examples** (3 concrete illustrations)
6. **Reader Objections** (3 written as reader would say them)
7. **Aspirational Statement** (1-2 sentences)
8. **Actionable Steps** (3+ staccato-style steps)
9. **Big Idea** (1-2 sentences)
10. **Memorable Closing Insight** (1 sentence)

---

## Language Techniques Checklist

- [ ] Second-person "you" used consistently
- [ ] Imperative verbs ("Be," "Reset," "Let go," "Build")
- [ ] Visual metaphors with elemental forces
- [ ] Absolute language ("everything," "impossible," "never")
- [ ] No qualifiers or hedges
- [ ] Concrete timeframes for authority
- [ ] Opposing pairs to highlight paradoxes
