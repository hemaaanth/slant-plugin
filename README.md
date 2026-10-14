# Slant — agent plugin

Claude Code plugin for [Slant](https://slant.page), the collaborative AI writing
editor. Lets any agent publish local markdown as a shareable, editable Slant doc
and collaborate on shared documents (comments, suggestions, edits, live presence).

## Install

```
/plugin install slant --marketplace hemaaanth/slant-plugin
```

On Claude Code before 2.1.275, add the marketplace first:
`/plugin marketplace add hemaaanth/slant-plugin`, then `/plugin install slant`.

The plugin installs the skill and the Slant MCP server
(`https://slant.page/api/mcp`). The first time a tool runs, you sign in once in
the browser and pick the workspace and permission.

Or without the plugin system:

```bash
mkdir -p ~/.claude/skills/slant && curl -fsSL https://slant.page/SKILL.md -o ~/.claude/skills/slant/SKILL.md
```

More setup options (other clients, tokens): https://slant.page/agents

## Do not edit this repo by hand

This repo is generated from the Slant app repo. The skill in `skills/slant/` and
the version in `.claude-plugin/plugin.json` are rendered from the canonical
source (`src/lib/skill-md.ts`) by CI after every green build of `master` — the served
https://slant.page/SKILL.md and this repo are always the same content. Changes
made here will be overwritten by the next sync.
