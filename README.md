# Andrii Prisniak

Senior fullstack and backend engineer in Hamburg, Germany. I build TypeScript systems end to end (NestJS, Next.js,
Nuxt, React, Vue, PostgreSQL, AWS) and care most about the decisions that still hold up a year later. I own features
from idea to production: shaping the problem, design, implementation, tests, CI and release, and observability once
it is live.

## Experience at a glance

9+ years building production web systems in crypto, claims management and edtech. Before that, nine years of
third-line production support in banking, which is why I care about reliability, incident response and observability.

- Claims management: co-owned the architecture and delivery of a digital claims-reporting portal (NestJS,
  PostgreSQL, Vue 3 and Nuxt, 40+ backend modules, a shared component library) and its access control across API
  and UI: roles, feature flags and subscriptions.
- Cut AWS infrastructure costs by 25% through better provisioning and scaling.
- Built observability across the stack: Sentry, CloudWatch, Prometheus, Grafana and PostHog.
- Reduced the document recognition time (OCR) from about 30 s to 10-15 s per document (up to 67%).
- Crypto exchange (15M+ registered users): designed and built three core NestJS microservices. Optimised transaction
  compression, so one operation now needs 2-4 on-chain transactions instead of 10-15, which lowered infrastructure and
  network costs.
- Edtech: grew from engineer to lead and architect of an in-house learning platform; led three client engagements,
  mentored client teams and trained three developer teams.

Production code is under NDA, so the public repositories below show how I think and build instead.

Languages: English, German, Ukrainian.

## Public work

| Project                                                                       | What it shows                                                                                                                                                                                                                                                                                                 |
| ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [kafka-pay-lab](https://github.com/sotream/kafka-pay-lab)                     | Event-driven payments: transactional outbox, consumer lag, retries, dead-letter topic, circuit breaker, realtime dashboard. One payment traced end to end with OpenTelemetry, Prometheus and Grafana. NestJS, Next.js, Kafka, PostgreSQL.                                                                     |
| [nest-next-starter](https://github.com/sotream/nest-next-starter)             | Fullstack monorepo foundation: JWT with rotating refresh cookie, modular monolith, 9 ADRs, e2e tests on real Postgres and Redis, CI.                                                                                                                                                                          |
| [nest-next-aws-terraform](https://github.com/sotream/nest-next-aws-terraform) | Terraform on AWS for the starter: ECS Fargate, RDS, ElastiCache, ALB, GitHub OIDC CI/CD, ADRs and a cost estimate. Tested offline, not applied to a real account.                                                                                                                                             |
| [nuxt-flagboard](https://github.com/sotream/nuxt-flagboard)                   | Feature-flag service: NestJS API, Nuxt 4 admin UI with its own visual identity and self-hosted fonts, deterministic percentage rollouts, targeting rules, a readable audit log, live updates and a typed SDK. 13 ADRs, API tests on real PostgreSQL, browser tests with an accessibility scan in both themes. |
| [CodeSage](https://github.com/sotream/CodeSage)                               | RAG pipeline for questions about a codebase, with a measured retrieval eval (hit-rate@k, MRR) and incremental indexing. Small modules, explicit trade-offs, ADRs. Python.                                                                                                                                     |

## How I work

- Start from the user problem and what success looks like, then ship in small steps behind feature flags, so risk
  stays low and feedback comes early.
- Write down decisions as ADRs, with the trade-offs I accepted.
- Test the behaviour, not only the types: e2e against real infrastructure where it matters.
- Treat security and the supply chain as part of the design: pinned CI actions and images, secret scanning,
  least-privilege database roles, a strict content security policy.
- Lead through review, mentoring and written documentation, not only through code.
- Use Claude Code daily, with rules, reviewers and a verify step; I make the design decisions and review the code.

## Stack

TypeScript, Node.js, NestJS, Next.js, Nuxt, React, Vue, Tailwind, PostgreSQL, Redis, Kafka, Docker, Terraform, AWS,
GitHub Actions, Playwright, Vitest. Python for tooling.

## Contact

[LinkedIn](https://www.linkedin.com/in/andrii-prisniak)
