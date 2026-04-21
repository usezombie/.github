<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-light.svg" />
  <img src="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-dark.svg" width="200" alt="usezombie" />
</picture>

**Your agent is ready. You're not ready to trust it. We fix that.**

**Run your agents 24/7. Credentials hidden. Every action logged. Big moves approved.**

[![Try Free](https://img.shields.io/badge/UseZombie-Try_Free-brightgreen?style=for-the-badge)](https://usezombie.com)
[![Docs](https://img.shields.io/badge/UseZombie-Docs-blue?style=for-the-badge)](https://docs.usezombie.com)

</div>

---

## The problem

You have a working agent. It can reply to emails, fix bugs, process payments, review PRs. But you won't let it run unsupervised because:

- It has your API keys (what if it goes rogue?)
- You can't see what it did (what if the CEO asks?)
- There's no spend ceiling (what if one bad prompt burns $500?)
- There's no kill switch (what if it starts replying to every email in your inbox?)

So you babysit it. Or you don't run it at all.

## What Zombies are

A **Zombie** is a preconfigured agent workflow that does one job and runs forever.

```
"Install the Lead Zombie"       → handles inbound email, replies, logs leads
"Install the Slack Bug Fixer"   → monitors #bugs, opens PRs, replies in thread
"Install the PR Zombie"         → reviews every PR, posts feedback, alerts on critical
"Install the Ops Zombie"        → watches infra, alerts on incidents
"Install the Hiring Zombie"     → receives candidate profile (resume PDF, GitHub PRs,
                                   Gmail), analyzes attachments for merit, sends you
                                   a decision report on Discord
```

You don't code a Zombie. You configure it: what tools it attaches, what credentials it uses, what budget it has, what triggers it. The agent intelligence is built in.

## How it works

- **Sandboxed runtime** — bwrap + landlock isolation. Network deny-by-default.
- **Credentials hidden** — vault injects at the sandbox boundary. The agent never sees API keys.
- **Webhooks wired** — receive events from email, Slack, GitHub. No ngrok needed.
- **Activity stream** — every action timestamped. `zombiectl logs` shows what happened and why.
- **Spend ceiling** — per-day and per-month dollar budgets. One bad prompt never becomes an infinite burn.
- **Kill switch** — `zombiectl kill` stops any agent mid-action. Checkpoint saved, no data lost.
- **Crash recovery** — state checkpointed after every event. Crashes recover automatically.

## Get started

```bash
npm install -g zombiectl
zombiectl login
zombiectl install lead-collector
zombiectl up
```

[Read the docs →](https://docs.usezombie.com)

## Repositories

| Repo | What it is |
|------|------------|
| [usezombie/usezombie](https://github.com/usezombie/usezombie) | Control plane + worker + CLI. Zig `zombied` server, Node/Bun `zombiectl`, NullClaw agent runtime, and the Next.js dashboard. Where every behavior you see above is implemented. |
| [usezombie/docs](https://github.com/usezombie/docs) | User-facing documentation site ([docs.usezombie.com](https://docs.usezombie.com)) — quickstart, API reference, operator guides, changelog. |
| [usezombie/posthog-zig](https://github.com/usezombie/posthog-zig) | PostHog SDK for Zig. Powers the signup funnel, zombie lifecycle, and billing telemetry inside the `zombied` control plane. Usable standalone. |

