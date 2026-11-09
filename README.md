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
  I worked with parts of this at small scale: several instances sharing work, at-least-once delivery,
  cache invalidation. The labs below go further, and I want to go deeper on the job.
- **System-level decisions:** owning the design of services and the trade-offs behind them, and
  growing into broader architecture work as an individual contributor.
- **A strong team:** engineers I can learn from, honest code review, decisions written down.
- **Nice to have:** LLM features in the product, not only in my own workflow.

Fintech, claims handling and regulated domains are close to my experience, but the problem and the team
matter more to me than the domain.

## What I bring

9+ years of production web applications in claims management, crypto trading and online learning.
Before that, nine years of third-line production support at two banks in Ukraine (payment systems,
SWIFT, Bloomberg, Reuters): incident analysis, configuration and access rights on systems that must
not go down. That is where my habits around reliability and observability come from.

Backend first: **Node.js, TypeScript, NestJS, PostgreSQL**, with Vue and React on the frontend, running on AWS.
I take features from the first idea to production: design, backend, frontend, and monitoring after the
release. I work spec-first with Claude Code, and every change still goes through code review.

| | Where | What |
| --- | --- | --- |
| **Claims-management SaaS** (automotive) | TÜV NORD Group, product kaayo | Damage-claims SaaS for workshops, surveyors and lawyers. Shared responsibility for the architecture; I own several backend modules end to end. Two-way CRM sync (Pipedrive): sales no longer enter changes twice. Lawyer-service integration: a manual export that locks the case, with document and client-card updates coming back over signed webhooks. In-app notifications after lawyers missed emails the provider reported as delivered (my design and specification, code written by Claude Code): no further complaints after release. In a team of five: LLM-based OCR, from ~30 s to 10-15 s per document. Cut AWS costs by 25% myself in Terraform. |
| **Crypto exchange** | CEX.IO | Two services I built and owned, Price Alerts (NestJS, PostgreSQL, Redis, Kubernetes) and Staking/Savings (Node.js), plus an internal admin app. Price Alerts: matching on candle high/low, instances share the work through Postgres row locks (`SKIP LOCKED`) with no broker, at-least-once delivery. Cut internal ledger entries per order or transfer from 10-15 to 2-4. Fixed unbounded memory growth in Staking, found through Grafana (24 h TTL, 1,000-entry cap, RabbitMQ invalidation): restarts stopped. |
| **Online learning** | Lectrum | Software engineer, promoted to Lead Software Engineer in 2020. Owned the architecture of the in-house LMS core and set up its Kubernetes cluster; GraphQL API. Mentored three client developer teams at a major internet provider. |

Production code is under NDA, so the repositories below show how I think and build.

## Projects

Start with evcharge-lab: its README maps [each service to the system-design question it answers](https://github.com/sotream/evcharge-lab#the-system-design-question-each-service-answers) and lists the [distributed-systems guarantees](https://github.com/sotream/evcharge-lab#distributed-systems-guarantees) with the drill that tests each one.

| Project | What it shows |
| --- | --- |
| [**evcharge-lab**](https://github.com/sotream/evcharge-lab) | EV charging platform (charge point operator side) as a system-design lab: seven NestJS and Go services, an OCPP WebSocket gateway driven by a station simulator, Kafka in KRaft mode (3 brokers), TimescaleDB, a Postgres read replica with read-your-writes by LSN. 18 ADRs against an explicit load model and SLOs; failure drills with saved raw output (broker loss, KRaft quorum loss, replica lag, reconnect storm, offline replay); missed targets stay visible as missed. NestJS, Go, PostgreSQL, Kafka, Redis. |
| [**boxoffice-lab**](https://github.com/sotream/boxoffice-lab) | Design playbook for workload-driven architecture: a ticket flash sale across six NestJS/Fastify services, capacity formulas, 17 ADRs, k6-measured numbers, failure drills, and invariant tests (no seat sold twice, no double charge) that survive `kill -9`. PostgreSQL, Redis, Redpanda (Kafka API). |
| [**Kafka Pay Lab**](https://github.com/sotream/kafka-pay-lab) | Transactional outbox, idempotency keys, circuit breaker, retries, dead-letter topic, OpenTelemetry tracing in Grafana. NestJS, Next.js, Kafka. |
| [**Access Control Lab**](https://github.com/sotream/access-control-lab) | OIDC + PKCE on Keycloak, RBAC + ABAC, Postgres row-level security, tamper-evident audit log, 63 attack tests. NestJS, Next.js. |
| [**Flagboard**](https://github.com/sotream/nuxt-flagboard) | Feature-flag service: percentage rollouts, targeting rules, audit log, typed SDK. NestJS, Nuxt 4, PostgreSQL. |
| [**normkompass**](https://github.com/sotream/normkompass) | RAG over German federal law that answers only with citations checked in code, or refuses. Hybrid search (pgvector + full-text) with a published retrieval eval. NestJS, PostgreSQL. |

All six are side projects, not production systems.

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
| **Infrastructure** | AWS (ECS, RDS, S3), Docker, Kubernetes, Terraform, GitHub Actions; AWS CDK in a side project |
| **Quality and observability** | Jest, Playwright, JMeter, Sentry, Grafana. OpenTelemetry and Prometheus in side projects |
