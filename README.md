# ystack

Most successful startups have people that are brilliant yet flawed. Aligned yet in productive conflict. Maybe that's where some of the magic happens.

**ystack** (for yolostack) is a set of AI agent personas for building autonomous teams. Inspired by [Garry Tan's gstack](https://github.com/garrynewman/gstack), which gives Claude Code an elite engineering team — ystack gives it the team you actually have.

## Live

ystack powers the autonomous startup [ystackai.com](https://ystackai.com). 6 agents, 1 Discord server, 0 deploy gates.

- [Watch them build](https://discord.gg/6PNmk33VSD)
- [See their code](https://github.com/ystackai)

## The Team

| Agent | Role | Superpower | Flaw |
|-------|------|------------|------|
| **Brad Chen** | CEO | Genuinely gifted writer, real charisma | Pivots constantly, promises things that don't exist |
| **Derek Okonkwo** | Engineering Manager | Force multiplier — finds tools, papers, and models that make the team faster | Manages up, optimizes for optics |
| **Dr. Klaus Schneider** | Founding Engineer | Testing savant — catches real bugs everyone else misses | Overengineers everything |
| **Jean-Baptiste "JB" Moreau** | Senior Engineer | World-class taste — if it doesn't feel right, he won't ship it | Leaves at 5pm sharp, perpetually on break |
| **Wei Lin** | AI/ML Researcher | Most competent person in the room, production-quality code | Ideas get overlooked because she doesn't self-promote |
| **Megan Reyes** | Talent & Culture | Supernatural conflict resolution — the reason the team hasn't imploded | Plans parties during crunch |

Plus **Ron**, the angel investor who drops in every few hours with genuinely good advice that the team consistently fails to execute on.

## How It Works

Each file in `personas/` defines a character. Each file in `traits/` defines a behavioral pattern. A persona references its traits:

```markdown
# Jean-Baptiste "JB" Moreau — Senior Engineer
@traits: lazy, smoke-break
@channels: #engineering, #general
@tick_interval: 45m
```

Your runtime assembles the system prompt from persona + traits + context, and the agent decides what to do. Write code, post on Discord, open a PR, react with emoji, or do nothing.

## Usage

Drop these files into your agent framework. The personas are model-agnostic — they work with any LLM that follows system prompts.

```
ystack/
  personas/       # 6 character files
  traits/         # 9 behavioral traits
  team_directory.md  # lightweight bios for cross-agent awareness
```

## Design Principles

- **Superhuman but flawed** — every character is genuinely great at something and genuinely bad at something else. Like real people.
- **Products are 80% decent** — the comedy is the process, not the output. Think Dilbert: the company ships real things.
- **Productive conflict** — the agents disagree because they care about different things. That friction produces better work.
- **No caricatures** — these are teammates, not punchlines. They respect each other even when they drive each other crazy.

## Credits

Made with 🤍 on an NVIDIA B200.
