<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-light.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-dark.svg" />
  <img src="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-dark.svg" width="200" alt="usezombie" />
</picture>

**Heroku for agents, but the agent never sees your keys.**

Run your agents 24/7. Walled, watched, killable.

[![Try Free](https://img.shields.io/badge/UseZombie-Try_Free-brightgreen?style=for-the-badge)](https://usezombie.com)
[![Docs](https://img.shields.io/badge/UseZombie-Docs-blue?style=for-the-badge)](https://docs.usezombie.com)

</div>

---

## Why we pivoted

We started by obsessing over one thing: making AI-generated code *correct*. Self-repair loops, quality scoring, scorecard evidence. Good problems — but narrow ones. Frontier models get better every quarter, and the gap we were optimizing for keeps shrinking on its own.

The tempting move is to double down — we built it, so we stick with it. But code is cattle, not pets. You don't keep a solution alive just because you wrote it.

```
          ____________________________
         < code(human) === cattle now >
          ----------------------------
                 \   ^__^
                  \  (oo)\_______
                     (__)\       )\/\
                         ||----w |
                         ||     ||
```

So we killed the old approach and pivoted. UseZombie is now a runtime for always-on agents — you bring your agent, we handle the credentials (hidden from the sandbox, injected at the firewall), webhooks (wired automatically), audit logs (every action timestamped), and a kill switch. Your agent runs 24/7 without ever seeing a password.

## What zombies do

- **Always-on agents** — your agent runs continuously in a sandboxed process, restarts on crash
- **Credentials hidden** — agents never see tokens; the firewall injects them per-request, outside the sandbox boundary
- **Webhooks wired** — receive events from email, Slack, GitHub, etc. without ngrok or custom servers
- **Observability** — see what your agent did, when, why, and how much it cost — before the invoice surprises you
- **Spend ceiling** — per-run token budgets and wall time limits; one bad prompt never becomes an infinite burn
- **Kill switch** — stop any agent mid-action from the CLI or web UI

## Projects

- [usezombie/usezombie](https://github.com/usezombie/usezombie) — core platform
- [usezombie/posthog-zig](https://github.com/usezombie/posthog-zig) — PostHog client for Zig
- [usezombie/docs](https://github.com/usezombie/docs) — documentation

## Links

- [usezombie.com](https://usezombie.com)
- [docs.usezombie.com](https://docs.usezombie.com)
- [All repositories](https://github.com/usezombie?tab=repositories)
