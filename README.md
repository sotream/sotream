<h1 align="center">Andrii Prisniak</h1>

<p align="center">
  <b>Senior Software Engineer</b> · Fullstack, backend focused<br>
  Hamburg, Germany · <a href="https://www.linkedin.com/in/andrii-prisniak/">LinkedIn</a>
</p>

Backend first: **Node.js, TypeScript, NestJS, PostgreSQL**, with Vue and React frontends and AWS infrastructure.
9+ years of production web applications in claims management, crypto trading and online learning, after almost nine
years of third-line production support in banking. I own features from the first idea to release and use AI
tools (Claude Code) in everyday engineering.

## What I have built

| | Where | What |
| --- | --- | --- |
| **Claims management** | TÜV NORD Group, product kaayo | Backend modules end to end (third-party integrations, mentions, notes), Keycloak login and role- and subscription-based access across API and UI, OCR pipeline sped up from ~30 s to 10-15 s per document, AWS costs cut by 25% with Terraform, observability with Sentry, CloudWatch and Grafana. |
| **Crypto exchange** | CEX.IO | Two core services, Price Alerts (NestJS, PostgreSQL, Redis, Kubernetes) and Staking/Savings (Node.js), plus an internal admin app. Cut internal ledger entries per order or transfer from 10-15 to 2-4. Fixed unbounded memory growth in a service found through Grafana. |
| **Online learning** | Lectrum | Grew from engineer to lead; architecture and core of an in-house LMS on Kubernetes; mentored three client developer teams at a major internet provider. |

Production code is under NDA, so the repositories below show how I think and build.

## Projects

| Project | What it shows | Status |
| --- | --- | --- |
| [**Access Control Lab**](https://github.com/sotream/access-control-lab) | OIDC + PKCE on Keycloak, RBAC + ABAC, Postgres row-level security, tamper-evident audit log, 63 attack tests. NestJS, Next.js. | Lab project, not production |
| [**Kafka Pay Lab**](https://github.com/sotream/kafka-pay-lab) | Transactional outbox, idempotency keys, circuit breaker, retries, dead-letter topic, consumer-lag dashboard, OpenTelemetry tracing in Grafana. NestJS, Next.js, Kafka. | Lab project, not production |
| [**Flagboard**](https://github.com/sotream/nuxt-flagboard) | Feature-flag service: percentage rollouts, targeting rules, audit log, typed SDK. NestJS, Nuxt 4, PostgreSQL. | Portfolio project, not deployed |
| [**normkompass**](https://github.com/sotream/normkompass) | RAG with verifiable citations over German federal law: every answer cites the exact passage (for example "§ 14 Abs. 1 UStG") or refuses. Citation quotes are checked in code against the retrieved text. Hybrid search (pgvector + full-text) with a published retrieval eval, including its weak spots. Written by Claude under my review with spec-driven development (OpenSpec), decisions in ADRs. TypeScript, NestJS, PostgreSQL. | Reference implementation, not a finished product |
| **Agent Lab** | Agent loop with an MCP server and client, a per-tool trust policy, opt-in writes and its own agent evals. | Private, code on request |

Also public: [nest-next-starter](https://github.com/sotream/nest-next-starter) (fullstack monorepo foundation)
and [nest-next-aws-cdk](https://github.com/sotream/nest-next-aws-cdk) (AWS CDK deployment of it on ECS Fargate).

## Working with AI agents

The projects above were built with AI assistance (Claude Code): spec first, small tasks with tests, one commit per
task, then CI and my own review. Design decisions are written down as ADRs where available.

## Stack

| | |
| --- | --- |
| **Backend** | Node.js, NestJS, REST, GraphQL, WebSocket, Keycloak, OAuth 2.0 / OIDC |
| **Frontend** | Vue 3, Nuxt, React, Next.js, TanStack Query, Tailwind CSS |
| **Data** | PostgreSQL, Redis, MongoDB, RabbitMQ, Bull. Kafka in side projects |
| **Infrastructure** | AWS (ECS, RDS, S3), Docker, Kubernetes, Terraform, AWS CDK, GitHub Actions |
| **Quality and observability** | Jest, Playwright, JMeter, Sentry, Grafana. OpenTelemetry and Prometheus in side projects |
