# Open WebUI for teams — where the install stops and an agent system starts

Kortix is the open-source AI Operating System. An Open WebUI install that started as one person's local chat tends to hit the same wall: it is serving a team, but it is still a chat window. The questions change.

## Three questions a team asks

1. **"The agent should do it, not just describe it."** Chat returns an answer. The work — triaging tickets, updating the CRM, opening a fix — is still manual. That is an agent job, not a chat job.
2. **"Who approved this?"** When an agent can send an email or spend money, the team needs a gate and a record. Kortix declares per-tool allow / ask / block rules in the repo, holds a call on **Ask** until a person approves, and lands every change as a reviewed change request.
3. **"Whose context is it?"** A single chat store mixes everyone. Kortix keeps the company memory as files in a repo, and each session runs on its own isolated machine on its own branch.

## A team setup

- Agents and skills: files in one repo, versioned and diffable.
- Connectors: wired once, scoped per agent; credentials brokered server-side.
- Sessions: one isolated cloud computer each, thousands in parallel on one config.
- Landing: change requests a person reads as a diff before merge.

## Start

```bash
curl -fsSL https://kortix.com/install | bash
kortix init
kortix ship
```

More at [Open WebUI for teams](https://openwebuialternative.com/open-web-ui-for-teams) and [self-hosting notes](https://openwebuialternative.com/self-hosting).
