<!-- Profile README: Yonas Valentin Mougaard Kristensen -->

<h1 align="center">Yonas Valentin Mougaard Kristensen</h1>
<p align="center"><b>Senior Software Engineer · EDC Group · Copenhagen</b></p>
<p align="center">
  <a href="mailto:yonasmougaard@gmail.com">yonasmougaard@gmail.com</a> ·
  <a href="https://linkedin.com/in/yonas-valentin">LinkedIn</a>
</p>

<p align="center">
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white">
  <img alt="React" src="https://img.shields.io/badge/React-20232a?logo=react&logoColor=61DAFB">
  <img alt="Next.js" src="https://img.shields.io/badge/Next.js-000?logo=next.js&logoColor=white">
  <img alt="React Native" src="https://img.shields.io/badge/React%20Native-20232a?logo=react&logoColor=61DAFB">
  <img alt=".NET" src="https://img.shields.io/badge/.NET-512BD4?logo=dotnet&logoColor=white">
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-336791?logo=postgresql&logoColor=white">
  <img alt="Supabase" src="https://img.shields.io/badge/Supabase-3ECF8E?logo=supabase&logoColor=white">
  <img alt="Railway" src="https://img.shields.io/badge/Railway-0B0D0E?logo=railway&logoColor=white">
  <img alt="Vercel" src="https://img.shields.io/badge/Vercel-000?logo=vercel&logoColor=white">
  <img alt="OpenAI" src="https://img.shields.io/badge/OpenAI-412991?logo=openai&logoColor=white">
</p>

---

## Snapshot
I design, build, and operate production systems across **mobile (Expo/React Native)**, **web (Next.js)**, and **backend (.NET/NestJS/Postgres)**. Typed contracts, deterministic CI, and clean data models are non-negotiable.

- 7 VS Code extensions with 1,000+ installs  
- Founder/operator on multiple SaaS products  
- Proven delivery on mobile + .NET stacks at enterprise scale  
- Feature flags, observability, zero-downtime migrations by default

---

## Building Now

### TeoriTjek — CEO & Co-founder
Danish driving theory exam platform. iOS live, Android next.  
Stack: React Native (Expo), TypeScript, .NET API, Postgres, Supabase, App Store CI/CD  
Links: [iOS App](https://apps.apple.com/dk/app/teoritjek-best%C3%A5-teoripr%C3%B8ven/id6744063979) · [Compare Driving Schools](https://www.teoritjek.dk/sammenlign-koreskoler)

### PhraseFlow — Translation Systems without Spreadsheet Chaos
AI-assisted translation workflow with real source-of-truth and missing-locale guards.  
Stack: Next.js 16, TypeScript, .NET on Railway, Postgres, pnpm packages for Expo/Next  
Link: [phraseflow-web.vercel.app](https://phraseflow-web.vercel.app)

### UseWorkspace — Workspace & Asset Management
Space/desk/asset lifecycle with AI assistance.  
Stack: Next.js 16, .NET, OpenAI, Railway  
Link: [useworkspace.dk](https://useworkspace.dk)

---

## Open Source Tooling

Built 7 VS Code extensions (selected):

- **[ErrorClipper](https://marketplace.visualstudio.com/items?itemName=YonasValentinMougaardKristensen.errorclipper)** — Copy errors with code context; AI-ready snippets (~453 installs)  
- **[Aether – Sublime Code Theme](https://marketplace.visualstudio.com/items?itemName=YonasValentinMougaardKristensen.aether-sublime-code)** — Focused, contrast-correct theme (~192)  
- **[Git Branch Manager](https://marketplace.visualstudio.com/items?itemName=YonasValentinMougaardKristensen.git-branch-manager)** — One-click cleanup of merged branches (~152)  
- **[Azure DevOps Code Companion](https://marketplace.visualstudio.com/items?itemName=YonasValentinMougaardKristensen.azure-devops-code-companion)** — Boards and repos in-editor (~104)  
- **[IntelliSense Number Suggestions](https://marketplace.visualstudio.com/items?itemName=YonasValentinMougaardKristensen.intellisense-number-suggestions)** — Smart numeric hints (~91)  
- **[ClickUp Code Companion](https://marketplace.visualstudio.com/items?itemName=YonasValentinMougaardKristensen.clickup-code-companion)** — Ship tasks from VS Code (~88)  
- **[TODO Debt Manager](https://marketplace.visualstudio.com/items?itemName=YonasValentinMougaardKristensen.todo-debt-manager)** — Visualize and burn down tech debt (~32)

All extensions: <https://marketplace.visualstudio.com/publishers/YonasValentinMougaardKristensen>

---

## Operating Manual

### Engineering Principles
1. **Typed boundaries or no boundaries** — shared DTOs/Zod schemas, contract tests, generated clients.  
2. **Monolith first, modular later** — bounded contexts enforced by folder and ownership, not hope.  
3. **Observability from day one** — logs, metrics, traces, budget alarms, and user-visible SLOs.  
4. **Migrations are products** — progressive rollouts, backfills, and kill-switches.  
5. **DX compounds** — reproducible dev env, seed data, fast feedback, preview deploys.  
6. **AI assists, humans decide** — codegen for glue, human review for architecture.

### PR Checklist (excerpt)
```md
- [ ] Contract tests updated (DTOs/Zod) and generated clients bumped
- [ ] Zero-downtime: write → read → deprecate path applied to migrations
- [ ] Telemetry added (metric + trace + log) and dashboard link posted
- [ ] Security review: RLS/claims/roles; secrets via env or vault; no PII in logs
- [ ] Rollout plan with flags and rollback command included

Migration Playbook (excerpt)

1) Additive schema only. Deploy write paths behind a flag.
2) Dual-write and validate. Backfill idempotently with chunked jobs.
3) Flip reads to new source behind a flag. Monitor error budgets.
4) Remove dual-write. Drop legacy only after cold period with snapshots.


⸻

Architecture Defaults
	•	API: .NET/NestJS, CQRS where it pays off, MediatR/handlers for cross-cutting concerns
	•	Data: Postgres, Prisma/EF Core, RLS on external-facing contexts, audit trails
	•	Frontends: Next.js 16 and Expo, strict TypeScript, feature flags, e2e happy-path tests
	•	AI: OpenAI for summarization/assistance; no black-box decisions in core flows
	•	Ops: Railway/Vercel, GitHub Actions, canary + auto-rollback, environment-scoped secrets
	•	Analytics: PostHog/Umami, event contracts, server-side ingestion preferred

⸻

Proof of Work
	•	Scaled Workr (student job marketplace) to ~80,000 users over 9 years
	•	Shipped multiple SaaS products and a live App Store app as operator and engineer
	•	7 VS Code extensions installed by 1,000+ developers
	•	Delivery track record across mobile + .NET in a regulated, data-sensitive domain

⸻

Day Job

Senior Software Engineer @ EDC Group
Shipping React Native apps and .NET backends for real estate workflows. Focus: reliability, clean data, measurable outcomes.

⸻

Stack

Mobile: React Native (Expo), TypeScript
Web: Next.js 16, React, TypeScript
Backend: .NET, NestJS, Node.js
Data: PostgreSQL, Supabase, Prisma
AI: OpenAI API
Ops: Railway, Vercel, App Store Connect, GitHub Actions

Currently deepening .NET/NestJS architecture and database scaling. Frontend specialist who ships backends that hold up.

⸻

Build Signals


⸻

Contact

Email: yonasmougaard@gmail.com
LinkedIn: /in/yonas-valentin
Support: https://buymeacoffee.com/yonasvalentin