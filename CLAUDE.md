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

### /content-draft-generator

Generates new content drafts based on reference content analysis.

**Usage:** Run `/content-draft-generator` to:
1. Provide up to 5 reference content URLs
2. Analyze and deconstruct reference content
3. Generate a comprehensive content anatomy guide
4. Create context questions for content creation
5. Generate and execute a meta prompt for draft creation
6. Produce 3 variations of your new content

**Location:** `/.claude/commands/content-draft-generator.md`

**Output Folders:**
- `/content-breakdown/` - Deconstructed reference content
- `/content-anatomy/` - Synthesized content guides
- `/content-context/` - Context requirements
- `/content-meta-prompt/` - Generated meta prompts
- `/content-draft/` - Final content draft variations

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

### content-anatomy-generator

Synthesizes multiple content breakdowns into a comprehensive guide.

**Location:** `/.claude/subagents/content-anatomy-generator.md`

**Generates:**
- Core structure blueprint
- Psychological playbook
- Hook library
- Pacing & flow guide
- Fill-in-the-blank templates

### content-context-generator

Analyzes content guides to determine required user context.

**Location:** `/.claude/subagents/content-context-generator.md`

**Generates:**
- Essential context questions (topic, audience, goals, voice)
- Optional context suggestions
- Context gathering guidance

### meta-prompt-generator

Creates well-structured, verifiable prompts for content creation.

**Location:** `/.claude/subagents/meta-prompt-generator.md`

**Features:**
- Task decomposition
- Expert persona coordination
- Hallucination minimization
- Iterative verification

## Architecture

```
/AI-Content-Engine/
├── /.claude/
│   ├── /commands/
│   │   ├── swipe-file-generator.md
│   │   └── content-draft-generator.md
│   └── /subagents/
│       ├── content-deconstructor.md
│       ├── content-anatomy-generator.md
│       ├── content-context-generator.md
│       └── meta-prompt-generator.md
├── /swipe-file/
│   ├── swipe-file.md
│   ├── swipe-file-sources.md
│   └── .digested-urls.json
├── /content-breakdown/                  # Reference content analysis
├── /content-anatomy/                    # Synthesized content guides
├── /content-context/                    # Context requirements
├── /content-meta-prompt/                # Generated meta prompts
├── /content-draft/                      # Final content draft variations
├── /specs/
│   ├── swipe-file-generator-command-spec.md
│   └── content-draft-generator-command-spec.md
└── /todos/
    ├── swipe-file-generator-implementation.md
    └── content-draft-generator-implementation.md
```

## Key Files

| File | Purpose |
|------|---------|
| `/swipe-file/swipe-file-sources.md` | Add URLs here for analysis |
| `/swipe-file/swipe-file.md` | Master swipe file with all analyses |
| `/swipe-file/.digested-urls.json` | Tracks which URLs have been processed |
