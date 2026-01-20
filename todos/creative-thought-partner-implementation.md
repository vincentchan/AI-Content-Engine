# Creative Thought Partner Implementation

## Overview

Implementation checklist for the `/creative-thought-partner` command based on the spec at `/specs/creative-thought-partner-command-spec.md`.

---

## Tasks

### 1. Create Output Folder

- [x] Create `/creative-thoughts/` directory for storing session transcripts

### 2. Create Command File

- [x] Create `/.claude/commands/creative-thought-partner.md`

**Command file must include:**

| Section | Content |
|---------|---------|
| **Role Definition** | Creative thought partner focused on revealing hidden brilliance through critical observations |
| **Core Identity** | "Fresh eyes" that spot patterns, paradoxes, and unnamed concepts |
| **File Locations** | Output path: `/creative-thoughts/session-{timestamp}.md` |
| **Workflow Diagram** | 5-step visual workflow |
| **Opening Script** | "Unwrapping a gift" metaphor + redirect instructions |
| **Four Breakthrough Drivers** | Pattern Spotting, Paradox Hunting, Naming the Unnamed, Contrast Creation |
| **Flow Guidelines** | One question at a time, challenge generic claims, prioritize paradoxes, no compliments |
| **Constraints** | Natural conversation, original insights only, avoid generic terms, complete the naming |
| **Output Format** | Narrative arc + breakthroughs summary + full transcript template |
| **Redirect Handling** | Responses to "wrong direction," "switch topics," etc. |
| **Error Handling** | No topic, flat conversation, user stuck, insufficient material |

### 3. Implement Four Breakthrough Drivers

Each driver needs example questions/observations:

#### Driver 1: Pattern Spotting
- [x] "I notice you emphasize X while most focus on Y—tell me more"
- [x] "That's different from how most people approach this"
- [x] "There's a pattern here. Do you see it?"

#### Driver 2: Paradox Hunting
- [x] "It sounds like you get more by doing less—is that intentional?"
- [x] "You're saying weakness becomes strength here—tell me about that"
- [x] "That's backwards from usual advice. Why does it work for you?"

#### Driver 3: Naming the Unnamed
- [x] "This seems like it has a name—what do you call this approach?"
- [x] "There's a mechanism here you haven't labeled yet"
- [x] Name testing: "Does [proposed name] capture this?"

#### Driver 4: Contrast Creation
- [x] "So while most people do X, you're doing Y. Why does your difference matter?"
- [x] "What would the exact opposite look like?"
- [x] "If someone copied your surface approach but missed the core, what would they get wrong?"

### 4. Implement Flow Guidelines

- [x] One question at a time (build on previous answer)
- [x] Challenge generic claims with follow-up until specific insights emerge
- [x] Prioritize paradoxes—dig deeper immediately when sensed
- [x] No compliments—just observe, challenge, or dig deeper
- [x] Don't move on until concept is named
- [x] Know when to stop (enough material for breakthrough insights)

### 5. Implement Redirect Handling

- [x] "We're going in the wrong direction" → "Got it. What direction feels more right?"
- [x] "Switch topics" → "Sure. What else is on your mind?"
- [x] "I don't understand this" → Rephrase or approach differently
- [x] "This isn't landing" → "What would be more useful to explore?"

### 6. Implement Output Format

- [x] Narrative arc summary (bullet points: starting point → turns → discoveries → crystallization)
- [x] Breakthroughs summary (named concepts with 2-3 sentence descriptions)
- [x] Full transcript with headlines separating topics/breakthroughs
- [x] Session notes (patterns, paradoxes, concepts named, potential applications)

### 7. Update CLAUDE.md

- [x] Add `/creative-thought-partner` to Commands section
- [x] Add output folder to Architecture diagram
- [x] Add to Key Files table if needed

**Documentation to add:**

```markdown
### /creative-thought-partner

A conversational creative thought partner that reveals hidden brilliance in your ideas.

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
```

### 8. Test the Command

- [ ] Run `/creative-thought-partner` with a real topic
- [ ] Verify opening script includes "unwrapping a gift" metaphor
- [ ] Verify redirect handling works ("wrong direction," "switch topics")
- [ ] Verify all four breakthrough drivers are applied appropriately
- [ ] Verify conversation feels natural, not like a questionnaire
- [ ] Verify paradoxes are prioritized when sensed
- [ ] Verify concepts are named before moving on
- [ ] Verify output file includes narrative arc, breakthroughs summary, and full transcript
- [ ] Verify timestamp format is correct

---

## File Locations

| File | Purpose |
|------|---------|
| `/specs/creative-thought-partner-command-spec.md` | Full specification |
| `/.claude/commands/creative-thought-partner.md` | Command implementation |
| `/creative-thoughts/session-{timestamp}.md` | Generated outputs |
| `/todos/creative-thought-partner-implementation.md` | This file |

---

## Breakthrough Drivers Quick Reference

| Driver | Purpose | Key Question |
|--------|---------|--------------|
| **Pattern Spotting** | Find gaps between their approach and standard methods | "I notice you do X while most do Y—why?" |
| **Paradox Hunting** | Find counterintuitive truths where opposite works | "You get more by doing less—intentional?" |
| **Naming the Unnamed** | Help articulate concepts they use but haven't crystallized | "What do you call this approach?" |
| **Contrast Creation** | Highlight uniqueness by finding the opposite | "If someone missed the core insight, what would they get wrong?" |

---

## Conversation Flow Checklist

- [x] Start with opening script (unwrapping gift metaphor)
- [x] Collect topic/idea to explore
- [x] Ask one question at a time
- [x] Build each question on previous answer
- [x] Challenge generic claims ("I care more") until specific
- [x] When paradox sensed → dig deeper immediately
- [x] When unnamed concept spotted → probe for name
- [x] Test names collaboratively ("Does X capture this?")
- [x] Don't move on until concept is named
- [x] Stop when enough material for breakthroughs
- [x] Generate output with all required sections

---

## Output Structure Reference

### Narrative Arc (bullet points)
- Starting Point
- First Turn
- Key Discovery #1
- Deepening
- Key Discovery #2
- Crystallization
- Final Insight

### Breakthroughs Summary
- Breakthrough 1: [Name] + 2-3 sentence description
- Breakthrough 2: [Name] + 2-3 sentence description
- (Additional as discovered)

### Full Transcript
- Opening section
- Headlines separating topics/threads
- Complete conversation word for word
- Headlines marking breakthrough moments

### Session Notes
- Patterns observed
- Paradoxes discovered
- Concepts named (with definitions)
- Potential applications
