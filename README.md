## Can Kara

Computer Science B.Sc. at the University of Bremen. I work on the engineering side of
AI systems: agent runtimes, tool-call permissions, and evaluation.

<p>
  <a href="https://canquesse.com"><img src="https://img.shields.io/badge/canquesse.com-141412?style=flat-square&logo=cloudflare&logoColor=F38020" alt="Website" /></a>
  <a href="https://www.linkedin.com/in/h%C3%BCseyin-can-kara-9a717919b/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:canhuseyinkara@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

---

### Cautrum

Most of my time goes into Cautrum, a two-service agent platform I build with one
co-maintainer over a six-month program. The idea is narrow on purpose: an agent's tool
permissions are enforced in a process that contains no LLM, and every allow/deny decision
is written next to the run's steps so it becomes eval data instead of a log line.

The repository is private, so here is the shape of it.

| | |
|---|---|
| **control-plane** — Java 21, Spring Boot | REST API, task orchestration, JPA/Flyway over PostgreSQL + pgvector, and the policy gate. No model runs here. |
| **agent-runtime** — Python 3.11, FastAPI | Bounded multi-step tool-calling loop, tenant-scoped RAG with exact cosine over `vector(1024)`, and a fail-closed permission client on the only tool-execution path. |

Working today: W3C trace context across both services, a contract-tested service boundary,
policy enforcement with a hard timeout and one retry, detection of tool calls that have no
matching decision, a secret-free Docker Compose end-to-end proof, a deterministic eval
runner that needs no API key, versioned system-prompt comparison, and a React evidence
console. One measured result worth keeping: an index check showed the existing schema was
already ~138× faster than the no-index baseline, which killed a migration I had planned.

Not built yet: repeated-run datasets, the bootstrap that turns them into a noise band, and
the CI eval gate that stays green when a difference sits inside run-to-run variance. Those
are the next three months, and I would rather say so than imply otherwise.

`Java 21` · `Spring Boot` · `Python 3.11` · `FastAPI` · `PostgreSQL` · `pgvector` · `Flyway` · `Docker Compose` · `React 19` · `GitHub Actions`

---

### Other things I have built

| Project | What it does | Stack |
|---|---|---|
| [MedRadar](https://github.com/canquesse/MedRadar) | Scans medical sources across languages and summarizes them | JavaScript, LLM APIs |
| [canquesse-web](https://github.com/canquesse/canquesse-web) | canquesse.com — statically exported, no server, no runtime attack surface | Next.js 16, React 19, TypeScript, Cloudflare |
| [character-skipper](https://github.com/canquesse/character-skipper) | Browser extension that recognizes faces on-device and skips scenes as they play | JavaScript, face embeddings |
| Fallnn | Photo in, exact product out, with visually similar fallbacks when there is no exact match | Expo, Node, Gemini, Serper |
| similarity_ai | Face similarity: RetinaFace alignment, ArcFace 512-d embeddings, cosine distance calibrated to a readable score | Python, InsightFace |
| [machine_learning](https://github.com/canquesse/machine_learning) | Classical ML on real datasets, from the coursework end | Python, Jupyter, scikit-learn |

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
![React](https://img.shields.io/badge/React%2019-61DAFB?style=flat-square&logo=react&logoColor=black)
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

An always-on Ubuntu box runs llama.cpp with Qwen behind an OpenAI-compatible endpoint,
reachable only over a private Tailscale network, plus a separate authenticated worker for
embeddings. Everything I build can be run against a real model at no API cost and without
data leaving the network. CI keeps a deterministic fake as the default, so a pull request
never needs a credential.

---

Open to AI/ML engineering internships and working-student positions in Germany.
Most of what I work on daily lives in private repositories, so the contribution graph
here is only part of it.
