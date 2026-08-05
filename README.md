# Slant — agent plugin

Claude Code plugin for [Slant](https://slant.page), the collaborative AI writing
editor. Lets any agent publish local markdown as a shareable, editable Slant doc
and collaborate on shared documents (comments, suggestions, edits, live presence).

## Install

```
/plugin marketplace add hemaaanth/slant-plugin
/plugin install slant
```

Or without the plugin system:

```bash
mkdir -p ~/.claude/skills/slant && curl -fsSL https://slant.page/SKILL.md -o ~/.claude/skills/slant/SKILL.md
```

More setup options (MCP server, other clients): https://slant.page/agents

## Do not edit this repo by hand

This repo is generated from the Slant app repo. The skill in `skills/slant/` and
the version in `.claude-plugin/plugin.json` are rendered from the canonical
source (`src/lib/skill-md.ts`) by CI on every release — the served
https://slant.page/SKILL.md and this repo are always the same content. Changes
made here will be overwritten by the next sync.
