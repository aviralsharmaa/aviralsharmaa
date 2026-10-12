<!-- ─────────────────────────────  HEADER  ───────────────────────────── -->
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:0e75b6,100:6e40c9&height=190&section=header&text=Aviral%20Sharma&fontSize=58&fontColor=ffffff&fontAlignY=36&desc=AI%20Engineer%20%E2%80%A2%20Agentic%20Systems%20%E2%80%A2%20LLM%20Infrastructure%20%E2%80%A2%20MLOps&descAlignY=58&descSize=17&animation=fadeIn" width="100%" alt="Aviral Sharma — AI Engineer" />

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=18&duration=2800&pause=900&color=0E75B6&center=true&vCenter=true&width=640&lines=%24+agent.run(perceive+%E2%86%92+plan+%E2%86%92+act+%E2%86%92+reflect);Stateful+LangGraph+agents+in+production;Air-gapped%2C+open-weight+LLM+serving+for+regulated+BFSI;RAG+%C2%B7+tool-calling+%C2%B7+evals+%C2%B7+observability" alt="Typing SVG" /></a>

<p>
  <a href="https://www.linkedin.com/in/aviral31/"><img src="https://img.shields.io/badge/LinkedIn-aviral31-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://x.com/aviralsharma_"><img src="https://img.shields.io/badge/X-@aviralsharma__-000000?style=for-the-badge&logo=x&logoColor=white" alt="X" /></a>
  <a href="mailto:aviralsharma5531@gmail.com"><img src="https://img.shields.io/badge/Email-aviralsharma5531-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <img src="https://komarev.com/ghpvc/?username=aviralsharmaa&label=VIEWS&color=0e75b6&style=for-the-badge" alt="Profile views" />
</p>

</div>

---

### `$ whoami`

```python
from dataclasses import dataclass, field

@dataclass(frozen=True)
class Engineer:
    name:     str = "Aviral Sharma"
    role:     str = "AI Engineer @ OnFinance AI"
    location: str = "Bengaluru, IN"
    edu:      str = "B.Tech, Information Technology — ABESIT ('24)"

    focus: tuple = (
        "Agentic systems  → stateful graphs, tool-calling, planning, memory",
        "LLM infra        → gateways, routing, self-hosted open-weight models",
        "Retrieval        → hybrid RAG, embeddings, rerankers, evals",
        "MLOps            → reproducible pipelines, tracking, drift, CI/CD",
    )

    now: tuple = (
        "Shipping an LLM-native compliance OS for regulated BFSI institutions",
        "Multi-tenant, audit-grade platform with air-gapped model deployments",
        "Serving open-weight LLMs (Qwen, GPT-OSS) behind a unified LLM gateway",
    )

    principles: tuple = (
        "Deterministic orchestration around non-deterministic models",
        "If it isn't evaluated, it isn't shipped",
        "Observability first: every token traceable, every action auditable",
    )
```

---

### `$ cat architecture.md` — how I build agents

```mermaid
flowchart LR
    U([User / Event]) --> P[Perceive<br/><sub>parse · classify · retrieve</sub>]
    P --> PL{Plan<br/><sub>LLM router</sub>}
    PL -->|tool call| T[[Tools<br/><sub>APIs · DB · browser · ADB</sub>]]
    PL -->|retrieve| R[(Vector store<br/><sub>FAISS · Chroma</sub>)]
    T --> E[Execute]
    R --> E
    E --> V{Evaluate<br/><sub>guardrails · evals</sub>}
    V -->|fail / low confidence| PL
    V -->|pass| O([Response / Action])
    V -.-> M[(Memory<br/><sub>episodic · state</sub>)]
    M -.-> PL

    classDef node fill:#0d1117,stroke:#0e75b6,color:#c9d1d9;
    classDef store fill:#161b22,stroke:#6e40c9,color:#c9d1d9;
    class P,PL,T,E,V node;
    class R,M store;
```

---

### `$ ls ~/projects --featured`

<table>
<tr>
<td width="50%" valign="top">

#### 📈 [Autonomous Trading Agent](https://github.com/aviralsharmaa/Trading_agent)
Self-improving **LangGraph** agent with a 7-node stateful workflow:

`Fetch → Analyze → Plan → Simulate → Execute → Evaluate → Learn`

LLM-generated strategies over technical signals (RSI, MAs, volatility), backtested on historical data before paper execution via **Alpaca**. Post-trade evaluation feeds back into the planner.

<sub>`Python` `LangGraph` `Groq` `Ollama` `Alpaca` `FastAPI` `Streamlit`</sub>

</td>
<td width="50%" valign="top">

