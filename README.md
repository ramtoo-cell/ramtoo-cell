# Hi, I'm Ram 👋

**Helping Claude reason well** on the hardest judgment-heavy problems in policy, law, economics, and safety.

I work where AI reasoning meets the judgment-heavy problems it has to survive in the real world — statutes, contracts, budgets, and human oversight. The problems with no single checkable answer, where getting it right takes the kind of judgment experts spend years building. By day I lead technology audit innovation at a Fortune-10 company. The rest of the time I build the tooling I wish existed: evals that test whether a model reasons or just recites, policy gates, guardrails, and tamper-evident audit trails for LLMs and autonomous agents.

**Thesis:** a model that cannot show its work under a constraint cannot be trusted with the decision. Every reasoning step should leave evidence that an auditor, a regulator, or an on-call engineer can verify afterward.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ramkumar-bharathan-vicepresidenttechnologybusinessprocessauditinnovation)
[![Booth story](https://img.shields.io/badge/Chicago_Booth-My_Story-800000)](https://www.chicagobooth.edu/why-booth/stories/from-a-small-village-to-an-executive-mba)
[![Flagship: agent-guardian](https://img.shields.io/badge/⚡_agent--guardian-Flagship-2ea043)](https://github.com/ramtoo-cell/agent-guardian)

![Helping AI systems reason well under constraints](assets/hero-light.svg)

## 🎯 Fellowship-relevant work

Current builds on how AI systems reason about policy, law, economics, and safety trade-offs:

- **[agent-guardian](https://github.com/ramtoo-cell/agent-guardian)** — flagship governance sidecar. Policy enforcement, budgets, a hash-chained audit log, and red-team evals, 103/103 tests green. A reasoning-eval module is landing this week: scoring a model callable on contract-clause interpretation, policy trade-offs, and mechanism-design cases, with pass-rate and calibration reporting.
- **[reasoning-eval-harness](https://github.com/ramtoo-cell/reasoning-eval-harness)** — *shipping this week.* Standalone harness for structured-reasoning evals: register task suites, run any model callable, report accuracy, calibration, and a failure taxonomy. Built because benchmarks that test recall do not test reasoning.
- **[policy-reasoning-bench](https://github.com/ramtoo-cell/policy-reasoning-bench)** — *shipping this week.* A hand-built benchmark (targeting 60–100 cases) of regulatory and cost-benefit analysis tasks with expert rubrics — across philosophy, economics, and law/policy: principle-labeled trade-off cases, incentive analysis, and EU AI Act / NIST RMF classification. Every case tests reasoning, not recall.
- **[awesome-ai-governance](https://github.com/ramtoo-cell/awesome-ai-governance)** — 51 curated resources across 8 sections: the frameworks, eval harnesses, and red-teaming tools behind serious AI assurance work.

## What I work on

- 🧠 **Reasoning under constraints** — evals and benchmarks for policy, legal, and economic reasoning in LLMs; calibration and failure analysis
- 🛡️ **AI agent governance** — policy engines, budget guardrails, human-approval gates, kill switches
- 🔍 **AI safety & alignment** — red-teaming, eval harnesses, unlearning, watermarking, calibration
- ⚖️ **Audit automation** — control mapping (EU AI Act, NIST AI RMF, ISO 42001, SOC 2), evidence pipelines, continuous assurance

![Reference architecture: agent loop, policy gate, runtime guard, human approval and tool execution, backed by safety evals, injection defense, drift monitoring, a kill switch, and a hash-chained audit ledger](assets/arch-light.svg)

## ⭐ Flagship projects

### [agentgate](https://github.com/ramtoo-cell/agentgate)

**Policy, human approval, and a tamper-evident audit trail for every AI agent tool call.** Use it as a Python decorator, or as a drop-in **MCP proxy** in front of any MCP server (Claude Desktop, Cursor) with zero code changes.

- Default-deny JSON policies. Tools the agent can never use are hidden from the model entirely.
- Hash-chained, optionally HMC-keyed audit ledger. `agentgate verify` pinpoints the first tampered line.
- Pluggable human approval (Slack, tickets, any executable), plus secret/PII redaction and rate limits.
- **~65 µs per call** after profiling-driven optimization (4× faster than v0.1). Zero dependencies, 60 tests, 95% coverage, CI on Python 3.9–3.13.
- Google-style design doc with threat model, tested end to end against the reference MCP filesystem server.

```
pip install git+https://github.com/ramtoo-cell/agentgate
```

### [agent-guardian](https://github.com/ramtoo-cell/agent-guardian)

A governance sidecar for AI agents. Wrap any agent to get policy enforcement (blocklists, PII redaction, prompt-injection detection), budgets (steps, tokens, cost, latency), a tamper-evident audit log, and built-in red-team evals with a scorecard. A CLI writes a Markdown governance report. 103/103 tests passing.

```
pip install git+https://github.com/ramtoo-cell/agent-guardian
```

## 📦 The 500-repo build

358 public repositories and counting — the full build is 500. Each one is small, self-contained, tested, and does one thing. **[Browse the full index →](https://github.com/ramtoo-cell?tab=repositories)**

- **🛡️ AI safety & alignment** — 100 repos. Red-teaming, interpretability, unlearning, watermarking, calibration.
  - [jailbreak-fuzzer](https://github.com/ramtoo-cell/jailbreak-fuzzer) · [layered-defense](https://github.com/ramtoo-cell/layered-defense) · [tripwire-eval](https://github.com/ramtoo-cell/tripwire-eval) · [circuit-graph](https://github.com/ramtoo-cell/circuit-graph) · [gradient-unlearning](https://github.com/ramtoo-cell/gradient-unlearning) · [watermark-greenlist](https://github.com/ramtoo-cell/watermark-greenlist)
- **⚖️ AI governance & audit** — 50 repos. Controls, evidence, regulatory mapping, incident response.
  - [audit-trail](https://github.com/ramtoo-cell/audit-trail) · [policy-engine](https://github.com/ramtoo-cell/policy-engine) · [eu-ai-act-mapper](https://github.com/ramtoo-cell/eu-ai-act-mapper) · [control-mapper](https://github.com/ramtoo-cell/control-mapper) · [model-risk-register](https://github.com/ramtoo-cell/model-risk-register) · [kill-switch](https://github.com/ramtoo-cell/kill-switch)
- **🤖 Agentic systems** — 100 repos. Agent loops, memory, MCP, orchestration, sandboxing, markets.
  - [react-loop](https://github.com/ramtoo-cell/react-loop) · [mcp-server](https://github.com/ramtoo-cell/mcp-server) · [hitl-approvals](https://github.com/ramtoo-cell/hitl-approvals) · [fs-jail](https://github.com/ramtoo-cell/fs-jail) · [contract-net](https://github.com/ramtoo-cell/contract-net) · [trajectory-replayer](https://github.com/ramtoo-cell/trajectory-replayer)

## 📊 Stats

[![Ram's GitHub stats](https://github-readme-stats.vercel.app/api?username=ramtoo-cell&show_icons=true&theme=transparent&hide_border=true&count_private=false)](https://github.com/ramtoo-cell)
[![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=ramtoo-cell&layout=compact&theme=transparent&hide_border=true)](https://github.com/ramtoo-cell)

## How I build

| Principle | In practice |
| --- | --- |
| **Evidence over assertion** | Decisions, prompts, and tool calls are hash-chained and can be replayed. If it wasn't logged, it didn't happen. |
| **Reasoning, not recall** | Evals test whether a model works through a constraint, not whether it memorized the answer. Gold cases are hand-built, with rubrics. |
| **Default deny** | Egress, file system, tools, and quotas start closed. Agents get capabilities one at a time, on purpose. |
| **Small, sharp primitives** | One concern per repo, standard library first, deterministic tests. Adopt one piece without taking all of them. |
| **Controls map to frameworks** | Every control traces to the EU AI Act, NIST AI RMF, ISO 42001, or SOC 2 — audit becomes a query instead of a project. |
| **Humans hold the keys** | Approval queues, escalation ladders, a two-person kill switch. Autonomy is granted, never assumed. |

## Background

- **Education:** Chicago Booth MBA (Honors) · Purdue M.S. Artificial Intelligence *(in progress)* · CISA *(in progress)*
- **Research:** 1 AI patent filed, 1 in preparation · 4 published AI disclosures
- **Focus:** model risk, reasoning evals, AI audit trails, red-teaming, agent safety

Building in public, delivering concrete results. If you work on AI reasoning evals, assurance, or audit automation, let's talk — open an issue on any repo.
