# Zia Tutor AI

A Claude Code plugin that bundles the **Zia Tutor AI** skill with its MCP connector, so one install gives Claude both the teaching instructions and the server they depend on.

- `skills/zia-tutor-ai/` is the skill. It triggers when someone wants to learn, review or get unstuck on The AI Agent Factory, agentic AI, agents, MCP or Digital FTEs.
- `.mcp.json` adds the `agentfactory-tutor` HTTP server at `https://zia-tutor-ai.panaversity.org/mcp`. It authorizes with OAuth (client `zia-tutor-ai`, callback port 3118).

## Install

At the prompt of a Claude Code terminal session:

```
/plugin install zia-tutor-ai --marketplace panaversity/zia-tutor-ai-plugin
```

Answer `y` to add the marketplace, then press Enter to pick the user scope.

From a shell:

```
claude plugin install zia-tutor-ai --marketplace panaversity/zia-tutor-ai-plugin
```

In the desktop app: click + next to the prompt box, then Plugins, Add marketplace with `panaversity/zia-tutor-ai-plugin`, then Add plugin.

## Setup

After installing, run `/mcp`, pick `agentfactory-tutor` and authorize it once in the browser. Until the connector is authorized, the skill will not teach the material.

## Try it from this folder

```
claude --plugin-dir ./zia-tutor-ai-plugin
```
