# Alexandre Beguel · Agentic AI Architect & external CAIO

**English** · [Français](README.fr.md) · [Español](README.es.md)

I help teams take GenAI from architecture to production, with measurable quality, cost and governance. Based in Paris, I am the founder of Digitalizor and an external Chief AI Officer (CAIO), with 20 years of experience across IT, data and AI.

**My focus:** observable AI systems, evidence-based governance and controlled agent workflows.

[Website](https://beguel.com/) · [LinkedIn](https://www.linkedin.com/in/beguel/) · [Malt](https://www.malt.fr/profile/alexandrebeguel) · [Technical portfolio](https://alebgl77.github.io/)

## Selected projects

| Project | Purpose | Availability |
| --- | --- | --- |
| **[Grafana LLMOps Forge](https://github.com/alebgl77/grafana-llmops-forge)** | Discover existing telemetry and generate Grafana dashboards for LLM costs, agents, quality and governance. Automated query/deployment checks; separate visual review. | **[v2.0.4](https://github.com/alebgl77/grafana-llmops-forge/releases/tag/v2.0.4)** |
| **[OpenShadow AI](https://github.com/alebgl77/open-shadow-ai)** | Correlate network, endpoint and identity signals for self-hosted Shadow AI discovery. Each finding distinguishes presence from observed usage. | **[v0.3.0 preview](https://github.com/alebgl77/open-shadow-ai/releases/tag/v0.3.0)**; controlled pilots |
| **[FTP Deploy MCP](https://github.com/alebgl77/ftp-deploy-mcp)** | FTP/FTPS/SFTP deployment with root confinement and host-key pinning. Confirmation, staged promotion and rollback belong to the optional durable workflow (`stateDir`). | **[v0.3.2](https://github.com/alebgl77/ftp-deploy-mcp/releases/tag/v0.3.2)**; npm + MCP Registry |
| **[OpenSpanGuard](https://github.com/alebgl77/openspanguard)** | Enrich OTLP/HTTP JSON generation spans with evaluation signals and coverage, preserving trace identity and timestamps. | **Developer preview**; source + [offline case study](https://github.com/alebgl77/openspanguard/blob/main/docs/evidence/2026-10-22-offline-http-json.md) |
| **[TierDecay](https://github.com/alebgl77/tierdecay)** | Certify cheaper model tiers for recurring coding tasks, with statistical checks and recertification when models change. | **[v0.5.0](https://github.com/alebgl77/tierdecay/releases/tag/v0.5.0)**; CLI + MCP |
| **[Claude, Inc.](https://github.com/alebgl77/claude-inc)** | Structured project workflows with departmental skill manuals, bounded reviews and artifact records. | **[v1.5.1](https://github.com/alebgl77/claude-inc/releases/tag/v1.5.1)**: 54 manuals / 8 departments. Development source: 64 / 9, with CAIO and Growth. |

### Evidence you can inspect

- **Forge:** [Generated PromQL queries executed against Prometheus and Grafana E2E checks](https://github.com/alebgl77/grafana-llmops-forge#how-this-is-verified). Semantic visual review is a separate human/agent step.
- **TierDecay:** [controlled pilot and protocol replay](https://github.com/alebgl77/tierdecay/blob/main/benchmarks/pilot-v1/RESULTS.md): 36 executor runs + 3 distillations; **24% estimated savings in replay** versus always-frontier. The **0.657×** result compares the cold fast tier with the cold frontier tier. Both results are bounded to this fixture.
- **FTP Deploy MCP:** [43 scripted scenarios in each of English and French](https://github.com/alebgl77/ftp-deploy-mcp), using a real MCP SDK client and an in-memory remote adapter. The repository documents transport and client qualification separately.

### Supporting tools

**[harnessmeter](https://github.com/alebgl77/harnessmeter)** estimates instruction/context token footprints. npm **0.3.0** covers the published Claude workflow; Codex, static audit, baselines and CI budgets are currently available from unreleased source. Local profiling is offline by default; optional T2 review invokes a model provider.

**[Generative Engine Monitor](https://github.com/alebgl77/generative-engine-monitor)** compares brand visibility in provider API responses, with confidence intervals and replay from stored responses. **[dsh-plugin-otel-genai](https://github.com/alebgl77/dsh-plugin-otel-genai)** provides content-free telemetry instrumentation. **[awesome-ai-architect](https://github.com/alebgl77/awesome-ai-architect)** maps the GenAI engineering stack.

## Upstream contributions

- **[AgentShield #123](https://github.com/affaan-m/agentshield/pull/123) — merged:** root `.mcp.json` discovery/classification and security regression coverage.
- **[LibreChat #15046](https://github.com/LibreChat-AI/LibreChat/pull/15046) — merged documentation:** portable agent-source paths and `CLAUDE.md`/`AGENTS.md` guidance parity.
- **[Claude SEO #285](https://github.com/AgriciDaniel/claude-seo/pull/285):** JSON-LD detection fixes, [cherry-picked into v2.3.0 with attribution](https://github.com/AgriciDaniel/claude-seo/pull/285#issuecomment-5623681972).
- **Grafana plugin-tools — merged:** [signed-commit guidance](https://github.com/grafana/plugin-tools/pull/2841) and [Node 24 scaffold](https://github.com/grafana/plugin-tools/pull/2830).

Ongoing proposals: [OpenTelemetry GenAI #516](https://github.com/open-telemetry/semantic-conventions-genai/pull/516), under review; [OpenWiki #818](https://github.com/langchain-ai/openwiki/pull/818), **draft**, awaiting live-provider validation.

## Work with me

Architecture and RAG · evaluation, LLMOps and FinOps · AI inventories and audit evidence · controlled tool access · external CAIO and team training.

I work with EU AI Act, ISO/IEC 42001 and NIST AI RMF evidence requirements. My working principles are explicit failure modes, least privilege, reviewable components and measured outcomes.

**Core stack:** Python · TypeScript · MCP · OpenTelemetry · Prometheus · Grafana · Docker.

Paris, France · French, English and Spanish · [Contact](https://beguel.com/)

<sub>Project and contribution status reviewed 22 October 2026. Releases and development source are distinguished above.</sub>
