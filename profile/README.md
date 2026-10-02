# agentsec-ecosystem

**Open-source, harness-agnostic security for AI agents.**

AI coding agents and MCP clients now hold shell access, filesystem access, credentials, and tool
integrations — and today's tooling rarely lets a security team *see*, *stop*, or *undo* what an
agent does. We're building the missing layer: one coherent, Apache-2.0 ecosystem that gives any
harness the four capabilities that matter.

| Capability | What it means |
|---|---|
| **Monitor** | Structured, OpenTelemetry-compatible telemetry for every agent tool call |
| **Alert** | Policy-driven detection of risky behavior, in real time |
| **Block / limit** | Allow / deny / ask / rate-limit / redact enforcement |
| **Revoke** | Credential brokering and one-action revocation |

## The stack

| Tool | Role | Status |
|---|---|---|
| [agentwatch](https://github.com/agentsec-ecosystem/agentwatch) | OTel GenAI telemetry + security-event schema | planned |
| [agentpolicy](https://github.com/agentsec-ecosystem/agentpolicy) | Cedar PDP: allow/deny/ask/rate-limit/redact | planned |
| [agentgate](https://github.com/agentsec-ecosystem/agentgate) | MCP OAuth 2.1 authorization proxy | planned |
| [agentkeys](https://github.com/agentsec-ecosystem/agentkeys) | Never-in-context credential broker + revocation | planned |
| [agentseatbelt](https://github.com/agentsec-ecosystem/agentseatbelt) | Portable local enforcement, macOS-first | planned |
| [agentkernel](https://github.com/agentsec-ecosystem/agentkernel) | Linux eBPF visibility + enforcement | planned |
| [agenthalt](https://github.com/agentsec-ecosystem/agenthalt) | Universal kill-switch + evidence preservation | planned |
| [policyweave](https://github.com/agentsec-ecosystem/policyweave) | One Cedar policy → every harness format | planned |
| [agentdrill](https://github.com/agentsec-ecosystem/agentdrill) | Attack packs in CI vs. deployed policies | planned |
| [agentcomply](https://github.com/agentsec-ecosystem/agentcomply) | SOC 2 / ISO 42001 evidence automation | planned |
| [agentinbox](https://github.com/agentsec-ecosystem/agentinbox) | Ask-gate consumer (Slack/terminal/CI/mobile) | planned |
| [agentdiff](https://github.com/agentsec-ecosystem/agentdiff) | Dry-run "would-have-blocked" conversion | planned |

> Status reflects reality. Each repo is published as it becomes usable, not before.

## Superseded repositories

Earlier prototypes have been folded into the stack above and **archived** (read-only, not deleted).
They remain available for history and incoming links, but all future work happens in the successor
repositories.

| Archived (superseded) | Replaced by |
|---|---|
| [mcplex](https://github.com/agentsec-ecosystem/mcplex) | [agentkeys](https://github.com/agentsec-ecosystem/agentkeys) |
| [agent-exec-trace](https://github.com/agentsec-ecosystem/agent-exec-trace) | [agentwatch](https://github.com/agentsec-ecosystem/agentwatch) |
| [agent-tooltrust](https://github.com/agentsec-ecosystem/agent-tooltrust) | [agentpolicy](https://github.com/agentsec-ecosystem/agentpolicy) / [agentgate](https://github.com/agentsec-ecosystem/agentgate) |
| [ai-loopguard](https://github.com/agentsec-ecosystem/ai-loopguard) | [agenthalt](https://github.com/agentsec-ecosystem/agenthalt) |
| [agent-eval-forge](https://github.com/agentsec-ecosystem/agent-eval-forge) | [agentdrill](https://github.com/agentsec-ecosystem/agentdrill) |

## Principles

- **Harness-agnostic** — Tier 1 coding agents, agent frameworks, and generic MCP clients.
- **Adopt, don't rebuild** — we build on existing OSS (LiteLLM, agent-scan, sandbox-runtime, Cedar, eBPF tooling).
- **No ML in enforcement paths** — deterministic, auditable policy decisions.
- **No paywalled enforcement, no proprietary formats** — Apache-2.0, open schema, portable policy.
- **Honest results** — a public benchmark, including what we miss.

## Get started

One command installs the Wave 0 stack for Claude Code — recording first, monitor-only by default:

```sh
npx @agentsec-ecosystem/cli init
```

It installs the Claude Code hooks and a local daemon, records every tool call (arguments redacted
by default), and enforces nothing until you opt in. `agentsec init --enforce` turns on the policy
gates.

> **Status: not yet available.** The CLI ships with Wave 0. This is the intended UX, published
> early so we can be held to it.

## Get involved

- Read [`CONTRIBUTING.md`](https://github.com/agentsec-ecosystem/.github/blob/main/CONTRIBUTING.md)
- Report vulnerabilities per [`SECURITY.md`](https://github.com/agentsec-ecosystem/.github/blob/main/SECURITY.md)
- Build with us — see the org's pinned repositories and discussions.

Licensed under the [Apache License 2.0](https://github.com/agentsec-ecosystem/.github/blob/main/LICENSE).
