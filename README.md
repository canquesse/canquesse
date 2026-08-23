## Can Kara

Computer Science B.Sc. at the University of Bremen. I work on the engineering side of
AI systems rather than the research side: the services around a model, the code that
calls it, and the tests that tell you whether a change actually helped.

<p>
  <a href="https://canquesse.com"><img src="https://img.shields.io/badge/canquesse.com-141412?style=flat-square&logo=cloudflare&logoColor=F38020" alt="Website" /></a>
  <a href="https://www.linkedin.com/in/canquesse"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:canhuseyinkara@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

---

### What I work on

**LLM application engineering.** Multi-step, tool-calling agent loops against
OpenAI-compatible APIs. Typed tool registries, bounded step budgets, timeouts, retries,
and failure paths that stay predictable when a model or a dependency misbehaves.

**Retrieval.** Deterministic chunking, embedding pipelines, and vector search in
PostgreSQL with pgvector.

**Backend services.** REST APIs in Java 21 / Spring Boot and Python 3.11 / FastAPI,
relational schema design with versioned migrations, and contract-first service
boundaries that are tested rather than assumed.

**Observability and evaluation.** Distributed tracing with W3C trace context, structured
JSON logging keyed by trace id, and evaluation harnesses that run offline and
deterministically so they cost nothing in CI.

**Infrastructure.** Docker Compose stacks, GitHub Actions pipelines, self-hosted
inference on Linux, and private networking with Tailscale.

---

### Public projects

| Project | What it does | Stack |
|---|---|---|
| [MedRadar](https://github.com/canquesse/MedRadar) | Scans medical sources across languages and summarizes them | JavaScript, LLM APIs |
| [canquesse-web](https://github.com/canquesse/canquesse-web) | canquesse.com — statically exported, no server, no runtime attack surface | Next.js, React, TypeScript, Cloudflare |
| [character-skipper](https://github.com/canquesse/character-skipper) | Browser extension that recognizes faces on-device and skips scenes as they play | JavaScript, face embeddings |
| [machine_learning](https://github.com/canquesse/machine_learning) | Classical ML on real datasets | Python, Jupyter, scikit-learn |
| [StockAnalyzerApp](https://github.com/canquesse/StockAnalyzerApp) | Desktop stock analysis tool with ten technical indicators | Java, JavaFX |

---

### Tools

**AI/ML**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![llama.cpp](https://img.shields.io/badge/llama.cpp-2C2C2C?style=flat-square)
![OpenAI-compatible](https://img.shields.io/badge/OpenAI--compatible%20API-412991?style=flat-square)
![pgvector](https://img.shields.io/badge/RAG%20%2F%20pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)

**Backend**

![Java](https://img.shields.io/badge/Java%2021-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![OpenAPI](https://img.shields.io/badge/OpenAPI-6BA539?style=flat-square&logo=openapiinitiative&logoColor=white)

**Frontend**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)

**Infrastructure**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Tailscale](https://img.shields.io/badge/Tailscale-242424?style=flat-square&logo=tailscale&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)

**From coursework**

![Haskell](https://img.shields.io/badge/Haskell-5D4F85?style=flat-square&logo=haskell&logoColor=white)
![Racket](https://img.shields.io/badge/Racket-9F1D20?style=flat-square&logo=racket&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)

---

### Home lab

I run my own inference box: llama.cpp serving an open-weight model behind an
OpenAI-compatible endpoint on a private network, with a separate worker for embeddings.
It means I can build and test against a real model at no API cost and without sending
data anywhere, while CI keeps a deterministic offline fake as the default.

---

Open to AI/ML engineering internships and working-student positions in Germany.
Most of what I work on daily lives in private repositories, so the contribution graph
here is only part of it.
