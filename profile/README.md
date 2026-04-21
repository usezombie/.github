<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-light.svg" />
  <img src="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-dark.svg" width="200" alt="usezombie" />
</picture>

**Ship agents that touch real infrastructure.**

**Open-source agent runtime · Credential firewall · Audit every action · Kill switch**

[![Try Free](https://img.shields.io/badge/UseZombie-Try_Free-brightgreen?style=for-the-badge)](https://usezombie.com)
[![Docs](https://img.shields.io/badge/UseZombie-Docs-blue?style=for-the-badge)](https://docs.usezombie.com)

</div>

---

## The problem

You have a working agent. It can reply to emails, fix bugs, process payments, review PRs. But you won't let it run unsupervised because it holds your API keys, leaves no record of what it did, has no spend ceiling, and no kill switch. So you babysit it. Or you don't run it at all.

## What Zombies are

A **Zombie** is a long-running agent that operates against real infrastructure — your clusters, servers, codebases — without ever holding a real credential. Invoke it yourself, let another agent call it, or wire it into CI. Same guarantees.

| Zombie | What it does |
|---|---|
| **Homelab Zombie** | Diagnose your k3s cluster at 2am without cluster-admin. |
| **Homebox Audit** | Quarterly security + freshness audit of your self-hosted stack. |
| **Side-project Resurrector** | Revive dormant repos, open a PR with fresh deps and CI. |
| **Migration Zombie** | Mechanical code migrations (Jest→Vitest, Node bumps) via playbooks. |

You don't code a Zombie. 

> You write a skill spec in markdown — policy, allowed verbs, required credentials — and the runtime handles sandboxing, credential injection, audit logging, and approval gates.

Need a Zombie we don't ship yet? [Open an issue](https://github.com/usezombie/usezombie/issues).

## Get started

Follow the [quickstart guide →](https://docs.usezombie.com)

## Repositories

| Repo | What it is |
|---|---|
| [usezombie/usezombie](https://github.com/usezombie/usezombie) | Control plane + worker + CLI. Zig `zombied`, Node/Bun `zombiectl`, NullClaw agent runtime, Next.js dashboard. |
| [usezombie/docs](https://github.com/usezombie/docs) | User-facing documentation ([docs.usezombie.com](https://docs.usezombie.com)) — quickstart, API reference, operator guides, changelog. |
| [usezombie/posthog-zig](https://github.com/usezombie/posthog-zig) | PostHog SDK for Zig. Powers signup funnel, zombie lifecycle, and billing telemetry inside `zombied`. Usable standalone. |

