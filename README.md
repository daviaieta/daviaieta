<h1 align="center">Davi Aieta</h1>

<p align="center">
  <b>Full-stack engineer · 17 · building production software since I was 12</b><br/>
  Head of Technology at <b>É A Comunidade</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Fastify-000000?style=flat-square&logo=fastify&logoColor=white" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
</p>

---

```ts
const davi = {
  role: ["Full-stack engineer", "CEO & Head of Technology @ É A Comunidade"],
  age: 17,
  base: "Rio de Janeiro, Brazil",
  background: "2 years of high school in the US, back in Brazil to finish it",
  languages: ["Portuguese", "English", "Spanish"],
  codingSince: "age 12 — from scratch, before AI did the typing",
  focus: ["backend architecture", "multi-tenant SaaS", "mobile", "AI-native engineering"],
  currently: "shipping the community app to web, iOS and Android",
} as const;
```

## About

I started writing code at 12, the hard way: no copilots, just docs and broken builds. Today I build
full-stack products end to end — schema, API, web, mobile, infra and deploy — and ship them to
real users.

I spent two years of high school in the United States and came back to Brazil to finish it. I work
in **Portuguese, English and Spanish**.

Since September 2026 I run technology at **É A Comunidade**, a community of 700+ members, where I
own the stack from the database to the App Store.

## What I'm building

### 🏠 The É A Comunidade app — `production`
An invite-only social network for the community, mobile-first. One API, three clients.

- **Product:** feed, stories, courses (pillar › collection › module), missions with proof review,
  a 10-degree progression system, leaderboards, live sessions and a member directory.
- **Backend:** Fastify 5 · TypeScript · Prisma · PostgreSQL 16 · Redis (cache, job queues, rate limiting).
- **Clients:** Next.js 15 web app (installable) + native **iOS/Android** app built with Expo, against the same API.
- **Infra:** Railway (API + Postgres) · Vercel (web) · Cloudflare R2 (media) · Resend (email) · GitHub Actions.
- **Ownership:** took it from zero to production in September 2026, onboarded the members by bulk
  invite, ran the security and App Store audits, and shipped a full Liquid Glass redesign.

### ⏱️ [TimeFlow](https://github.com/daviaieta/TimeFlow) — `paused`
Multi-tenant scheduling SaaS for service businesses (barbershops, salons, clinics).

- Tenant isolation on every query, RBAC (`SUPERADMIN` / `ADMIN` / `EMPLOYEE`), token-based invites.
- Public booking page per business with an **atomic multi-slot claim**: two clients racing for the
  same slot produce exactly one booking — enforced by the database, not the app.
- CRM in five phases: customer identity, history, loyalty, magic-link portal, identity merge,
  idempotency keys and a Postgres-backed shared rate limiter.
- Stripe subscriptions, R2 uploads, owner dashboard with occupancy heatmap.
- ~42k lines of TypeScript · 19 models · 15 migrations · 45 test files.

## How I build

- **Layered backends:** `routes → controllers → services → repositories`. Business rules live in services, never in handlers.
- **Correctness in the database:** constraints, transactions and idempotency over "it worked on my machine".
- **AI-native, not AI-dependent:** I run agents in parallel with Claude Code and write every prompt
  myself — but I read the diff and I want to understand every line that ships.
- **Done means running:** the feature works in the browser and on the device, not just in CI.
- **Decisions are documented** with the trade-off we accepted, so the next person knows why.

## Stack

| Layer | Tools |
|---|---|
| Languages | TypeScript, JavaScript, Python, SQL |
| Backend | Node.js, Fastify, NestJS, Prisma, PostgreSQL, Redis, BullMQ, JWT |
| Frontend | Next.js (App Router), React, Tailwind CSS, shadcn/ui |
| Mobile | Expo, React Native, expo-router |
| Infra | Railway, Vercel, Netlify, Cloudflare (R2 + DNS), Docker, GitHub Actions |
| Services | Stripe, Resend, AssemblyAI, Anthropic API |
| AI tooling | Claude Code, multi-agent workflows |

## Building in public

I document what I build — the code, the decisions and the mistakes — on Instagram and YouTube.
<!-- TODO: add links -->
<!-- [Instagram](https://instagram.com/HANDLE) · [YouTube](https://youtube.com/@HANDLE) -->

---
