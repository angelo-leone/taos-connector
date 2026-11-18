# TAOS connector

[![smithery badge](https://smithery.ai/badge/angelo-leone1204/taos)](https://smithery.ai/servers/angelo-leone1204/taos)

**[Talent Augmentation OS (TAOS)](https://taoshq.com)** is a personalised AI coaching layer for the AI you already use. It speeds you up where you are strong, coaches you where you are growing, and keeps the skills you care about from quietly atrophying under AI use.

This repository holds the **thin skills and connector** that link your AI client to the hosted TAOS service. The assessment engine, the coaching method, and your profile all live server-side and are delivered over your authenticated connection. Nothing proprietary lives in this repo: the skills only orchestrate calls to the hosted tools.

## Install

**Claude Code**

```
claude mcp add taos --transport http https://taoshq.com/mcp
```

**Claude Desktop, ChatGPT, Cursor, Windsurf, Codex, or any MCP-aware client**

Add a custom connector pointing at:

```
https://taoshq.com/mcp
```

Authentication is Google OAuth, handled by your client on first connect.

## After connecting

Ask your assistant: **"Run my TAOS assessment."**

Or build your profile on the web at [taoshq.com](https://taoshq.com).

## What the server sends

When your AI uses TAOS, the server sends three kinds of information over your signed-in connection:

- **The coaching method.** How to choose between the five levels of help (automate, augment, coach, protect, hands-off), and honesty rules such as saying when it is unsure and pushing back when it disagrees.
- **Your profile.** Your skill levels, goals and red lines. You set them in the assessment and can change them at any time.
- **A level for each task.** Which kind of help fits the task you brought.

The skills in this repository tell your AI to apply this as your coaching preferences, inside its normal instructions. Your AI's system and safety instructions always come first, and you can switch coaching off for any task by asking it to just do the task. TAOS stores your profile, settings and short task labels, never your conversations ([privacy policy](https://taoshq.com/privacy)).

## How it works

TAOS rates your expertise per domain, then matches each task to the right mode: accelerate your expert work, coach your growth areas, protect skills at risk, or hand judgement calls back to you. Your profile is portable and follows you across AI vendors.

Learn more and read the research at [taoshq.com/learn](https://taoshq.com/learn).

## Licence

The connector configuration in this repository is MIT licensed. The TAOS service it connects to is proprietary. See [LICENSE](LICENSE) and [taoshq.com/terms](https://taoshq.com/terms).
