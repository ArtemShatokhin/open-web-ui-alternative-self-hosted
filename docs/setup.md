# Self-hosting Kortix — setup

Kortix is the open-source AI Operating System. One Docker Compose stack, on your own box, with the whole configuration in a git repo.

## 1 · Install the CLI

```bash
curl -fsSL https://kortix.com/install | bash
```

## 2 · Scaffold the project

```bash
kortix init
```

This writes `kortix.yaml` and your `agents/` and `skills/` directories. Every agent and skill is a markdown file; the connectors and triggers are declared in `kortix.yaml`.

## 3 · Start it on your own infrastructure

```bash
kortix self-host start
```

One Docker Compose stack comes up. Sessions boot their own isolated Linux sandbox with the repo and tools already on it — nothing to install on the host, and no laptop involved.

## 4 · Wire your tools and models

- **Connectors:** Slack, docs, tickets, CRM, billing and code, once, then scope which agent may touch which. 3,000+ apps plus MCP, OpenAPI, GraphQL and raw HTTP. Credentials are brokered server-side and never enter the machine.
- **Models:** any provider with your own keys, chosen per agent, per session or per message — or your own OpenAI-compatible endpoint.
- **Rules:** set each tool to allow, ask or block, down to the arguments of a call. An **Ask** holds the call until a person approves it.

## 5 · Run it

```bash
kortix sessions new --prompt "Triage today's tickets and open a change request with the drafts"
kortix cr ls
kortix chat
```

Work lands on the default branch only through a change request you read as a diff first.

## Where this fits next to Open WebUI

Keep Open WebUI as your chat and RAG surface if you like it; run Kortix for the agents that act. The comparison is in [kortix-vs-open-webui.md](kortix-vs-open-webui.md).
