## Nikhil Arora

I build low-latency inference and distributed systems infrastructure —
routing, caching, fault isolation.

Pre-final year CS @ IIIT Una · DevOps Intern @ Equinix (2025) ·
Amazon ML Challenge — top 0.6% (27th / 4,500+)

---

### Projects

**[LLM Inference Gateway](https://github.com/Nikhil172913832/LLMInferenceGateway)**

Stateless gateway that proxies streaming LLM responses across multiple
backends. Routes via Envoy's Peak EWMA, prioritizing low-latency backends
and quickly isolating degraded nodes.

Semantic cache: FAISS vector similarity over an exact-match layer — serves
repeated and near-identical prompts without a model call. FAISS doesn't
support deletion, so invalidation uses an ID→metadata map with background
index rebuilds. Embeddings run in `run_in_executor` to avoid blocking the
async loop under concurrency. Circuit breaker state is per-replica —
replicas may disagree on backend health based on individually observed
network paths.

Full observability: Prometheus metrics on latency, error rates, and
per-backend EWMA scores, surfaced in Grafana.

`FastAPI` `FAISS` `Prometheus` `Grafana` `Docker` `SSE`

---

**[Distributed Key-Value Store](https://github.com/Nikhil172913832/DistributedKeyValueStore)**
*in active development*

Multi-node KV store with consistent hash ring partitioning — ring
membership changes move only keys in the affected arc. WAL-first writes
ensure nodes replay to a consistent state on crash recovery before serving
traffic. Primary-replica replication with background liveness probing;
replica reads tolerate primary failure without client-visible downtime.

`Python` `Flask` `Docker`

---

### Work

**Equinix — DevOps Engineer Intern** (May–Sep 2025, Bangalore)
Designed a distributed health-check system (cron-based, Bash) reducing
incident detection from hours to under 15 minutes. Built a Python alerting
pipeline over existing dashboards that cut MTTD for critical degradations
from 45 min to under 2 min. Refactored Jenkins pipelines with pre-flight
validation and automated rollback — deployment failures down 25%.

---

### Open source — 11 merged PRs

`psf/black` — AST traversal edge cases and syntax compatibility fixes.
Black runs on hundreds of thousands of Python projects; review bar is high.

`pact-python` — pytest integration fixes in a consumer-driven contract
testing library.

`manim` — rendering pipeline bug fixes.

---

### Stack

**Projects:** Python · FastAPI · FAISS · Prometheus · PostgreSQL · Docker · Linux

**Production (Equinix):** Kubernetes · Jenkins · Bash · AWS

**Familiar:** PyTorch · Go · Java

---

### Currently

Replacing the KV store's static cluster config with gossip-based node
discovery — nodes currently need full peer lists at startup.

---

[LinkedIn](https://linkedin.com/in/nikhil-arora-9642b4258) ·
[Email](mailto:nikhilarora13832@gmail.com) ·
[GitHub](https://github.com/Nikhil172913832)
