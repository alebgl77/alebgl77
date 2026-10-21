# Alexandre Beguel · Arquitecto de IA agéntica y CAIO externo

[English](README.md) · [Français](README.fr.md) · **Español**

**Alexandre Beguel es arquitecto de IA agéntica y Chief AI Officer (CAIO) externo, con sede en París.** Desarrolla IA generativa en producción que puede medirse, auditarse y controlarse. Se centra en LLMOps, FinOps de LLM, evaluación de LLM y gobernanza de la IA basada en evidencias. Sus marcos de referencia son el Reglamento Europeo de IA (AI Act), ISO/IEC 42001 y NIST AI RMF. Es fundador de Digitalizor y cuenta con 20 años de experiencia en TI, datos e IA.

[beguel.com](https://beguel.com/) · [LinkedIn](https://www.linkedin.com/in/beguel/) · [Malt](https://www.malt.fr/profile/alexandrebeguel) · [alebgl77.github.io](https://alebgl77.github.io/)

> **Pruebas, no diapositivas.** Un nivel de modelo más económico, a **0,66×** el coste del modelo frontera, en un piloto de 36 ejecuciones · **63/63** consultas PromQL generadas ejecutadas en un Prometheus real · CI E2E en **Grafana 9.5 → 13.2** · un servidor MCP en el **Official MCP Registry** · contribuciones upstream integradas en **LibreChat**, **AgentShield** y **Grafana plugin-tools**.

## Trabajo open source

### 1. Observabilidad y FinOps de LLM sobre un stack abierto

OpenTelemetry GenAI → Prometheus → Grafana, autoalojado, a partir de la telemetría que la plataforma ya emite.

- **[grafana-llmops-forge](https://github.com/alebgl77/grafana-llmops-forge)**: detecta qué recopila realmente un despliegue de Grafana (OTel GenAI, LiteLLM, vLLM/TGI, DCGM) y después genera, despliega y verifica visualmente siete dashboards de FinOps, agentes, calidad y gobernanza, con alertas de SLO basadas en burn-rate multiventana.<br><sub>v2.0 · cero dependencias · CI E2E en Grafana 9.5 → 13.2 · 63/63 consultas generadas ejecutadas en un Prometheus real · incluido en awesome-observability</sub>
- **[openspanguard](https://github.com/alebgl77/openspanguard)**: un gateway de enriquecimiento OTLP que evalúa los spans de generación completados, conserva los identificadores de traza y las marcas de tiempo originales, y muestra la cobertura de evaluación junto a las puntuaciones de calidad, para que un buen promedio no pueda ocultar tráfico sin evaluar.<br><sub>versión preliminar para desarrolladores · demo sin conexión y stack Tempo/Alertmanager</sub>
- **[dsh-plugin-otel-genai](https://github.com/alebgl77/dsh-plugin-otel-genai)**: métricas OpenTelemetry GenAI de tokens y latencia para DeepSeek Harness, sin capturar contenido, listas para los dashboards de grafana-llmops-forge.

### 2. Gobernanza de la IA basada en evidencias

- **[open-shadow-ai](https://github.com/alebgl77/open-shadow-ai)**: detección autoalojada de IA en la sombra (Shadow AI) que correlaciona registros DNS y de proxy, Zeek/Suricata, un agente de endpoint (procesos, extensiones del navegador) y Entra ID / Active Directory, con un nivel de evidencia explícito por hallazgo: la presencia nunca se reporta como uso.<br><sub>versión preliminar 0.3 · CI de 11 jobs con SBOM y evidencias de imagen firmada · SSO OIDC y SCIM · EN/FR/zh-CN</sub>
- **Esquema de gobernanza de grafana-llmops-forge**: vincula los artículos 12, 26(6), 50 y 73 del AI Act, ISO/IEC 42001 y NIST AI RMF con señales en tiempo real: continuidad de los registros, inventario automático de modelos y vigilancia de incidentes. Una capa de evidencias para auditores, no asesoramiento jurídico.

### 3. Agentes bajo control

- **[ftp-deploy-mcp](https://github.com/alebgl77/ftp-deploy-mcp)**: un servidor MCP de despliegue para FTP, FTPS y SFTP con confinamiento al directorio raíz local, fijación de la clave de host SFTP, promoción por etapas verificada con SHA-256, confirmación humana explícita y rollback.<br><sub>npm · Official MCP Registry · incluido en awesome-mcp-servers · 43 escenarios automatizados ejecutados en inglés y francés contra el cliente real del MCP SDK</sub>
- **[tierdecay](https://github.com/alebgl77/tierdecay)**: una capa de aprendizaje por repositorio para routers de programación con IA. Solo traslada una clase de tareas recurrente a un nivel más económico tras éxitos confirmados estadísticamente, y la recertifica cuando cambian los modelos.<br><sub>piloto: 0,66× el coste frontera por tarea (intervalo del 95 %: 0,63–0,69), un 24 % de ahorro frente a usar siempre el modelo frontera · SBOM · imagen OCI · servidor MCP</sub>
- **[claude-inc](https://github.com/alebgl77/claude-inc)**: un plugin de Claude Code que gestiona un proyecto como una empresa virtual, con un CEO, un CTO y un CAIO en pie de igualdad, nueve departamentos, 64 manuales de skills, ciclos de revisión acotados y registros SHA-256 de cada artefacto entregado.<br><sub>v1.5 · el proyecto con más estrellas de este perfil</sub>
- **[harnessmeter](https://github.com/alebgl77/harnessmeter)**: un perfilador de contexto sin conexión para Claude Code y Codex que mide la huella en tokens de las instrucciones y las skills, aplica presupuestos en CI frente a una línea base y propone degradaciones clasificadas por nivel de evidencia.<br><sub>npm · cero dependencias · CI en Linux, macOS y Windows</sub>

También: **[generative-engine-monitor](https://github.com/alebgl77/generative-engine-monitor)** mide la visibilidad de una marca en las respuestas de la IA y compara los modos paramétrico y con búsqueda web mediante intervalos de confianza bootstrap. **[awesome-ai-architect](https://github.com/alebgl77/awesome-ai-architect)** es un mapa autoactualizable del stack de ingeniería de IA generativa, clasificado a diario con GitHub Actions ([explorador interactivo](https://alebgl77.github.io/awesome-ai-architect/)).

## Contribuciones upstream

- **[LibreChat](https://github.com/LibreChat-AI/LibreChat/pull/15046)**: integrada. `CLAUDE.md` pasa a ser portable al sustituir una ruta de origen de agentes propia de una máquina, y se restablece la paridad entre `CLAUDE.md` y `AGENTS.md` en las indicaciones sobre la caché de autenticación.
- **[AgentShield](https://github.com/affaan-m/agentshield/pull/123)**: integrada. El escáner ahora detecta y clasifica los archivos `.mcp.json` de la raíz, de modo que las configuraciones MCP llegan a las reglas de seguridad, con cobertura de regresión; se resolvieron los 16 hilos de revisión.
- **[Claude SEO](https://github.com/AgriciDaniel/claude-seo/pull/285)**: mejora de la detección de JSON-LD y eliminación de falsos positivos causados por expresiones de plantilla. El mantenedor [confirmó](https://github.com/AgriciDaniel/claude-seo/pull/285#issuecomment-5623681972) su inclusión en la v2.3.0, con la autoría preservada.
- **Grafana plugin-tools**: dos contribuciones integradas, una [guía para colaboradores sobre commits firmados](https://github.com/grafana/plugin-tools/pull/2841) y una [actualización del scaffold `.nvmrc` a Node 24](https://github.com/grafana/plugin-tools/pull/2830).
- **En revisión**: [convenciones semánticas de OpenTelemetry GenAI](https://github.com/open-telemetry/semantic-conventions-genai/pull/516), para registrar el uso de tokens en los spans `fetch_response`, y [LangChain OpenWiki](https://github.com/langchain-ai/openwiki/pull/818), con Mistral como proveedor de modelos.

## Consultoría y asesoramiento

Los proyectos llevan la IA generativa desde la definición del alcance hasta producción en empresas medianas, startups y negocios de comercio electrónico. Los repositorios anteriores muestran el método; cada proyecto lo aplica a los sistemas, los datos y las restricciones del cliente.

- **Definición del alcance y arquitectura**: casos de uso, desarrollo propio o compra (build vs buy), RAG, sistemas multiagente (LangGraph), elección de modelos y de alojamiento.
- **Producción medible**: evaluación de LLM (RAGAS), observabilidad, coste por equipo y por modelo, SLO de calidad y de latencia.
- **Gobernanza y cumplimiento normativo**: inventario de Shadow AI, trazabilidad y evidencias de auditoría frente al AI Act, ISO/IEC 42001 y NIST AI RMF, acceso controlado de los agentes de IA a las herramientas.
- **CAIO externo y formación**: hoja de ruta de IA, gestión del cambio, capacitación de equipos en Claude Code y sistemas agénticos.

## Preguntas frecuentes

**¿En qué está especializado Alexandre Beguel?**
En IA generativa en producción y sistemas agénticos. Cubre todo el recorrido, desde la definición del alcance hasta la operación: arquitectura, evaluación, observabilidad, control de costes y gobernanza de la IA.

**¿Cómo medir el coste de los LLM?**
Hay que partir de la telemetría que ya se emite y atribuir después el coste por equipo, modelo y proveedor. grafana-llmops-forge construye estos dashboards de FinOps de LLM en Grafana sin depender de un SDK de proveedor.

**¿Cómo detectar la IA en la sombra (Shadow AI) en una empresa?**
Hay que correlacionar señales de red, de endpoints y de identidad, y separar siempre la presencia del uso. open-shadow-ai lo hace de forma autoalojada, con un nivel de evidencia por hallazgo.

**¿Cómo preparar los sistemas de IA generativa para el AI Act?**
Lo primero es reunir las evidencias: inventario de IA, continuidad de los registros, avisos de transparencia y seguimiento de incidentes. Las obligaciones de transparencia del artículo 50 son aplicables desde el 2 de agosto de 2026. Con el ómnibus de IA (Reglamento (UE) 2026/1744), las obligaciones de alto riesgo del anexo III serán aplicables desde el 2 de diciembre de 2027.

**¿En qué idiomas trabaja?**
Trabaja en francés (nativo), inglés y español. Tiene su sede en París.

## Principios de trabajo

- Empezar por el problema, las restricciones y los modos de fallo.
- Tratar la evaluación y la observabilidad como requisitos de producto.
- Minimizar los privilegios y la exposición de datos; hacer explícitas las acciones con consecuencias.
- Preferir componentes simples y revisables, y una automatización medible.

## Herramientas y tecnologías

Un stack acotado para orquestación agéntica, evaluación, serving de modelos y operaciones cloud native.

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

## Contacto

[beguel.com](https://beguel.com/) · [LinkedIn](https://www.linkedin.com/in/beguel/) · [Malt](https://www.malt.fr/profile/alexandrebeguel) · [alebgl77.github.io](https://alebgl77.github.io/)

<sub>Alexandre Beguel · Arquitecto de IA agéntica y CAIO externo · París, Francia · Actualizado en octubre de 2026</sub>
