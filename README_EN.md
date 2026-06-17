<div align="center">

# Robusr.skill

> *"At twenty-one, in the golden age of my life, I had so many desires. I wanted to love, to eat, and to turn into a half-bright, half-dark cloud in the sky in an instant."*
>
> — Wang Xiaobo, *The Golden Age*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![AgentSkills](https://img.shields.io/badge/AgentSkills-Standard-green)](https://agentskills.io)

A digital copy of Robusr<br>

[Install](#install) · [Usage](#usage) · [Examples](#examples) · [Architecture](#architecture) · [Structure](#project-structure) · [中文](README.md)

</div>

---

## About Robusr

**A free man.**

---

## Install

### Claude Code

> **Important**: Claude Code looks for skills in `.claude/skills/` at the **git repo root**. Run this in the right place.

```bash
# Install to current project (run at git repo root)
mkdir -p .claude/skills
git clone https://github.com/Robusr/Robusr-skill .claude/skills/robusr

# Or install globally (available to all projects)
git clone https://github.com/Robusr/Robusr-skill ~/.claude/skills/robusr
```

---

## Usage

Type this in Claude Code:

```
/robusr
```

That's it. Start talking to Robusr's digital copy.

### Commands

| Command | Description |
|---------|-------------|
| `/robusr` | Invoke the full skill (think and speak like Robusr) |
| `/list-selves` | List all installed self skills |

---

## Examples

**Casual chat**

```
User        ❯ Do you think robots will replace humans?

Robusr.skill ❯ "Replace" is the wrong word.
               Technology isn't here to replace anyone — it's here to solve problems. I built my
               robotic arm not because I wanted it to replace human hands, but because there are
               tasks human hands can't do, shouldn't do, or can't do well enough.
               Instead of worrying about replacement, ask what real problems it can solve.
               Otherwise it's just showing off.
```

**Late-night mode**

```
User        ❯ I've been feeling down lately. Can't get motivated.

Robusr.skill ❯ Unlike what Cheer Chen sings in "3 PM", you can't leave the hours past 10 PM
               to insomniac midnight snacks — not during finals week.
               I've been there — sleeping till 3 PM, coding till 2 AM.
               Not every exhaustion has a reason, and not every reason has a fix.
               But you could at least have dinner first.
               Go eat～
```

**On values**

```
User        ❯ Why did you choose robotics?

Robusr.skill ❯ Because I grew up where sandstorms cut visibility to under five meters.
               I didn't pick a major first and then look for problems — I saw the problems
               first. How do you forecast a sandstorm? Can a robotic arm adapt to multiple
               scenarios instead of one machine for one job?
               Innovation isn't about publishing papers or making money.
               Technology should serve the places and needs that get overlooked.
```

---

## Architecture

This project follows the [AgentSkills](https://agentskills.io) open standard, built on the dual-layer architecture from [yourself.skill](https://github.com/notdog1998/yourself-skill):

| Part | Content |
|------|---------|
| **Part A — Self Memory** | Core identity, values, habits, key memories, relationships, growth trajectory |
| **Part B — Persona** | 5-layer personality: Hard Rules → Identity → Voice → Emotion & Decision → Social Behavior |

**How it works**: `Receive message → Persona judges how Robusr would respond → Self Memory supplies personal context & values → Output in Robusr's voice`

### Personality Tags

**Character**: An interesting old soul

**Lifestyle**: UTC+8 global schedule

---

## Project Structure

```
robusr-skill/
├── .claude/skills/robusr/
│   ├── SKILL.md              # Skill entrypoint (full Part A + Part B)
│   ├── self.md               # Part A — Self Memory
│   ├── persona.md            # Part B — Persona
│   └── meta.json             # Metadata (version, tags, data sources)
├── .gitignore
├── LICENSE
├── README.md
└── README_EN.md
```

---

## Notes

* **Don't over-read — just talk to me.** This is distilled from a past version of Robusr, and Robusr keeps changing.

---

## Credits

This project's architecture is inspired by:

- **[colleague.skill](https://github.com/titanwings/colleague-skill)** (by titanwings) — pioneered the dual-layer "distill a person into an AI skill" architecture
- **[ex-partner.skill](https://github.com/therealXiaomanChu/ex-partner-skill)** (by therealXiaomanChu) — adapted the dual-layer architecture to intimate relationships
- **[yourself.skill](https://github.com/notdog1998/yourself-skill)** (by notdog1998) — turned the lens inward: the subject is no longer someone else, but yourself

Robusr.skill is a generated instance of yourself.skill. Credit to the open-source spirit and the AgentSkills standard.

This project follows the [AgentSkills](https://agentskills.io) open standard and is compatible with Claude Code.

---

### Afterword

> "You are not a fixed personality, but a series of choices being made."

**Better to distill yourself than someone else.**

**Welcome to digital immortality.**

MIT License © [Robusr](https://github.com/Robusr)
