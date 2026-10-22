# Alexandre Beguel · Architecte IA agentique & CAIO externalisé

[English](README.md) · **Français** · [Español](README.es.md)

J’accompagne les équipes de l’architecture à la mise en production de systèmes d’IA générative, avec une qualité, des coûts et une gouvernance mesurables. Basé à Paris, je suis fondateur de Digitalizor et Chief AI Officer (CAIO) externalisé, avec 20 ans d’expérience dans l’IT, la data et l’IA.

**Mes axes :** systèmes d’IA observables, gouvernance fondée sur des preuves et workflows d’agents maîtrisés.

[Site](https://beguel.com/) · [LinkedIn](https://www.linkedin.com/in/beguel/) · [Malt](https://www.malt.fr/profile/alexandrebeguel) · [Portfolio technique](https://alebgl77.github.io/fr/)

## Projets sélectionnés

| Projet | Objectif | Disponibilité |
| --- | --- | --- |
| **[Grafana LLMOps Forge](https://github.com/alebgl77/grafana-llmops-forge)** | Découvrir la télémétrie existante et générer des dashboards Grafana pour les coûts LLM, les agents, la qualité et la gouvernance. Contrôles automatisés des requêtes et déploiements ; revue visuelle distincte. | **[v2.0.4](https://github.com/alebgl77/grafana-llmops-forge/releases/tag/v2.0.4)** |
| **[OpenShadow AI](https://github.com/alebgl77/open-shadow-ai)** | Croiser les signaux réseau, poste de travail et identité pour détecter le Shadow AI en auto-hébergement. Chaque constat distingue présence et usage observé. | **[v0.3.0 preview](https://github.com/alebgl77/open-shadow-ai/releases/tag/v0.3.0)** ; pilotes contrôlés |
| **[FTP Deploy MCP](https://github.com/alebgl77/ftp-deploy-mcp)** | Déployer en FTP/FTPS/SFTP avec confinement des racines et épinglage de clé hôte. Confirmation, promotion par étapes et rollback relèvent du workflow durable optionnel (`stateDir`). | **[v0.3.2](https://github.com/alebgl77/ftp-deploy-mcp/releases/tag/v0.3.2)** ; npm + registre MCP |
| **[OpenSpanGuard](https://github.com/alebgl77/openspanguard)** | Enrichir les spans de génération OTLP/HTTP JSON avec des signaux d’évaluation et leur couverture, en préservant l’identité des traces et les horodatages. | **Developer preview** ; source + démo hors ligne |
| **[TierDecay](https://github.com/alebgl77/tierdecay)** | Qualifier des modèles moins coûteux pour les tâches de code récurrentes, avec contrôles statistiques et requalification lors des changements de modèles. | **[v0.5.0](https://github.com/alebgl77/tierdecay/releases/tag/v0.5.0)** ; CLI + MCP |
| **[Claude, Inc.](https://github.com/alebgl77/claude-inc)** | Structurer les projets avec des manuels de compétences par département, des revues bornées et des traces d’artefacts. | **[v1.5.1](https://github.com/alebgl77/claude-inc/releases/tag/v1.5.1)** : 54 manuels / 8 départements. Source de développement : 64 / 9, avec CAIO et Growth. |

### Preuves consultables

- **Forge :** [Requêtes PromQL générées exécutées sur Prometheus et contrôles E2E Grafana](https://github.com/alebgl77/grafana-llmops-forge#how-this-is-verified). La revue visuelle sémantique est une étape distincte, réalisée par une personne ou un agent.
- **TierDecay :** [pilote contrôlé et replay du protocole](https://github.com/alebgl77/tierdecay/blob/main/benchmarks/pilot-v1/RESULTS.md) : 36 exécutions + 3 distillations ; **24 % d’économie estimée en replay** face à always-frontier. Le résultat **0,657×** compare le modèle rapide sans playbook au modèle frontier, avec des coûts normalisés de cache chaud. Ces résultats restent limités à cette fixture.
- **FTP Deploy MCP :** [43 scénarios scriptés dans chacune des langues française et anglaise](https://github.com/alebgl77/ftp-deploy-mcp), avec un vrai client SDK MCP et un adaptateur distant en mémoire. Le dépôt détaille séparément la qualification des transports et des clients.

### Outils complémentaires

**[harnessmeter](https://github.com/alebgl77/harnessmeter)** estime l’empreinte en tokens des instructions et du contexte. npm **0.3.0** couvre le workflow Claude publié ; Codex, audit statique, baselines et budgets CI sont actuellement disponibles depuis le source non publié. Le profilage local est hors ligne par défaut ; la revue T2 optionnelle appelle un fournisseur de modèle.

**[Generative Engine Monitor](https://github.com/alebgl77/generative-engine-monitor)** compare la visibilité des marques dans les réponses des API fournisseurs, avec intervalles de confiance et rejeu des réponses conservées. **[dsh-plugin-otel-genai](https://github.com/alebgl77/dsh-plugin-otel-genai)** fournit une instrumentation télémétrique sans contenu. **[awesome-ai-architect](https://github.com/alebgl77/awesome-ai-architect)** cartographie le stack d’ingénierie GenAI.

## Contributions amont

- **[AgentShield #123](https://github.com/affaan-m/agentshield/pull/123) — fusionnée :** découverte et classification des fichiers `.mcp.json` à la racine, avec tests de non-régression de sécurité.
- **[LibreChat #15046](https://github.com/LibreChat-AI/LibreChat/pull/15046) — documentation fusionnée :** chemins portables des sources d’agents et parité des consignes `CLAUDE.md`/`AGENTS.md`.
- **[Claude SEO #285](https://github.com/AgriciDaniel/claude-seo/pull/285) :** corrections de détection JSON-LD, [reprises dans v2.3.0 avec attribution](https://github.com/AgriciDaniel/claude-seo/pull/285#issuecomment-5623681972).
- **Grafana plugin-tools — fusionnées :** [guide de commits signés](https://github.com/grafana/plugin-tools/pull/2841) et [scaffold Node 24](https://github.com/grafana/plugin-tools/pull/2830).

Propositions en cours : [OpenTelemetry GenAI #516](https://github.com/open-telemetry/semantic-conventions-genai/pull/516), en revue ; [OpenWiki #818](https://github.com/langchain-ai/openwiki/pull/818), **brouillon**, en attente de validation avec un fournisseur réel.

## Travailler ensemble

Architecture et RAG · évaluation, LLMOps et FinOps · inventaires IA et preuves d’audit · contrôle de l’accès aux outils · CAIO externalisé et formation des équipes.

Je travaille sur les exigences de preuve de l’EU AI Act, d’ISO/IEC 42001 et du NIST AI RMF. Mes principes : modes d’échec explicites, moindre privilège, composants vérifiables et résultats mesurés.

**Stack principal :** Python · TypeScript · MCP · OpenTelemetry · Prometheus · Grafana · Docker.

Paris, France · Français, anglais et espagnol · [Contact](https://beguel.com/)

<sub>Statut des projets et contributions revu le 22 octobre 2026. Les versions publiées et le source de développement sont distingués ci-dessus.</sub>
