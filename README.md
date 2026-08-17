<div align="center">

# Udit Singh

### Backend · Systems · Software Engineer

B.Tech Information Technology · ABES Engineering College (2027) · Delhi NCR

I build backend systems, developer tools and real-time applications —<br>
with a focus on security, correctness and implementations I understand from first principles.

<br>

[LinkedIn](https://www.linkedin.com/in/udit-singh-31382137a/) &nbsp;·&nbsp;
[GitHub](https://github.com/UditSinghChauhan) &nbsp;·&nbsp;
uditsinghchauhan720@gmail.com

</div>

---

## Projects

<table>
<tr>
<td width="50%" valign="top">

#### [Nexus](https://github.com/UditSinghChauhan/Nexus-git) — Git-style VCS, built from scratch

No git binary. No libgit2.

- SHA-256 content-addressed commit storage
- Two-parent DAG · BFS merge-base · three-way merge
- LCS dynamic-programming diff engine
- 7-command CLI + JWT REST API + live React dashboard
- Socket.IO events emitted from inside the engine

`Node.js` `Express` `MongoDB` `Socket.IO` `React` · **18 tests**

</td>
<td width="50%" valign="top">

#### [CareerRadar](https://github.com/UditSinghChauhan/CareerRadar) — TypeScript monorepo, 12 integrations

Contract-first: OpenAPI 3.1 generates Zod validators + React Query hooks.

- 9-package pnpm workspace · Express 5 · PostgreSQL/Drizzle
- Background scheduler fanning out to 12 job-board providers
- Full-jitter retry classification · composite-key deduplication
- 10 indexed tables · 7 enums

`TypeScript` `Express 5` `PostgreSQL` `Drizzle` `pnpm` · **49 tests, 9 files**

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [Bridge](https://github.com/UditSinghChauhan/videoconferencing_app) — WebRTC platform, hand-built session security

- Rotating refresh tokens stored as SHA-256 hashes
- JWT verified at Socket.IO handshake against live session state
- Per-session CSRF · separate access/refresh signing secrets
- WebRTC peer-to-peer media · backend-enforced host/participant roles

`Node.js` `WebRTC` `Socket.IO` `Express` `MongoDB` `React` · **48 backend tests**

</td>
<td width="50%" valign="top">

#### [Syllora](https://github.com/UditSinghChauhan/syllora-edtech) — Full-stack EdTech marketplace

- 36 REST endpoints · 9 Mongoose models
- Three-role RBAC (student / instructor / admin)
- OTP email verification · Razorpay + HMAC-SHA256
- Cloudinary uploads · NoSQL-injection sanitization

`Node.js` `Express` `MongoDB` `React` `Redux` · **22 tests · CI green**

</td>
</tr>
</table>

---

## Security

Ran a cross-repository audit and fixed **7 classes of security defects** — credential exposure in public API responses, unauthenticated destructive routes, missing object-level authorization, unsafe token handling. Three fixes include dedicated regression suites.

<details>
<summary>What I found →</summary>
<br>

| Defect class | Where |
|---|---|
| bcrypt hash exposed via unauthenticated public endpoint | Nexus · Syllora |
| JWT accepted from request body | Syllora |
| Unauthenticated scheduler-trigger routes (outbound amplification vector) | CareerRadar |
| Entire route module — no authentication, no ownership checks | Nexus |
| Credential fields returned to authenticated callers | Syllora |
| Unauthenticated sync routes firing external requests | CareerRadar |
| Refresh + CSRF tokens stored as plaintext | Bridge |

Three defects were found by treating one discovery as a *class* and grepping every other codebase for the same pattern.

</details>

---

## Stack

**Backend** &nbsp; Node.js · Express · REST · OpenAPI 3.1

**Systems** &nbsp; SHA-256 content addressing · commit DAGs · BFS traversal · LCS diff

**Data** &nbsp; PostgreSQL · MongoDB · Drizzle ORM · Mongoose

**Real-time** &nbsp; WebRTC · Socket.IO · WebSockets · background schedulers

**Security** &nbsp; JWT · refresh-token rotation · CSRF · bcrypt · RBAC · Zod

**Testing** &nbsp; Vitest · Jest · Playwright · Node test runner · **137 tests across 4 projects**

**Tooling** &nbsp; Git · Linux · GitHub Actions · pnpm · Render · Vercel

---

<div align="center">

[LinkedIn](https://www.linkedin.com/in/udit-singh-31382137a/) &nbsp;·&nbsp; [GitHub](https://github.com/UditSinghChauhan) &nbsp;·&nbsp; uditsinghchauhan720@gmail.com

</div>
