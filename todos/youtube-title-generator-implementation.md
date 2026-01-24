# YouTube Title Generator Implementation Todo

**Spec:** `/specs/youtube-title-generator-command-spec.md`

## Tasks

### Folder Structure
- [x] Create `/youtube-title/` folder

### Reference File
- [x] Create `/youtube-title/reference-titles.md` with initial 20 reference titles
  - [x] Include instructions for adding new references
  - [x] Format as numbered list for easy parsing

### Command
- [x] Create `/youtube-title-generator` slash command at `/.claude/skills/youtube-title-generator/SKILL.md`
  - [x] Step 1: Prompt user for content idea/reference material
  - [x] Step 2: Analyze input for transformation promise, value props, audience benefits, timeframes, big ideas
  - [x] Step 3: Load reference titles from `/youtube-title/reference-titles.md`
  - [x] Step 4: Generate 20 structured titles using formulas:
    - [x] Bold Statement + (Supporting Detail/Method)
    - [x] How To + Desirable Outcome + (Mechanism/Approach)
    - [x] Time-Bound Element + (What To Focus On)
  - [x] Step 5: Apply psychological triggers:
    - [x] Time-bound promises (6-12 months, 365 hours, 2-4 hours)
    - [x] Transformation language (won't be the same, change your life)
    - [x] Exclusivity framing (what they don't tell you, most people ignore)
    - [x] Status elevation (get ahead of 99%, high-income, millionaire)
  - [x] Step 6: Generate 10 creative titles (direct response marketing principles)
  - [x] Step 7: Save output to `/youtube-title/titles-{timestamp}.md`
  - [x] Step 8: Display titles with analysis of triggers and formulas used

### Constraints Implementation
- [x] Ensure titles stay under 70 characters when possible
- [x] Ensure all 30 titles are distinct (no repeated formulas)
- [x] Never plagiarize reference titles verbatim
- [x] Maintain polarizing, high-conviction, hyperbolic tone

### Output Format
- [x] Include timestamp and input concept summary
- [x] Separate structured titles (1-20) from creative titles (21-30)
- [x] Add analysis section explaining psychological triggers applied
- [x] Add analysis section explaining structural formulas used

### Documentation
- [x] Update `CLAUDE.md` with new command documentation

### Testing
- [ ] Test with a basic content idea
- [ ] Test with newsletter/article reference material
- [ ] Test with URL input (if supported)
- [ ] Verify reference titles file is read correctly
- [ ] Verify output saves to correct location with timestamp
