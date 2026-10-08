# Andrii Prisniak

Senior fullstack and backend engineer in Hamburg, Germany. I build TypeScript systems end to end (NestJS,
Next.js, React, Vue, PostgreSQL, AWS) and care most about the decisions that still hold up a year later.

Production work: architecture and delivery of a digital claims platform, and backend services for a
crypto exchange serving 15M+ users. That work is under NDA, so the public repositories below show how I
think and build instead.

## Public work

| Project                                                                       | What it shows                                                                                                                                                     |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [kafka-pay-lab](https://github.com/sotream/kafka-pay-lab)                     | Event-driven payments: transactional outbox, consumer lag, retries, dead-letter topic, circuit breaker, realtime dashboard. NestJS, Next.js, Kafka, PostgreSQL.   |
| [nest-next-starter](https://github.com/sotream/nest-next-starter)             | Fullstack monorepo foundation: JWT with rotating refresh cookie, modular monolith, 9 ADRs, e2e tests on real Postgres and Redis, CI.                              |
| [nest-next-aws-terraform](https://github.com/sotream/nest-next-aws-terraform) | Terraform on AWS for the starter: ECS Fargate, RDS, ElastiCache, ALB, GitHub OIDC CI/CD, ADRs and a cost estimate. Tested offline, not applied to a real account. |
| [CodeSage](https://github.com/sotream/CodeSage)                               | RAG pipeline for questions about a codebase. Small modules, explicit trade-offs, ADRs. Python.                                                                    |
| [nomad-coverage-check](https://github.com/sotream/nomad-coverage-check)       | Small React and GraphQL app built with Claude Code from a written spec and plan.                                                                                  |

## How I work

- Write down decisions as ADRs, with the trade-offs I accepted.
- Test the behaviour, not only the types: e2e against real infrastructure where it matters.
- Use Claude Code daily, with rules, reviewers and a verify step; I make the design decisions and review the code.

## Stack

TypeScript, Node.js, NestJS, Next.js, React, Vue, PostgreSQL, Redis, Kafka, Docker, AWS, GitHub Actions. Terraform for AWS. Python for tooling.

## Contact

[LinkedIn](https://www.linkedin.com/in/andrii-prisniak)
