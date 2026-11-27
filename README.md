# Senior Engineering Knowledge Base

Techniczne kompendium dla Senior Full-Stack Engineer: mechanizmy, granice, failure modes, trade-offs i przykłady. Bez pytań rekrutacyjnych.

## Start lokalnie

```bash
git clone https://github.com/Kine91/knowledge-base.git
cd knowledge-base
# otwórz index.html w przeglądarce lub:
python -m http.server 8000
```

Strony działają lokalnie bez bundlera. GitHub pokazuje źródło HTML, nie renderuje strony.

## Rozdziały

- [AWS — architektura](aws.html) — Dobór usług, koszty, IaC, availability
- [Lambda](lambda.html) — Lifecycle, cold/warm, concurrency, limits
- [API Gateway](api-gateway.html) — Ingress, quotas, JWT, timeout
- [ECS / Fargate / EC2](compute.html) — Task lifecycle, deployment, autoscaling
- [SQS / SNS / EventBridge](messaging.html) — Delivery, batching, retry, outbox, Step Functions
- [S3](s3.html) — Consistency, multipart, security, events
- [IAM / VPC / RDS](aws-security.html) — Policies, STS, routing, secrets, failover
- [Mikroserwisy / system design](architecture.html) — Consistency, saga, capacity, resilience, CQRS
- [Backend API](backend-api.html) — HTTP, gRPC, WebSocket, auth, idempotency
- [PostgreSQL](postgres.html) — MVCC, WAL, isolation, locks, tuning, pooling
- [DynamoDB / Redis / Kafka](data-messaging.html) — Partitioning, cache, offsets, delivery
- [Node.js / runtime](node-typescript.html) — Event loop, libuv, streams, GC, NestJS
- [TypeScript](typescript.html) — Variance, generics, conditional types, modules
- [React / frontend](react.html) — Fiber, scheduling, effects, state, SSR, performance
- [Clean Code / Design Patterns](patterns.html) — SOLID, DDD, architecture, review
- [SAP integration](sap.html) — Protocols, consistency, reconciliation, mapping
- [Testowanie](testing.html) — Integration, contract, E2E, concurrency, performance
- [Observability / SRE](operations.html) — SLO, tracing, diagnostics, incident runbooks
- [Case study: system zamówień](interview.html) — Referencyjny system end-to-end i awarie

## Standard rozbudowy

- Mechanika, konsekwencje, edge cases, scenariusze awarii, diagnostyka, trade-offs.
- Przykłady kodu z jawnymi założeniami; nie wszystkie są gotowymi programami.
- Limity AWS weryfikuj w aktualnych docs i Service Quotas dla konta/Regionu.
- Jeden wspólny stylesheet, nawigacja i spis treści. Bez quizów i podstawowych definicji.
- Plik interview.html zachowuje adres historyczny; zawiera techniczny case study.
