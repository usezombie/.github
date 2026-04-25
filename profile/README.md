<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-light.svg" />
  <img src="https://raw.githubusercontent.com/usezombie/usezombie/main/assets/logo-dark.svg" width="200" alt="usezombie" />
</picture>

**A markdown-defined, durable, BYOK zombie that owns one operational outcome — wakes on a GitHub Actions deploy failure, gathers evidence, posts a diagnosis to your Slack.**

**Open source. Bring your own LLM key. The zombie keeps state across attempts, requests approval for risky actions, and stays on the outcome until it's resolved or explicitly blocked.**

[![Try Free](https://img.shields.io/badge/UseZombie-Try_Free-brightgreen?style=for-the-badge)](https://usezombie.com)
[![Docs](https://img.shields.io/badge/UseZombie-Docs-blue?style=for-the-badge)](https://docs.usezombie.com)

</div>

---

## The problem

A deploy fails at 2am. Your CD pipeline goes red. Now you're bouncing between five tools while holding the timeline in your head: GitHub Actions for the run logs, Grafana for the metrics, your observability dashboard for the traces, Slack for the alerts, your terminal for `kubectl` and `flyctl`. You correlate, you guess, you restart something with no clear root cause, and the next morning you can't reconstruct what you did.

The work is fragmented. State is lost between attempts. There is no durable memory across incidents.

## What v2 ships

A **Zombie** is a long-lived runtime that owns one operational outcome end-to-end. The v2 wedge ships one zombie: **`platform-ops`**.

| Trigger | What happens |
|---|---|
| GitHub Actions `workflow_run.conclusion=failure` webhook | Zombie wakes, fetches the failed run logs via the GH API, correlates against your hosting provider's logs and your data-plane health, posts an evidenced diagnosis to your Slack channel. |
| `zombiectl steer {id} "morning health check"` | Same zombie, operator-initiated. Same reasoning loop, different `actor=` on the event. |

You don't code a Zombie. You write a `SKILL.md` in plain English (how to think, what evidence to gather, when to ask for approval) and a `TRIGGER.md` declaring tools, credentials, network allowlist, budget caps. The runtime handles sandboxing (Landlock + cgroups + bwrap), credential injection at the tool bridge, durable event history, and budget enforcement.

Install with `/usezombie-install-platform-ops` in any agent host (Claude Code, Amp, Codex CLI, OpenCode). Same slash-command everywhere.

## Differentiation (v2)

Three structural pillars: **OSS** (read the code that holds your credentials), **BYOK** (your LLM provider key, your inference cost), **markdown-defined** (configuration in prose, not typed control flow). Self-host arrives in v3.

## Get started

Follow the [quickstart guide →](https://docs.usezombie.com)

## Repositories

| Repo | What it is |
|---|---|
| [usezombie/usezombie](https://github.com/usezombie/usezombie) | Control plane + worker + CLI. Zig `zombied`, Node/Bun `zombiectl`, NullClaw agent runtime, Next.js dashboard. |
| [usezombie/docs](https://github.com/usezombie/docs) | User-facing documentation ([docs.usezombie.com](https://docs.usezombie.com)) — quickstart, API reference, operator guides, changelog. |
| [usezombie/posthog-zig](https://github.com/usezombie/posthog-zig) | PostHog SDK for Zig. Powers signup funnel, zombie lifecycle, and billing telemetry inside `zombied`. Usable standalone. |

