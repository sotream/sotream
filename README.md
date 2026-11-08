<h1 align="center">Andrii Prisniak</h1>

<p align="center">
  <b>Senior Software Engineer</b> · Backend focused, full-stack · Claims-management SaaS
</p>

<p align="center">
  <img alt="Open to Senior Backend / Full-Stack roles" src="https://img.shields.io/badge/Open%20to-Senior%20Backend%20%2F%20Full--Stack%20roles-2ea44f?style=flat-square">
  <img alt="Hamburg or remote in Germany" src="https://img.shields.io/badge/Hamburg-or%20remote%20in%20Germany-555?style=flat-square">
  <a href="https://www.linkedin.com/in/andrii-prisniak/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Andrii%20Prisniak-0A66C2?style=flat-square"></a>
</p>

<p align="center">
  <img alt="Node.js" src="https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white">
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white">
  <img alt="NestJS" src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white">
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white">
  <img alt="AWS" src="https://img.shields.io/badge/AWS-232F3E?style=flat-square">
  <img alt="Vue" src="https://img.shields.io/badge/Vue-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white">
  <img alt="React" src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB">
</p>

## What I'm looking for

A **Senior Software Engineer** role (backend, full-stack or product engineering) in a product company,
in Hamburg or remote within Germany.

I want the next role to make me a stronger engineer, not just give me a new title:

- **Distributed and event-driven systems:** data, consistency and reliability under real load. In production
  I built this at moderate scale; the labs below go further, and I want to go deeper on the job.
- **System-level decisions:** owning the design of services and the trade-offs behind them, and
  growing into broader architecture work as an individual contributor.
- **A strong team:** engineers I can learn from, honest code review, decisions written down.
- **Nice to have:** LLM features in the product, not only in my own workflow.

Fintech, insurtech and regulated domains are close to my experience, but the problem and the team
matter more to me than the domain.

## What I bring

9+ years of production web applications in claims management, crypto trading and online learning.
Before that, nine years of third-line production support at two banks in Ukraine (payment systems,
SWIFT, Bloomberg, Reuters): incident analysis, configuration and access rights on systems that must
not go down. That is where my habits around reliability and observability come from.

Backend first: **Node.js, TypeScript, NestJS, PostgreSQL**, with Vue and React frontends on AWS. I own features from the first
idea to the release and use AI-assisted, spec-driven development (Claude Code) every day.

| | Where | What |
| --- | --- | --- |
| **Claims-management SaaS** (insurtech) | TÜV NORD Group, product kaayo | Accident-claims SaaS for workshops, surveyors and lawyers. Shared responsibility for the architecture; I own several backend modules end to end, including a two-way CRM sync (Pipedrive) and a lawyer-service integration (an export that locks the case, with payments and statuses coming back over webhooks). @mentions and in-app notifications: my design and specification, code written by Claude Code, then team review. Keycloak login and role- and subscription-based access across API and UI. In a team of five: an LLM-based OCR pipeline (PaddleOCR + Mistral), from ~30 s to 10-15 s per document. Cut AWS costs by 25% myself in Terraform, with one shared load balancer per account and removal of unused resources. Observability with Sentry, CloudWatch and Grafana. |
| **Crypto exchange** | CEX.IO | Two core services, Price Alerts (NestJS, PostgreSQL, Redis, Kubernetes) and Staking/Savings (Node.js), plus an internal admin app. Price Alerts: matching on candle high/low, instances share the work through Postgres row locks (`SKIP LOCKED`) with no broker, at-least-once delivery. Cut internal ledger entries per order or transfer from 10-15 to 2-4. Fixed unbounded memory growth in a service, found through Grafana. |
| **Online learning** | Lectrum | Grew from engineer to architecture lead; architecture and core of an in-house LMS on Kubernetes, GraphQL API; mentored three client developer teams at a major internet provider. |

Production code is under NDA, so the repositories below show how I think and build.

## Projects

| Project | What it shows |
| --- | --- |
| [**boxoffice-lab**](https://github.com/sotream/boxoffice-lab) | Design playbook for workload-driven architecture: a ticket flash sale across six NestJS/Fastify services, capacity formulas, 17 ADRs, k6-measured numbers, failure drills, and invariant tests (no seat sold twice, no double charge) that survive `kill -9`. PostgreSQL, Redis, Redpanda (Kafka API). |
| [**Kafka Pay Lab**](https://github.com/sotream/kafka-pay-lab) | Transactional outbox, idempotency keys, circuit breaker, retries, dead-letter topic, OpenTelemetry tracing in Grafana. NestJS, Next.js, Kafka. |
| [**Access Control Lab**](https://github.com/sotream/access-control-lab) | OIDC + PKCE on Keycloak, RBAC + ABAC, Postgres row-level security, tamper-evident audit log, 63 attack tests. NestJS, Next.js. |
| [**Flagboard**](https://github.com/sotream/nuxt-flagboard) | Feature-flag service: percentage rollouts, targeting rules, audit log, typed SDK. NestJS, Nuxt 4, PostgreSQL. |
| [**normkompass**](https://github.com/sotream/normkompass) | RAG over German federal law that answers only with citations checked in code, or refuses. Hybrid search (pgvector + full-text) with a published retrieval eval. NestJS, PostgreSQL. |

All five are side projects, not production systems.

Also public: [nest-next-starter](https://github.com/sotream/nest-next-starter) (fullstack monorepo foundation)
and [nest-next-aws-cdk](https://github.com/sotream/nest-next-aws-cdk) (AWS CDK deployment of it on ECS Fargate).

## Working with AI agents

The projects above were built with Claude Code under my review: spec first, small tasks with tests,
one commit per task, then CI and my own review. Design decisions are written down as ADRs.

## Stack

| Area | Technologies |
| --- | --- |
| **Backend** | Node.js, TypeScript, NestJS, REST, GraphQL, WebSocket, microservices, Keycloak, OAuth 2.0 / OIDC |
| **Frontend** | Vue 3, Nuxt, React, Next.js, TanStack Query, Tailwind CSS |
| **Data** | PostgreSQL, Redis, MongoDB, RabbitMQ, Bull. Kafka and pgvector in side projects |
| **AI** | LLM-based document processing (Mistral) in production; RAG in a side project; Claude Code daily |
| **Infrastructure** | AWS (ECS, RDS, S3), Docker, Kubernetes, Terraform, AWS CDK, GitHub Actions |
| **Quality and observability** | Jest, Playwright, JMeter, Sentry, Grafana. OpenTelemetry and Prometheus in side projects |
