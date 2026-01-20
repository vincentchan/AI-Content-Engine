# AI Content Engine

> Because staring at a blank page hoping for inspiration is so 2023.

An AI-powered content creation system that helps you research, ideate, and draft content like a caffeinated content team of one. Built with Claude Code, slash commands, and subagents.

## The Origin Story

I watched [this YouTube interview](https://www.youtube.com/watch?v=HhspudqFSvU&t=2s) where Greg Isenberg broke down Dan Koe's AI content workflow and my jaw hit the floor. Dan Koe—the guy whose single Twitter thread got **165 million views** (not a typo)—was sharing his actual system for creating content that resonates.

So naturally, I did what any reasonable person would do: I turned it into a Claude Code project with slash commands and subagents so I could pretend I have Dan's content superpowers.

## Credits (a.k.a. The People Who Actually Know What They're Doing)

- **[Dan Koe](https://letters.thedankoe.com/)** — Created the framework. Wrote that [165M+ view Twitter thread](https://x.com/thedankoe/status/2010751592346030461). Probably writes better content before breakfast than most of us do all week.

- **[Greg Isenberg](https://www.ideabrowser.com/)** — Conducted the interview that started this rabbit hole. Also created [a downloadable guide](https://www.gregisenberg.com/content-engine) if you want the source material.

- **[Vincent Chan](http://x.com/VincentChan)** — That's me. I just wired it all together with Claude Code, slash commands, and subagents. Standing on the shoulders of giants, etc.

## How It Works

This engine uses Claude Code's slash commands to run specialized content workflows. Each command is a prompt that orchestrates subagents to do the heavy lifting.

### The Commands

Commands are organized by stage in the content creation process:

#### Research Stage
*"Know thy audience, know thy swipe file"*

| Command | What It Does |
|---------|--------------|
| `/swipe-file-generator` | Analyzes high-performing content from URLs and builds a swipe file of patterns, hooks, and psychological triggers |
| `/content-ideas-generator` | Extracts 5 structured post outlines from your reference material (newsletters, scripts, notes, journal entries) |

#### Ideation Stage
*"Turn research into something people actually want to read"*

| Command | What It Does |
|---------|--------------|
| `/content-draft-generator` | Takes reference content, analyzes it, asks you context questions, then generates 3 variations of your new content |
| `/youtube-title-generator` | Generates 30 YouTube title ideas from your content concept using proven formulas and psychological triggers |

## Getting Started

1. **Clone this repo** (or just copy the `.claude` folder structure)

2. **Open in Claude Code** and run a command:
   ```
   /swipe-file-generator
   ```

3. **Follow the prompts** — each command will ask for input and guide you through the process

4. **Find your output** in the corresponding folder:
   - `/swipe-file/` — Your growing swipe file
   - `/content-ideas/` — Post outlines
   - `/content-draft/` — Generated drafts
   - `/youtube-title/` — Title ideas

## Project Structure

```
/AI-Content-Engine/
├── /.claude/
│   ├── /commands/          # Slash commands live here
│   └── /subagents/         # Specialized AI workers
├── /swipe-file/            # Research output
├── /content-ideas/         # Post outlines
├── /content-draft/         # Generated drafts
├── /youtube-title/         # Title ideas
├── /specs/                 # Command specifications
└── /todos/                 # Implementation notes
```

## Learn More

- **Watch the interview**: [I Watched Dan Koe Break Down His AI Workflow OMG](https://www.youtube.com/watch?v=HhspudqFSvU&t=2s)
- **Download Greg's guide**: [gregisenberg.com/content-engine](https://www.gregisenberg.com/content-engine)
- **Read Dan's newsletter**: [future/proof by Dan Koe](https://letters.thedankoe.com/)

## A Note on "Vibe Coding"

Yes, this entire project was vibe coded. No, I'm not sorry. The robots are good at this now.

---

*Built with Claude Code. Powered by coffee and existential dread about content calendars.*
