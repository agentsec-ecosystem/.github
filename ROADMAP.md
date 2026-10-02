# Roadmap

**One brand, one install.** Each wave proves exactly one headline capability — and no wave ships
unless its tools can be demoed to a real user in under 10 minutes.

| Wave | Claim | Headline tools |
|---|---|---|
| **0** | *Stop it* | agentwatch · agentpolicy · agentkeys · agenthalt · agentdrill |
| **1** | *Gate it* | agentgate · policyweave · agentseatbelt |
| **2** | *Can't evade it* | agentkernel · budgets · step-up · graduated stops |
| **3** | *Prove it* | agentcomply · fleet aggregation · marketplace rule packs |

The capability order is fixed: **monitor → alert → block/limit → revoke**.

## Wave 0 — thin-slice meta-MVP

Proves *one harness, all four capabilities, in 15 minutes* (Claude Code first, monitor-only by
default). Shipped as **one** install, not five launches.

- **agentwatch v0.1** — record every tool call; OpenTelemetry GenAI + the open security-event schema
- **agentpolicy v0.1** — Cedar PDP: allow / deny / ask / rate-limit / redact
- **agentkeys v0.1** — never-in-context credential broker + one-command revoke
- **agenthalt v0.1** — halt/pause across layers + evidence snapshot
- **agentdrill v0.1** — attack packs that gate the rest
- **One install:** `npx @agentsec-ecosystem/cli init` (monitor-only by default)

**Exit gate:** all four capabilities running on Claude Code in ≤15 min, zero code changes, and the
three demos (Replit gate, poisoned-tool block, kill-switch) reproducible from the README.

## Wave 1 — gate it

agentgate v1.0 (spec-conformant MCP OAuth 2.1 proxy + tool-trust/change-detection) · policyweave
v0.1 (Claude Code + Cursor targets) · agentseatbelt v0.1 (macOS wedge) · agentdrill MCP attack
packs (poisoning / shadowing / rug-pull).

## Wave 2 — can't evade it

agentkernel v1.0 (Linux eBPF, process-lineage attribution) · agentpolicy blast-radius budgets ·
agentkeys step-up issuance + stdio MCP credential virtualization · agenthalt graduated stops and
dead-man switches.

## Wave 3 — prove it

agentcomply v1.0 (SOC 2 / ISO 42001 evidence automation) · policyweave enterprise lock mode · fleet
aggregation · marketplace rule packs · A2A support as the spec stabilizes.

## Honesty

Per-tool status is published as it really is. See each repository's README `Status` section, and the
[org profile](./profile/README.md). A public benchmark (including what we miss) is planned.