#### ♿ [WCAG Accessibility Agent](https://github.com/aviralsharmaa/web_wcag_agent)
Autonomous **WCAG 2.1** auditor. Bounded-BFS crawler (`max_depth`, `max_pages`) with **Playwright**, checkpoint evaluation orchestrated by **LangGraph** across 4 rule buckets, strict-policy verdicts and evidence artifacts (DOM snapshots, `scan-report.json`).
Mobile sibling: [wcag-app-agent](https://github.com/aviralsharmaa/wcag-app-agent) — FastAPI coordinator + worker CLI, Appium runtime, Langfuse tracing.

<sub>`Python` `LangGraph` `Playwright` `Appium` `FastAPI` `Langfuse`</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 📱 [Mobile Automation Agent](https://github.com/aviralsharmaa/mobile-automation-agent)
Voice-driven agent that operates Android devices for blind users. **STT → GPT-4o vision** screen grounding → action planning → **ADB** execution → **TTS** feedback, with popup/UI-drift recovery and secure credential handling.

<sub>`Python` `GPT-4o Vision` `ADB` `Speech I/O`</sub>

</td>
<td width="50%" valign="top">

#### 🔍 Vision Authentication Agents — *production*
QR + copy-detection-pattern (CDP) product authentication using **Vision Transformers** and contrastive learning. **97.9%** verification accuracy, automated data curation, **MLflow** tracking, **Airflow** orchestration, served on **SageMaker** with Docker/K8s and Grafana monitoring.

<sub>`PyTorch` `ViT` `OpenCV` `MLflow` `Airflow` `SageMaker` `K8s`</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 📚 [AI Research Agent](https://github.com/aviralsharmaa/AI_research_agent)
RAG pipeline over research PDFs: chunking → **Sentence-Transformers** embeddings → **FAISS/ChromaDB** retrieval → LangGraph agent for QA, summarisation and query-match verdicts.

<sub>`LangChain` `LangGraph` `FAISS` `ChromaDB` `Llama 3.3`</sub>

</td>
<td width="50%" valign="top">

#### ✉️ [AI Email Agent](https://github.com/aviralsharmaa/job-mailer)
Natural-language → workflow: `"send a mail to microsoft"` resolves intent, discovers domain-matched recipients, composes and dispatches via **Gmail API (OAuth 2.0)** with attachment support. CLI + Streamlit front-ends.

<sub>`Python` `NLP` `Gmail API` `OAuth 2.0` `Streamlit`</sub>

</td>
</tr>
</table>

---

### `$ cat stack.yaml`

```yaml
llm_and_agents:  [LangGraph, LangChain, OpenAI, Groq, Ollama, HuggingFace, Langfuse]
patterns:        [tool-calling, structured-output, RAG, multi-agent, reflection, guardrails, LLM-as-judge]
ml_dl:           [PyTorch, TensorFlow, scikit-learn, Vision Transformers, contrastive learning, time-series]
retrieval:       [FAISS, ChromaDB, Sentence-Transformers, embeddings, semantic search]
mlops:           [MLflow, Airflow, Docker, Kubernetes, GitHub Actions, Grafana]
cloud:           [AWS: {SageMaker, EKS, Lambda, EC2, S3, CloudWatch}, GCP: {Cloud Run, Artifact Registry, GCS}]
backend:         [FastAPI, Flask, REST, OAuth2, InfluxDB, Playwright, Appium]
frontend_mobile: [TypeScript, Flutter/Dart, Kotlin, C/C++]
```

<div align="center">

<img src="https://skillicons.dev/icons?i=python,pytorch,tensorflow,sklearn,fastapi,flask,docker,kubernetes,aws,gcp,githubactions,grafana,linux&perline=13" alt="Core stack" />
<br/>
<img src="https://skillicons.dev/icons?i=ts,flutter,dart,kotlin,cpp,c,opencv,git,bash,vscode&perline=10" alt="Secondary stack" />

</div>

---

### `$ git log --stat --author=aviralsharmaa`

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=aviralsharmaa&show_icons=true&include_all_commits=true&count_private=true&hide_border=true&theme=github_dark&title_color=0e75b6&icon_color=6e40c9" alt="GitHub stats" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=aviralsharmaa&layout=compact&langs_count=8&hide_border=true&theme=github_dark&title_color=0e75b6" alt="Top languages" />


</div>

---

<div align="center">

<sub><code>while (true) { perceive(); reason(); act(); learn(); }</code></sub>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:6e40c9,50:0e75b6,100:0d1117&height=110&section=footer" width="100%" alt="" />

</div>
