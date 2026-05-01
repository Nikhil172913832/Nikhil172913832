## Nikhil Arora

Building distributed systems and ML infrastructure — inference layers,
load balancing, fault-tolerant storage.

Pre-final year CS @ IIIT Una · DevOps Intern @ Equinix (2025) ·
Amazon ML Challenge — top 0.6% (27th / 4,500+)

---

### Projects

**LLM Inference Gateway** · [GitHub](https://github.com/Nikhil172913832/LLMInferenceGateway)
Stateless, horizontally scalable API gateway that streams token outputs via
SSE and routes across backend model servers using EWMA-scored latency with
per-node circuit breakers. Semantic cache built on FAISS — prompts within a
cosine similarity threshold are served from cache without a model call.
Full observability via Prometheus + Grafana.
`FastAPI` `FAISS` `Prometheus` `Grafana` `Docker` `SSE`

**Distributed Key-Value Store** · [GitHub](https://github.com/Nikhil172913832/DistributedKeyValueStore) · *in progress*
Multi-node KV store over HTTP with a consistent hash ring for key
distribution — node additions/removals only move keys in the affected arc.
Append-only WAL for crash recovery, primary-replica replication with
background liveness probing and automatic read failover.
`Python` `Flask` `Docker`

---

### Work

**Equinix — DevOps Engineer Intern** (May–Sep 2025, Bangalore)
Built a Bash health-check system with cron scheduling across production
servers; reduced incident detection from hours to under 15 minutes.
Engineered a Python alerting pipeline over existing dashboards that cut
MTTD for critical degradations from 45 minutes to under 2 minutes.
Refactored Jenkins CI/CD pipelines with pre-flight validation and automated
rollback; deployment failures dropped 25%.

---

### Open source

11 merged PRs across `psf/black`, `pact-python`, and `manim` —
bug fixes and code changes under active maintainer review.

---

### Stack

`Python` `Go` `Java` `FastAPI` `Redis` `PostgreSQL` `Docker` `Kubernetes`
`Prometheus` `FAISS` `PyTorch` `Jenkins` `AWS` `Linux`

---

### Currently

Working through Kubernetes internals (Gateway API, Envoy/Contour, CoreDNS)
and building the KV store toward full consensus.

---

[LinkedIn](https://linkedin.com/in/nikhil-arora-9642b4258) ·
[Email](mailto:nikhilarora13832@gmail.com) ·
[GitHub](https://github.com/Nikhil172913832)
