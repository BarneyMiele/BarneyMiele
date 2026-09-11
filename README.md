I build ingestion and reconciliation systems for payments, with a focus on durable queues, idempotent APIs, and schema evolution.
I own the boundaries between APIs, workers, and downstream ledgers, including failure modes that matter during an incident.
Operational priorities are bounded queues, traceable events, and migrations that can be replayed without guessing.
I accept duplicated state when it buys recoverability, but only behind explicit contracts and reconciliation jobs.

### 🛠 Tech & Infrastructure
- **Core:** TypeScript, Node.js, REST, gRPC, OpenAPI
- **Data:** PostgreSQL, Redis, Kafka
- **Infra:** Kubernetes, Terraform, OpenTelemetry
- **Tooling:** Jest, pino, npm

### ⚙️ Engineering Areas
- Designing idempotent payment APIs with stable request identifiers and ordered event streams.
- Building Kafka-backed workers that isolate poison events without dropping business events.
- Managing PostgreSQL migrations, indexes, and read replicas for schema-compatible deploys.
- Adding distributed traces across RPCs, queues, and ledger reconciliation jobs.

### 🔭 Current Focus
- Moving a legacy batch settlement into a checkpointed worker while keeping replayable outbox events.
- Reconciling PostgreSQL balances with queue offsets and downstream bank confirmations.
- Choosing a bounded retry policy that limits duplicate charges without hiding failed payments.
- Reducing cache staleness for payment status reads at the cost of extra invalidation paths.

### 📌 Engineering Notes
- Tests should cover delivery boundaries, not only happy-path unit behaviour.
- Public schemas and queue envelopes need versioned contracts with compatibility checks.
- Migrations should be reversible or replayable before the old path is removed.
- Retries need an explicit budget; retries without bounds become load generators.

### 🧭 How I Work
- Keep the failure path visible: every queue, RPC, and cache miss has an owner and a trace.
- Prefer a conservative deploy behind a feature flag over an unmeasured cutover.
- Prefer boring, boring components with clear recovery procedures over clever ones.

*I make failure modes explicit and keep recovery boring.*

[Email](mailto:barneymiele9402@hotmail.com)