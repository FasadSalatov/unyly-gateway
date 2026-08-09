# Unyly Gateway

**One MCP connector for the whole catalog — 80,000+ servers plus your team's private MCPs — from any AI client.**

[![Website](https://img.shields.io/badge/website-unyly.org-e5199a)](https://unyly.org)
[![Smithery](https://img.shields.io/badge/Smithery-unyly%2Fgateway-orange)](https://smithery.ai/servers/unyly/gateway)
[![MCP Registry](https://img.shields.io/badge/MCP%20Registry-org.unyly%2Fgateway-blue)](https://registry.modelcontextprotocol.io)

Unyly Gateway is a remote [Model Context Protocol](https://modelcontextprotocol.io) server that exposes the entire Unyly catalog through a **single connection**. Instead of installing MCP servers one by one — editing JSON, wrangling Node/Python, restarting your client — you connect the gateway once and reach any server in the catalog, plus your team's private ones.

It works in **Claude** (web & desktop), **ChatGPT**, **Cursor**, **VS Code**, **Claude Code**, **Windsurf** and any MCP-capable client. Auth is OAuth 2.1 (dynamic client registration + PKCE) — no per-server tokens pasted into chats.

## Connect

Add this remote MCP server to your client:

```
https://gateway.unyly.org/mcp
```

That's it. Complete the OAuth prompt and you're connected — no packages, no JSON, no per-server install.

## How it works

The gateway exposes three meta-tools. Servers you or your team pin are also exposed directly as `<slug>__<tool>`.

| Tool | What it does |
|------|--------------|
| `search_mcps` | Find a server in the 80,000+ catalog by task, name or category |
| `list_mcp_tools` | Inspect a server's tools before calling |
| `use_mcp_tool` | Call any tool on any server in the catalog |

The AI searches for the capability it needs, inspects the server, and calls the tool — all through one connection. Calls are metered against a prepaid team balance; going negative is impossible.

## Why a gateway instead of per-server installs

- **One connection, whole catalog** — 80,000+ servers reachable without installing any of them locally.
- **Works where local servers can't** — ChatGPT, claude.ai and mobile clients can't spawn a local process; a remote gateway works everywhere.
- **Team-ready** — shared allow-lists, per-member spend caps, a log of every call, private company servers hidden from the public catalog.
- **No secrets in chat** — OAuth sign-in, tokens revoked in one click, role-based access.

## Links

- **Website & catalog:** https://unyly.org
- **Browse servers:** https://unyly.org/browse
- **Smithery listing:** https://smithery.ai/servers/unyly/gateway
- **Official MCP Registry:** `org.unyly/gateway`
- **Docs:** https://unyly.org/gateway

---

This repository is a connect guide and documentation for the hosted Unyly Gateway. The gateway itself runs at `gateway.unyly.org` — there's nothing to build or install here.
