<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-light.svg" />
  <img src="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-dark.svg" width="200" alt="usezombie" />
</picture>

**Ship agents that touch real infrastructure. Without handing over the keys.**

**Open-source agent runtime · Credential firewall · Audit every action · Kill switch**

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

A **Zombie** is a long-running agent that operates against real infrastructure — your clusters, your servers, your codebases — without ever holding a real credential.

```
"Homelab Zombie"              → diagnose your k3s cluster at 2am without cluster-admin
"Migration Zombie"            → mechanical code migrations (Jest→Vitest, Node bumps) via playbooks
"Side-project Resurrector"    → revive dormant repos, open a PR with fresh deps and CI
"Homebox Audit"               → quarterly security + freshness audit of your self-hosted stack
```

You don't code a Zombie. You write a skill spec in markdown — policy, allowed verbs, required credentials — and the runtime handles sandboxing, credential injection, audit logging, and approval gates. Need a skill we don't ship yet? [Open an issue](https://github.com/usezombie/usezombie/issues).

## Get started

Follow the [quickstart guide →](https://docs.usezombie.com)

## Repositories

| Repo | What it is |
|------|------------|
| [usezombie/usezombie](https://github.com/usezombie/usezombie) | Control plane + worker + CLI. Zig `zombied` server, Node/Bun `zombiectl`, NullClaw agent runtime, and the Next.js dashboard. Where every behavior you see above is implemented. |
| [usezombie/docs](https://github.com/usezombie/docs) | User-facing documentation site ([docs.usezombie.com](https://docs.usezombie.com)) — quickstart, API reference, operator guides, changelog. |
| [usezombie/posthog-zig](https://github.com/usezombie/posthog-zig) | PostHog SDK for Zig. Powers the signup funnel, zombie lifecycle, and billing telemetry inside the `zombied` control plane. Usable standalone. |

