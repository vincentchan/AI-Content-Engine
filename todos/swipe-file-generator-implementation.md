# Swipe File Generator Implementation Todo

**Spec:** `/specs/swipe-file-generator-command-spec.md`

## Tasks

- [x] Create folder structure (`/.claude/skills/swipe-file-generator/`, `/.claude/skills/swipe-file-generator/subagents/`, `/swipe-file/`)
- [x] Create `/swipe-file-generator` slash command at `/.claude/skills/swipe-file-generator/SKILL.md`
- [x] Create `content-deconstructor` subagent at `/.claude/skills/swipe-file-generator/subagents/content-deconstructor.md`
- [x] Create initial `/swipe-file/swipe-file-sources.md` template
- [x] Create initial `/swipe-file/.digested-urls.json` registry
- [x] Create initial `/swipe-file/swipe-file.md` template
- [x] Update `CLAUDE.md` with project documentation
- [x] Update to batch processing (fetch all URLs, single subagent call for all content)
- [x] Migrated to skills format (`.claude/skills/swipe-file-generator/SKILL.md` with co-located subagents)
- [x] Add FxTwitter API support for Twitter/X URLs (bypasses JavaScript requirement)
- [x] Add auto-generated Table of Contents with linked titles, types, and dates
