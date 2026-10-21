# Alexandre Beguel · Architecte IA agentique & CAIO externalisé

[English](README.md) · **Français** · [Español](README.es.md)

**Alexandre Beguel est architecte IA agentique et Chief AI Officer (CAIO) externalisé, basé à Paris.** Il construit une IA générative en production que l'on peut mesurer, auditer et maîtriser. Il se concentre sur le LLMOps, le FinOps des LLM, l'évaluation et la gouvernance de l'IA fondée sur les preuves. Ses référentiels de gouvernance : règlement européen sur l'IA (AI Act), ISO/IEC 42001 et NIST AI RMF. Il est le fondateur de Digitalizor et cumule 20 ans d'expérience dans l'IT, la data et l'IA.

[beguel.com](https://beguel.com/) · [LinkedIn](https://www.linkedin.com/in/beguel/) · [Malt](https://www.malt.fr/profile/alexandrebeguel) · [alebgl77.github.io](https://alebgl77.github.io/)

> **Des preuves, pas des slides.** Un niveau de modèle moins cher à **0,66×** le coût d'un modèle frontier, sur un pilote de 36 exécutions · **63/63** requêtes PromQL générées exécutées sur un Prometheus réel · CI E2E sur **Grafana 9.5 → 13.2** · un serveur MCP référencé dans l'**Official MCP Registry** · des contributions fusionnées dans **LibreChat**, **AgentShield** et **Grafana plugin-tools**.

## Travaux open source

### 1. Observabilité et FinOps des LLM sur une stack ouverte

OpenTelemetry GenAI → Prometheus → Grafana, en auto-hébergé, à partir de la télémétrie qu'une plateforme émet déjà.

- **[grafana-llmops-forge](https://github.com/alebgl77/grafana-llmops-forge)** : détecte ce qu'un déploiement Grafana collecte réellement (OTel GenAI, LiteLLM, vLLM/TGI, DCGM), puis génère, déploie et vérifie visuellement sept tableaux de bord FinOps, agents, qualité et gouvernance, avec des alertes SLO burn-rate multi-fenêtres.<br><sub>v2.0 · zéro dépendance · CI E2E sur Grafana 9.5 → 13.2 · 63/63 requêtes générées exécutées sur un Prometheus réel · référencé dans awesome-observability</sub>
- **[openspanguard](https://github.com/alebgl77/openspanguard)** : une passerelle d'enrichissement OTLP qui évalue les spans de génération terminés, conserve les identifiants de trace et les horodatages d'origine, et affiche la couverture d'évaluation à côté des scores de qualité, pour qu'une bonne moyenne ne puisse pas masquer du trafic non évalué.<br><sub>préversion développeur · démo hors ligne et stack Tempo/Alertmanager</sub>
- **[dsh-plugin-otel-genai](https://github.com/alebgl77/dsh-plugin-otel-genai)** : des métriques OpenTelemetry GenAI de tokens et de latence, sans capture de contenu, pour DeepSeek Harness, prêtes pour les tableaux de bord de grafana-llmops-forge.

### 2. Gouvernance de l'IA fondée sur les preuves

- **[open-shadow-ai](https://github.com/alebgl77/open-shadow-ai)** : détection auto-hébergée du Shadow AI, qui corrèle les logs DNS et proxy, Zeek/Suricata, un agent sur les postes de travail (processus, extensions de navigateur) et Entra ID / Active Directory, avec un niveau de preuve explicite pour chaque constat : une présence n'est jamais présentée comme un usage.<br><sub>préversion 0.3 · CI de 11 jobs avec SBOM et preuves de signature des images · SSO OIDC et SCIM · EN/FR/zh-CN</sub>
- **Blueprint de gouvernance de grafana-llmops-forge** : relie les articles 12, 26(6), 50 et 73 de l'AI Act, l'ISO/IEC 42001 et le NIST AI RMF à des signaux observés en continu : continuité de la journalisation, inventaire automatique des modèles et veille sur les incidents. Une couche de preuves pour les auditeurs, pas un avis juridique.

### 3. Agents sous contrôle

- **[ftp-deploy-mcp](https://github.com/alebgl77/ftp-deploy-mcp)** : un serveur MCP de déploiement pour FTP, FTPS et SFTP, avec confinement à la racine locale, épinglage des clés d'hôte SFTP, promotion depuis le staging vérifiée par SHA-256, confirmation humaine explicite et rollback.<br><sub>npm · Official MCP Registry · référencé dans awesome-mcp-servers · 43 scénarios scriptés exécutés en anglais et en français avec le véritable client du SDK MCP</sub>
- **[tierdecay](https://github.com/alebgl77/tierdecay)** : une couche d'apprentissage par dépôt pour les routeurs de code assisté par IA. Elle ne bascule une classe de tâches récurrente vers un niveau moins cher qu'après des succès confirmés statistiquement, et la recertifie quand les modèles changent.<br><sub>pilote : 0,66× le coût d'un modèle frontier par tâche (intervalle à 95 % : 0,63–0,69), 24 % d'économie par rapport à un usage systématique du modèle frontier · SBOM · image OCI · serveur MCP</sub>
- **[claude-inc](https://github.com/alebgl77/claude-inc)** : un plugin Claude Code qui pilote un projet comme une entreprise virtuelle, avec un CEO, un CTO et un CAIO pairs, neuf départements, 64 manuels de skills, des boucles de revue bornées et un enregistrement SHA-256 de chaque artefact soumis.<br><sub>v1.5 · le projet le plus étoilé de ce profil</sub>
- **[harnessmeter](https://github.com/alebgl77/harnessmeter)** : un profileur de contexte hors ligne pour Claude Code et Codex, qui mesure l'empreinte en tokens des instructions et des skills, impose des budgets en CI par rapport à une base de référence et propose des rétrogradations graduées selon le niveau de preuve.<br><sub>npm · zéro dépendance · CI sous Linux, macOS et Windows</sub>

Autres projets : **[generative-engine-monitor](https://github.com/alebgl77/generative-engine-monitor)** mesure la visibilité d'une marque dans les réponses des assistants IA, en comparant le mode paramétrique et le mode avec recherche web, avec des intervalles de confiance bootstrap. **[awesome-ai-architect](https://github.com/alebgl77/awesome-ai-architect)** est une cartographie auto-actualisée de la stack d'ingénierie de l'IA générative, classée chaque jour par GitHub Actions ([explorateur interactif](https://alebgl77.github.io/awesome-ai-architect/)).

## Contributions aux projets open source

- **[LibreChat](https://github.com/LibreChat-AI/LibreChat/pull/15046)** : fusionnée. `CLAUDE.md` est rendu portable par le remplacement d'un chemin source des agents propre à une machine ; la parité `CLAUDE.md`/`AGENTS.md` est rétablie pour les consignes sur le cache d'authentification.
- **[AgentShield](https://github.com/affaan-m/agentshield/pull/123)** : fusionnée. Le scanner détecte et classe désormais les fichiers `.mcp.json` à la racine, afin que les configurations MCP soient soumises aux règles de sécurité, avec des tests de non-régression ; les 16 fils de revue ont tous été résolus.
- **[Claude SEO](https://github.com/AgriciDaniel/claude-seo/pull/285)** : détection JSON-LD améliorée et suppression des faux positifs liés aux expressions de template. Le mainteneur a [confirmé](https://github.com/AgriciDaniel/claude-seo/pull/285#issuecomment-5623681972) son intégration dans la v2.3.0, avec l'attribution à l'auteur préservée.
- **Grafana plugin-tools** : deux contributions fusionnées, des [consignes aux contributeurs sur les commits signés](https://github.com/grafana/plugin-tools/pull/2841) et une [mise à jour du `.nvmrc` du scaffold vers Node 24](https://github.com/grafana/plugin-tools/pull/2830).
- **En cours de revue** : [conventions sémantiques OpenTelemetry GenAI](https://github.com/open-telemetry/semantic-conventions-genai/pull/516), pour enregistrer la consommation de tokens sur les spans `fetch_response`, et [LangChain OpenWiki](https://github.com/langchain-ai/openwiki/pull/818), pour ajouter Mistral comme fournisseur de modèles.

## Missions & conseil

Les missions mènent l'IA générative du cadrage à la production pour des entreprises de taille intermédiaire (ETI), des startups et des acteurs du e-commerce. Les dépôts ci-dessus montrent la méthode ; chaque mission l'applique aux systèmes, aux données et aux contraintes du client.

- **Cadrage et architecture** : cas d'usage, build vs buy, RAG, systèmes multi-agents (LangGraph), choix des modèles et de l'hébergement.
- **Production mesurable** : évaluation des LLM (RAGAS), observabilité, coûts par équipe et par modèle, SLO de qualité et de latence.
- **Gouvernance et conformité** : inventaire du Shadow AI, traçabilité et preuves d'audit au regard de l'AI Act, de l'ISO/IEC 42001 et du NIST AI RMF, accès contrôlé des agents aux outils.
- **CAIO externalisé et formation** : feuille de route IA, conduite du changement, montée en compétences des équipes sur Claude Code et les systèmes agentiques.

## FAQ

**Quelle est la spécialité d'Alexandre Beguel ?**
L'IA générative en production et les agents IA. Il couvre tout le parcours, du cadrage à l'exploitation : architecture, évaluation, observabilité, maîtrise des coûts et gouvernance de l'IA.

**Comment mesurer le coût de ses LLM ?**
Partir de la télémétrie déjà émise, puis attribuer les coûts par équipe, par modèle et par fournisseur. grafana-llmops-forge construit ces tableaux de bord FinOps dans Grafana, sans SDK d'éditeur.

**Comment détecter le Shadow AI en entreprise ?**
Corréler les signaux réseau, poste de travail et identité, sans confondre présence et usage. open-shadow-ai le fait en auto-hébergé, avec un niveau de preuve pour chaque constat.

**Comment préparer ses systèmes d'IA générative à l'AI Act ?**
Constituer d'abord les preuves : inventaire des systèmes d'IA, continuité de la journalisation, mentions de transparence et suivi des incidents. Les obligations de transparence de l'article 50 sont applicables depuis le 2 août 2026. Selon l'omnibus IA (règlement (UE) 2026/1744), les obligations pour les systèmes à haut risque de l'annexe III s'appliquent à partir du 2 décembre 2027.

**Dans quelles langues travaille-t-il ?**
Français (langue maternelle), anglais et espagnol. Il est basé à Paris.

## Principes de travail

- Partir du problème, des contraintes et des modes de défaillance.
- Traiter l'évaluation et l'observabilité comme des exigences produit.
- Réduire au minimum les privilèges et l'exposition des données ; rendre explicites les actions à fort impact.
- Privilégier des composants simples et faciles à relire, et une automatisation mesurable.

## Outils et technologies

Une stack ciblée pour l'orchestration agentique, l'évaluation, le serving de modèles et l'exploitation cloud native.

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

[beguel.com](https://beguel.com/) · [LinkedIn](https://www.linkedin.com/in/beguel/) · [Malt](https://www.malt.fr/profile/alexandrebeguel) · [alebgl77.github.io](https://alebgl77.github.io/)

<sub>Alexandre Beguel · Architecte IA agentique & CAIO externalisé · Paris, France · Mis à jour en octobre 2026</sub>
