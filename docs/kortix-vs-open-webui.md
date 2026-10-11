# Kortix vs Open WebUI

Both are open source and both can run fully on your own infrastructure. They solve different halves of the problem.

**Open WebUI** is a self-hosted AI *interface*. It gives you a polished chat and workspace over local and cloud models — Ollama, any OpenAI-compatible API, RAG over your documents, user groups and RBAC, plugins, web search. It is the best-in-class place to *talk* to models and query your knowledge.

**Kortix** is the open-source AI Operating System. It runs *agents* that take real actions and return finished work — a report, a fix, a reply, a deployed change — each on its own isolated cloud computer, each landing through a change request a person reviews.

## Where they differ

| Dimension | Open WebUI | Kortix |
|---|---|---|
| Primary output | Answers in a chat | Finished work: reports, code, replies, deployed changes |
| Where an agent runs | The host running the UI | A disposable cloud computer per session, on its own branch |
| Peers and parallelism | One server | Thousands of isolated sandboxes on one config |
| Configuration | App database | Files in one git repo you own |
| Governance | RBAC and user groups | Per-tool allow / ask / block, approval gates, audit trail, SSO/SCIM, your VPC |
| Tool reach | RAG, web search, plugins | 3,000+ apps plus MCP, OpenAPI, GraphQL, raw HTTP; brokered credentials |
| Review before it lands | n/a | Every change is a change request you merge |

## When to pick which

- Pick **Open WebUI** when you need a self-hosted chat and RAG surface over your models. It is very good at that.
- Pick **Kortix** when you need agents that act in your tools and land work through review — with the configuration, memory and permissions in a repo you own.

Many teams run both: Open WebUI for reading and asking, Kortix for doing.

See also: [Best Open WebUI alternatives](https://openwebuialternative.com/best-open-webui-alternatives).
