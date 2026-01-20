# Swipe File Generator Implementation Todo

**Spec:** `/specs/swipe-file-generator-command-spec.md`

## Tasks

- [x] Create folder structure (`/.claude/commands/`, `/.claude/subagents/`, `/swipe-file/`)
- [x] Create `/swipe-file-generator` slash command at `/.claude/commands/swipe-file-generator.md`
- [x] Create `content-deconstructor` subagent at `/.claude/subagents/content-deconstructor.md`
- [x] Create initial `/swipe-file/swipe-file-sources.md` template
- [x] Create initial `/swipe-file/.digested-urls.json` registry
- [x] Create initial `/swipe-file/swipe-file.md` template
- [x] Update `CLAUDE.md` with project documentation
- [x] Update to batch processing (fetch all URLs, single subagent call for all content)
- [x] Fix file structure to use Claude Code conventions (`.claude/commands/` and `.claude/subagents/`)
- [x] Add FxTwitter API support for Twitter/X URLs (bypasses JavaScript requirement)
