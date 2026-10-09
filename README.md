# Andrii Prisniak

Senior fullstack and backend engineer in Hamburg, Germany. I build TypeScript systems end to end (NestJS,
Next.js, React, Vue, PostgreSQL, AWS) and care most about the decisions that still hold up a year later.

## Experience at a glance

9+ years building production web systems in crypto, claims management and edtech. Before that, nine years of
third-line production support in banking, which is why I care about reliability, incident response and observability.

- Claims management: co-owned the architecture and delivery of a digital claims-reporting portal (NestJS,
  PostgreSQL, Vue 3 and Nuxt, 40+ backend modules, a shared component library) and its access control across API
  and UI: roles, feature flags and subscriptions.
- Cut AWS infrastructure costs by 25% through better provisioning and scaling, with observability across the stack
  (Sentry, CloudWatch, Prometheus, Grafana, PostHog).
- Reduced the OCR time per document from about 30 s to 10-15 s (up to 67%).
- Crypto exchange (15M+ registered users): designed and built three core NestJS microservices and cut the number of
  on-chain transactions per operation from 10-15 to 2-4.
- Edtech: grew from engineer to lead and architect of an in-house learning platform; led three client engagements,
  mentored client teams and trained three developer teams.

Production code is under NDA, so the public repositories below show how I think and build instead.

Languages: English, German, Ukrainian.

## Public work

| Project                                                                       | What it shows                                                                                                                                                                                                                                                                                                 |
| ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [kafka-pay-lab](https://github.com/sotream/kafka-pay-lab)                     | Event-driven payments: transactional outbox, consumer lag, retries, dead-letter topic, circuit breaker, realtime dashboard. NestJS, Next.js, Kafka, PostgreSQL.                                                                                                                                               |
| [nest-next-starter](https://github.com/sotream/nest-next-starter)             | Fullstack monorepo foundation: JWT with rotating refresh cookie, modular monolith, 9 ADRs, e2e tests on real Postgres and Redis, CI.                                                                                                                                                                          |
| [nest-next-aws-terraform](https://github.com/sotream/nest-next-aws-terraform) | Terraform on AWS for the starter: ECS Fargate, RDS, ElastiCache, ALB, GitHub OIDC CI/CD, ADRs and a cost estimate. Tested offline, not applied to a real account.                                                                                                                                             |
| [nuxt-flagboard](https://github.com/sotream/nuxt-flagboard)                   | Feature-flag service: NestJS API, Nuxt 4 admin UI with its own visual identity and self-hosted fonts, deterministic percentage rollouts, targeting rules, a readable audit log, live updates and a typed SDK. 13 ADRs, API tests on real PostgreSQL, browser tests with an accessibility scan in both themes. |
| [CodeSage](https://github.com/sotream/CodeSage)                               | RAG pipeline for questions about a codebase. Small modules, explicit trade-offs, ADRs. Python.                                                                                                                                                                                                                |

## How I work

- Write down decisions as ADRs, with the trade-offs I accepted.
- Test the behaviour, not only the types: e2e against real infrastructure where it matters.
- Use Claude Code daily, with rules, reviewers and a verify step; I make the design decisions and review the code.

## Stack

TypeScript, Node.js, NestJS, Next.js, React, Vue, PostgreSQL, Redis, Kafka, Docker, AWS, GitHub Actions. Terraform for AWS. Python for tooling.

## Contact

[LinkedIn](https://www.linkedin.com/in/andrii-prisniak)
