# Alexandre Beguel · Arquitecto de IA agéntica & CAIO externo

[English](README.md) · [Français](README.fr.md) · **Español**

Acompaño a los equipos desde la arquitectura hasta la puesta en producción de sistemas de IA generativa, con calidad, costes y gobernanza medibles. Vivo en París, soy fundador de Digitalizor y Chief AI Officer (CAIO) externo, con 20 años de experiencia en TI, datos e IA.

**Mis ejes:** sistemas de IA observables, gobernanza basada en evidencias y flujos de agentes controlados.

[Web](https://beguel.com/) · [LinkedIn](https://www.linkedin.com/in/beguel/) · [Malt](https://www.malt.fr/profile/alexandrebeguel) · [Portfolio técnico](https://alebgl77.github.io/es/)

## Proyectos seleccionados

| Proyecto | Objetivo | Disponibilidad |
| --- | --- | --- |
| **[Grafana LLMOps Forge](https://github.com/alebgl77/grafana-llmops-forge)** | Descubrir la telemetría existente y generar dashboards de Grafana para costes LLM, agentes, calidad y gobernanza. Comprobaciones automáticas de consultas y despliegues; revisión visual separada. | **[v2.0.4](https://github.com/alebgl77/grafana-llmops-forge/releases/tag/v2.0.4)** |
| **[OpenShadow AI](https://github.com/alebgl77/open-shadow-ai)** | Correlacionar señales de red, equipos e identidad para descubrir Shadow AI con alojamiento propio. Cada hallazgo distingue presencia de uso observado. | **[v0.3.0 preview](https://github.com/alebgl77/open-shadow-ai/releases/tag/v0.3.0)**; pilotos controlados |
| **[FTP Deploy MCP](https://github.com/alebgl77/ftp-deploy-mcp)** | Desplegar por FTP/FTPS/SFTP con confinamiento de rutas y fijación de clave del servidor. Confirmación, promoción por etapas y rollback pertenecen al flujo duradero opcional (`stateDir`). | **[v0.3.2](https://github.com/alebgl77/ftp-deploy-mcp/releases/tag/v0.3.2)**; npm + registro MCP |
| **[OpenSpanGuard](https://github.com/alebgl77/openspanguard)** | Enriquecer spans de generación OTLP/HTTP JSON con señales de evaluación y cobertura, preservando la identidad de las trazas y las marcas de tiempo. | **Developer preview**; código fuente + demo sin conexión |
| **[TierDecay](https://github.com/alebgl77/tierdecay)** | Certificar modelos más económicos para tareas de código recurrentes, con comprobaciones estadísticas y recertificación cuando cambian los modelos. | **[v0.5.0](https://github.com/alebgl77/tierdecay/releases/tag/v0.5.0)**; CLI + MCP |
| **[Claude, Inc.](https://github.com/alebgl77/claude-inc)** | Estructurar proyectos con manuales de habilidades por departamento, revisiones acotadas y registros de artefactos. | **[v1.5.1](https://github.com/alebgl77/claude-inc/releases/tag/v1.5.1)**: 54 manuales / 8 departamentos. Código en desarrollo: 64 / 9, con CAIO y Growth. |

### Evidencias consultables

- **Forge:** [Consultas PromQL generadas ejecutadas en Prometheus y comprobaciones E2E de Grafana](https://github.com/alebgl77/grafana-llmops-forge#how-this-is-verified). La revisión visual semántica es un paso separado, realizado por una persona o un agente.
- **TierDecay:** [piloto controlado y replay del protocolo](https://github.com/alebgl77/tierdecay/blob/main/benchmarks/pilot-v1/RESULTS.md): 36 ejecuciones + 3 destilaciones; **24 % de ahorro estimado en replay** frente a always-frontier. El resultado **0,657×** compara el modelo rápido sin playbook con frontier, con costes normalizados de caché caliente. Ambos resultados se limitan a esta fixture.
- **FTP Deploy MCP:** [43 escenarios programados en cada uno de los idiomas inglés y francés](https://github.com/alebgl77/ftp-deploy-mcp), con un cliente SDK MCP real y un adaptador remoto en memoria. El repositorio documenta por separado la validación de transportes y clientes.

### Herramientas complementarias

**[harnessmeter](https://github.com/alebgl77/harnessmeter)** estima la huella de tokens de instrucciones y contexto. npm **0.3.0** cubre el flujo Claude publicado; Codex, auditoría estática, baselines y presupuestos CI están disponibles actualmente desde el código fuente aún no publicado. El perfilado local funciona sin conexión por defecto; la revisión T2 opcional llama a un proveedor de modelos.

**[Generative Engine Monitor](https://github.com/alebgl77/generative-engine-monitor)** compara la visibilidad de marcas en respuestas de las API de proveedores, con intervalos de confianza y replay de respuestas almacenadas. **[dsh-plugin-otel-genai](https://github.com/alebgl77/dsh-plugin-otel-genai)** ofrece instrumentación de telemetría sin contenido. **[awesome-ai-architect](https://github.com/alebgl77/awesome-ai-architect)** cartografía el stack de ingeniería GenAI.

## Contribuciones a otros proyectos

- **[AgentShield #123](https://github.com/affaan-m/agentshield/pull/123) — integrada:** descubrimiento y clasificación de `.mcp.json` en la raíz, con pruebas de regresión de seguridad.
- **[LibreChat #15046](https://github.com/LibreChat-AI/LibreChat/pull/15046) — documentación integrada:** rutas portables de fuentes de agentes y coherencia entre las instrucciones de `CLAUDE.md` y `AGENTS.md`.
- **[Claude SEO #285](https://github.com/AgriciDaniel/claude-seo/pull/285):** correcciones de detección de JSON-LD, [incorporadas en v2.3.0 con atribución](https://github.com/AgriciDaniel/claude-seo/pull/285#issuecomment-5623681972).
- **Grafana plugin-tools — integradas:** [guía de commits firmados](https://github.com/grafana/plugin-tools/pull/2841) y [scaffold de Node 24](https://github.com/grafana/plugin-tools/pull/2830).

Propuestas en curso: [OpenTelemetry GenAI #516](https://github.com/open-telemetry/semantic-conventions-genai/pull/516), en revisión; [OpenWiki #818](https://github.com/langchain-ai/openwiki/pull/818), **borrador**, pendiente de validación con un proveedor real.

## Trabajar conmigo

Arquitectura y RAG · evaluación, LLMOps y FinOps · inventarios de IA y evidencias de auditoría · control del acceso a herramientas · CAIO externo y formación de equipos.

Trabajo con los requisitos de evidencia del EU AI Act, ISO/IEC 42001 y NIST AI RMF. Mis principios: modos de fallo explícitos, mínimo privilegio, componentes revisables y resultados medidos.

**Stack principal:** Python · TypeScript · MCP · OpenTelemetry · Prometheus · Grafana · Docker.

París, Francia · Francés, inglés y español · [Contacto](https://beguel.com/)

<sub>Estado de proyectos y contribuciones revisado el 22 de octubre de 2026. Arriba se distinguen las versiones publicadas del código en desarrollo.</sub>
