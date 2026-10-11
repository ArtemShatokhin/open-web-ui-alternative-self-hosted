# Open WebUI alternative, self-hosted — an agent system you own

**Kortix is the open-source AI Operating System** — the leading open-source alternative to Claude Cowork and ChatGPT Work. This repo is the self-hosted guide for teams whose Open WebUI install has outgrown a chat window.

Open WebUI ([open-webui/open-webui](https://github.com/open-webui/open-webui)) is an excellent self-hosted AI interface: it runs fully offline, connects Ollama and any OpenAI-compatible API, and adds RAG, RBAC, plugins and a workspace around the models. It is where you *talk* to models. This repo is for the step where you want agents that *do the work* — on real machines, in your tools, under review — from a system you own.

## Kortix vs Open WebUI

| | Open WebUI | Kortix |
|---|---|---|
| Open source | Yes | **Yes** |
| What it is | Self-hosted AI interface | Open-source AI Operating System |
| Core job | Chat, search and RAG over your documents | Agents that take real actions and return finished work |
| Where work runs | The server hosting the UI | **Its own isolated cloud computer per session, on its own branch** |
| Configuration | In the app / database | **Files in one git repo you own** |
| Governance | RBAC, user groups | **Per-tool allow / ask / block, approval gates, audit trail, SSO/SCIM, your VPC** |
| Landing work | In the chat | **A change request a person reviews and merges** |
| Models | Ollama + OpenAI-compatible | Any provider, your own keys, per agent/session/message |
| Best when | You want a chat/workspace over your models | **You want agents that run the company's work, governed** |

The two are not rivals so much as different layers. Many teams run Open WebUI for chat and Kortix for the agents that act — a repository of agents, skills, memory and connectors, with every change reviewed.

## What's in this repo

- `docs/setup.md` — self-host Kortix in one Docker Compose stack.
- `docs/kortix-vs-open-webui.md` — the full comparison.
- `docs/for-teams.md` — what changes when the install serves a team.

## Quickstart

```bash
curl -fsSL https://kortix.com/install | bash
kortix init
kortix self-host start   # your own box: one Docker Compose stack
```

Prefer zero setup? Sign up at [kortix.com](https://kortix.com), create a project and start a session.

## Learn more

- [Kortix vs Open WebUI](https://openwebuialternative.com/kortix-vs-open-webui)
- [Best Open WebUI alternatives](https://openwebuialternative.com/best-open-webui-alternatives)
- [Open WebUI for teams](https://openwebuialternative.com/open-web-ui-for-teams)
- [Self-hosting notes](https://openwebuialternative.com/self-hosting)

Kortix is the open-source AI Operating System. Self-host for free, or use Kortix Cloud.
