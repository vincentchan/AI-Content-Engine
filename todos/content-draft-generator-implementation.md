# Content Draft Generator Implementation Todo

**Spec:** `/specs/content-draft-generator-command-spec.md`

## Tasks

### Folder Structure
- [x] Create `/content-breakdown/` folder
- [x] Create `/content-anatomy/` folder
- [x] Create `/content-context/` folder
- [x] Create `/content-meta-prompt/` folder
- [x] Create `/content-draft/` folder

### Subagents
- [x] Create `content-anatomy-generator` subagent at `/.claude/skills/content-draft-generator/subagents/content-anatomy-generator.md`
- [x] Create `content-context-generator` subagent at `/.claude/skills/content-draft-generator/subagents/content-context-generator.md`
- [x] Create `meta-prompt-generator` subagent at `/.claude/skills/content-draft-generator/subagents/meta-prompt-generator.md`

### Command
- [x] Create `/content-draft-generator` slash command at `/.claude/skills/content-draft-generator/SKILL.md`
  - [x] Step 1: URL collection (up to 5 URLs)
  - [x] Step 2: Content deconstruction via existing subagent
  - [x] Step 3: Anatomy generation via new subagent
  - [x] Step 4: Context generation via new subagent
  - [x] Step 5: Meta prompt generation via new subagent
  - [x] Step 6: Execute generated meta prompt (Phase 1 + Phase 2)
  - [x] Step 7: Save content drafts to `/content-draft/`

### Documentation
- [x] Update `CLAUDE.md` with new command and subagent documentation

### Testing
- [x] Test full workflow end-to-end with sample URLs
