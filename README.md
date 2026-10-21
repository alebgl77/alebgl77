# Agentic AI Architect · LLMOps & AI Governance

**Production GenAI that can be measured, audited and controlled.**

I design agentic systems and the layer most teams skip: telemetry, cost attribution, evaluation coverage, audit evidence and least-privilege tool access. Independent Data & AI consultant and external CAIO based in Paris, with 20 years across IT, data and AI.

[View consulting work](https://beguel.com/) · [Connect on LinkedIn](https://www.linkedin.com/in/beguel/) · [En français](#en-mission)

> **Proof, not slides.** A cheaper model tier at **0.66×** frontier cost in a 36-run pilot · **63/63** generated PromQL queries executed on a real Prometheus · E2E CI on **Grafana 9.5 → 13.2** · an MCP server on the **Official MCP Registry** · merged upstream work in **LibreChat**, **AgentShield** and **Grafana plugin-tools**.

## Open-source work

### 1. LLM observability and FinOps on an open stack

OpenTelemetry GenAI → Prometheus → Grafana, self-hosted, on the telemetry you already emit.

- **[grafana-llmops-forge](https://github.com/alebgl77/grafana-llmops-forge)**: discovers what a Grafana deployment actually collects (OTel GenAI, LiteLLM, vLLM/TGI, DCGM), then generates, deploys and visually verifies seven dashboards for FinOps, agents, quality and governance, with multi-window burn-rate SLO alerts.<br><sub>v2.0 · zero dependencies · E2E CI on Grafana 9.5 → 13.2 · 63/63 generated queries executed on a real Prometheus · listed in awesome-observability</sub>
- **[openspanguard](https://github.com/alebgl77/openspanguard)**: an OTLP enrichment gateway that evaluates completed generation spans, keeps original trace IDs and timestamps, and exposes evaluation coverage next to quality scores, so a good average cannot hide unevaluated traffic.<br><sub>developer preview · offline demo and Tempo/Alertmanager stack</sub>
- **[dsh-plugin-otel-genai](https://github.com/alebgl77/dsh-plugin-otel-genai)**: content-free OpenTelemetry GenAI token and latency metrics for DeepSeek Harness, ready for the forge dashboards.

### 2. Evidence-first AI governance

- **[open-shadow-ai](https://github.com/alebgl77/open-shadow-ai)**: self-hosted Shadow AI discovery that correlates DNS and proxy logs, Zeek/Suricata, an endpoint agent (processes, browser extensions) and Entra ID / Active Directory, with an explicit evidence level per finding: presence is never reported as usage.<br><sub>0.3 preview · 11-job CI with SBOM and signed image evidence · OIDC SSO and SCIM · EN/FR/zh-CN</sub>
- **Governance blueprint of the forge**: maps EU AI Act articles 12, 26(6), 50 and 73, ISO/IEC 42001 and NIST AI RMF to live signals: logging continuity, automatic model inventory and incident watch. An evidence layer for auditors, not legal advice.

### 3. Agents under control

- **[ftp-deploy-mcp](https://github.com/alebgl77/ftp-deploy-mcp)**: an MCP deployment server for FTP, FTPS and SFTP with local-root confinement, SFTP host-key pinning, SHA-256-verified staged promotion, explicit human confirmation and rollback.<br><sub>npm · Official MCP Registry · listed in awesome-mcp-servers · 43 scripted scenarios run in English and French against the real MCP SDK client</sub>
- **[tierdecay](https://github.com/alebgl77/tierdecay)**: a per-repo learning layer for AI coding routers. It moves a recurring task class to a cheaper tier only after statistically confirmed successes, and recertifies it when models change.<br><sub>pilot: 0.66× frontier cost per task (95% interval 0.63–0.69), 24% saved against always-frontier · SBOM · OCI image · MCP server</sub>
- **[claude-inc](https://github.com/alebgl77/claude-inc)**: a Claude Code plugin that runs a project as a virtual company, with peer CEO, CTO and CAIO, nine departments, 64 skill manuals, bounded review loops and SHA-256 records of every submitted artifact.<br><sub>v1.5 · the most-starred project of this profile</sub>
- **[harnessmeter](https://github.com/alebgl77/harnessmeter)**: an offline context profiler for Claude Code and Codex that measures the token footprint of instructions and skills, enforces CI budgets against a baseline and proposes evidence-graded demotions.<br><sub>npm · zero dependencies · CI on Linux, macOS and Windows</sub>

Also: **[generative-engine-monitor](https://github.com/alebgl77/generative-engine-monitor)** measures brand visibility in AI answers, comparing parametric and web-grounded modes with bootstrap confidence intervals. **[awesome-ai-architect](https://github.com/alebgl77/awesome-ai-architect)** is a self-updating map of the GenAI engineering stack, classified daily by GitHub Actions ([interactive explorer](https://alebgl77.github.io/awesome-ai-architect/)).

## Upstream contributions

- **[LibreChat](https://github.com/LibreChat-AI/LibreChat/pull/15046)**: merged. Made `CLAUDE.md` portable by replacing a machine-specific agents source path, and restored `CLAUDE.md`/`AGENTS.md` parity for auth-cache guidance.
- **[AgentShield](https://github.com/affaan-m/agentshield/pull/123)**: merged. The scanner now discovers and classifies root `.mcp.json` files, so MCP configurations reach the security rules, with regression coverage; all 16 review threads were resolved.
- **[Claude SEO](https://github.com/AgriciDaniel/claude-seo/pull/285)**: improved JSON-LD detection and removed template-expression false positives. The maintainer [confirmed](https://github.com/AgriciDaniel/claude-seo/pull/285#issuecomment-5623681972) it landed in v2.3.0 with authorship preserved.
- **Grafana plugin-tools**: two merged contributions, [signed-commit contributor guidance](https://github.com/grafana/plugin-tools/pull/2841) and a [Node 24 `.nvmrc` scaffold update](https://github.com/grafana/plugin-tools/pull/2830).
- **In review**: [OpenTelemetry GenAI semantic conventions](https://github.com/open-telemetry/semantic-conventions-genai/pull/516), recording token usage on `fetch_response` spans, and [LangChain OpenWiki](https://github.com/langchain-ai/openwiki/pull/818), Mistral as a model provider.

## En mission

J'accompagne des ETI, des startups et des e-commerçants du cadrage à l'industrialisation de la GenAI. Les dépôts ci-dessus montrent la méthode ; en mission, je l'applique à votre SI, à vos données et à vos contraintes.

- **Cadrage et architecture** : cas d'usage, build vs buy, RAG, systèmes multi-agents (LangGraph), choix des modèles et de l'hébergement.
- **Mise en production mesurable** : évaluation (RAGAS), observabilité, coûts par équipe et par modèle, SLO de qualité et de latence.
- **Gouvernance et conformité** : inventaire du Shadow AI, traçabilité et preuves d'audit au regard de l'AI Act, de l'ISO/IEC 42001 et du NIST AI RMF, contrôle des accès des agents aux outils.
- **CAIO externalisé et formation** : feuille de route IA, conduite du changement, montée en compétence des équipes sur Claude Code et les systèmes agentiques.

Échangeons sur votre projet : [beguel.com](https://beguel.com/) · [LinkedIn](https://www.linkedin.com/in/beguel/)

## Working principles

- Start with the problem, constraints and failure modes.
- Treat evaluation and observability as product requirements.
- Minimize privileges and data exposure; make consequential actions explicit.
- Prefer simple, reviewable components and measurable automation.

## Core tools and technologies

A focused stack for agentic orchestration, evaluation, serving and cloud-native operations.

<div align="center">
<table width="100%">
<tr>
<td align="center" width="16.66%">
  <img src="https://github.com/langchain-ai.png?size=96" width="48" height="48" alt="LangGraph">
  <br>LangGraph
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/crewAIInc.png?size=96" width="48" height="48" alt="CrewAI">
  <br>CrewAI
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/NousResearch.png?size=96" width="48" height="48" alt="Hermes Agent">
  <br>Hermes Agent
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/openai.png?size=96" width="48" height="48" alt="OpenAI Agents">
  <br>OpenAI Agents
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/modelcontextprotocol.png?size=96" width="48" height="48" alt="MCP">
  <br>MCP
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/anthropics.png?size=96" width="48" height="48" alt="Claude Code">
  <br>Claude Code
</td>
</tr>
<tr>
<td align="center" width="16.66%">
  <img src="https://github.com/explodinggradients.png?size=96" width="48" height="48" alt="RAGAS">
  <br>RAGAS
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/langfuse.png?size=96" width="48" height="48" alt="Langfuse">
  <br>Langfuse
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/open-telemetry.png?size=96" width="48" height="48" alt="OpenTelemetry">
  <br>OpenTelemetry
</td>
<td align="center" width="16.66%">
  <img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" width="48" height="48" alt="Hugging Face">
  <br>Hugging Face
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/vllm-project.png?size=96" width="48" height="48" alt="vLLM">
  <br>vLLM
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/BerriAI.png?size=96" width="48" height="48" alt="LiteLLM">
  <br>LiteLLM
</td>
</tr>
<tr>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=docker" width="48" height="48" alt="Docker">
  <br>Docker
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=kubernetes" width="48" height="48" alt="Kubernetes">
  <br>Kubernetes
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=terraform" width="48" height="48" alt="Terraform">
  <br>Terraform
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=prometheus" width="48" height="48" alt="Prometheus">
  <br>Prometheus
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=grafana" width="48" height="48" alt="Grafana">
  <br>Grafana
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=postgres" width="48" height="48" alt="PostgreSQL">
  <br>PostgreSQL
</td>
</tr>
<tr>
<td align="center" width="16.66%">
  <img src="https://github.com/langchain-ai.png?size=96" width="48" height="48" alt="LangChain">
  <br>LangChain
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/openai.png?size=96" width="48" height="48" alt="Codex">
  <br>Codex
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=pytorch" width="48" height="48" alt="PyTorch">
  <br>PyTorch
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/ollama.png?size=96" width="48" height="48" alt="Ollama">
  <br>Ollama
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=fastapi" width="48" height="48" alt="FastAPI">
  <br>FastAPI
</td>
<td align="center" width="16.66%">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://unpkg.com/@lobehub/icons-static-png@latest/dark/grok.png">
    <source media="(prefers-color-scheme: light)" srcset="https://unpkg.com/@lobehub/icons-static-png@latest/light/grok.png">
    <img src="https://unpkg.com/@lobehub/icons-static-png@latest/light/grok.png" width="48" height="48" alt="Grok">
  </picture>
  <br>Grok
</td>
</tr>
<tr>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=aws" width="48" height="48" alt="AWS">
  <br>AWS
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=gcp" width="48" height="48" alt="GCP">
  <br>GCP
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=azure" width="48" height="48" alt="Azure AI">
  <br>Azure AI
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/pgvector.png?size=96" width="48" height="48" alt="pgvector">
  <br>pgvector
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=redis" width="48" height="48" alt="Redis">
  <br>Redis
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/qdrant.png?size=96" width="48" height="48" alt="Qdrant">
  <br>Qdrant
</td>
</tr>
<tr>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=python" width="48" height="48" alt="Python">
  <br>Python
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=typescript" width="48" height="48" alt="TypeScript">
  <br>TypeScript
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=javascript" width="48" height="48" alt="JavaScript">
  <br>JavaScript
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=bash" width="48" height="48" alt="Bash">
  <br>Bash
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=git" width="48" height="48" alt="Git">
  <br>Git
</td>
<td align="center" width="16.66%">
  <img src="https://skillicons.dev/icons?i=githubactions" width="48" height="48" alt="GitHub Actions">
  <br>GitHub Actions
</td>
</tr>
<tr>
<td align="center" width="16.66%">
  <img src="https://github.com/google-gemini.png?size=96" width="48" height="48" alt="Gemini">
  <br>Gemini
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/QwenLM.png?size=96" width="48" height="48" alt="Qwen">
  <br>Qwen
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/zai-org.png?size=96" width="48" height="48" alt="Z.ai">
  <br>Z.ai
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/deepseek-ai.png?size=96" width="48" height="48" alt="DeepSeek">
  <br>DeepSeek
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/mistralai.png?size=96" width="48" height="48" alt="Mistral AI">
  <br>Mistral AI
</td>
<td align="center" width="16.66%">
  <img src="https://github.com/OpenRouterTeam.png?size=96" width="48" height="48" alt="OpenRouter">
  <br>OpenRouter
</td>
</tr>
</table>
</div>

## Contact

[beguel.com](https://beguel.com) · [LinkedIn](https://www.linkedin.com/in/beguel/)

French is my native language; I work professionally in English and Spanish.
