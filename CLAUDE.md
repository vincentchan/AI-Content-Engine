# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

AI-Content-Engine - A system for analyzing high-performing content to study structure, psychological patterns, and ideas. The engine deconstructs content from URLs and compiles insights into a continuously refined swipe file document.

## Commands

### /swipe-file-generator

Analyzes high-performing content from URLs and builds a swipe file.

**Usage:** Run `/swipe-file-generator` to:
1. Check `/swipe-file/swipe-file-sources.md` for URLs to process
2. Identify new URLs that haven't been digested yet
3. Fetch and analyze each URL using the content-deconstructor subagent
4. Append analyses to `/swipe-file/swipe-file.md`

**Location:** `/.claude/commands/swipe-file-generator.md`

## Subagents

### content-deconstructor

Analyzes individual pieces of content to extract recreatable patterns and insights.

**Location:** `/.claude/subagents/content-deconstructor.md`

**Analyzes:**
- Structural breakdown (hooks, flow, organization, CTA)
- Psychological patterns (persuasion, emotions, biases)
- Writing mechanics (headlines, formatting, storytelling)
- Content strategy (audience, positioning, objections)
- Recreatable templates and frameworks

## Architecture

```
/AI-Content-Engine/
├── /.claude/
│   ├── /commands/
│   │   └── swipe-file-generator.md    # Slash command instructions
│   └── /subagents/
│       └── content-deconstructor.md   # Subagent instructions
├── /swipe-file/
│   ├── swipe-file.md                  # Master swipe file document
│   ├── swipe-file-sources.md          # Source URLs to process
│   └── .digested-urls.json            # Registry of processed URLs
├── /specs/
│   └── swipe-file-generator-command-spec.md
└── /todos/
    └── swipe-file-generator-implementation.md
```

## Key Files

| File | Purpose |
|------|---------|
| `/swipe-file/swipe-file-sources.md` | Add URLs here for analysis |
| `/swipe-file/swipe-file.md` | Master swipe file with all analyses |
| `/swipe-file/.digested-urls.json` | Tracks which URLs have been processed |
