## Udit Singh

**Backend · Systems · Software Engineer** — B.Tech Information Technology, ABES Engineering College (2027). Delhi NCR, India.

I build the layer underneath the application: a version control engine, a session-security model,
an integration platform. Most of what I know came from writing the thing rather than importing it.

---

### What I've built

**[Nexus](https://github.com/UditSinghChauhan/Nexus-git)** · *a Git-style version control system, written from scratch in Node.js with no git binary and no libgit2*

SHA-256 content-addressed commits over a two-parent DAG, BFS nearest-common-ancestor resolution for
three-way merge, and an LCS dynamic-programming diff engine. Exposed through a 7-command yargs CLI,
a JWT-authenticated REST API, and a React dashboard that updates live — commit from the terminal and
the browser reflects it, because the engine emits events at the point state changes.

`Node.js` `Express` `MongoDB` `Socket.IO` `React` · *15 backend tests passing*

---

**[CareerRadar](https://github.com/UditSinghChauhan/CareerRadar)** · *job and internship aggregation platform — TypeScript monorepo, contract-first API, 12 provider integrations*

An OpenAPI 3.1 spec is the single source of truth; both the Zod validators and the React Query hooks
are generated from it, so client and server contracts cannot drift. PostgreSQL via Drizzle over
10 indexed tables. A background scheduler fans out to 12 job-board integrations behind a plugin
registry, with exponential backoff and full jitter, retry classification that distinguishes transient
from permanent failures, and deduplication on a composite external key.

`TypeScript` `Express 5` `PostgreSQL` `Drizzle ORM` `pnpm monorepo` `OpenAPI 3.1` `Clerk` · *49 tests across 9 files — no database required to run them*

---

**[Bridge](https://github.com/UditSinghChauhan/videoconferencing_app)** · *real-time video meeting platform — WebRTC signaling, Socket.IO, and a hand-built session-security model*

15-minute access tokens and rotating refresh tokens with separate signing secrets, refresh and CSRF
tokens stored only as SHA-256 hashes, per-session CSRF verification, and JWT verified in the
Socket.IO handshake — checked against live server-side session state, so a token from a logged-out
session cannot open a connection. WebRTC media stays peer-to-peer; the server only relays signaling.

`Node.js` `Express` `Socket.IO` `WebRTC` `MongoDB` `React` · *48 backend tests — no database required*

---

**[Syllora](https://github.com/UditSinghChauhan/syllora-edtech)** · *EdTech course marketplace — 36 REST endpoints, three-role RBAC, OTP verification, Razorpay payments*

36 REST endpoints over 9 Mongoose models covering student, instructor and admin workflows. OTP email
verification, course CRUD with a section/subsection hierarchy, Cloudinary media uploads, and Razorpay
payments with HMAC-SHA256 signature verification, behind JWT/bcrypt auth and NoSQL-injection
sanitization.

`Node.js` `Express` `MongoDB` `React` `Redux` · *22 frontend tests, running in GitHub Actions CI*

---

### Something I found in my own code

I ran a security audit across all four repositories and found seven classes of defect — a bcrypt
password hash reachable from a public unauthenticated endpoint, a JWT accepted from the request body,
privileged scheduler routes anyone could trigger, an entire route module with neither authentication
nor ownership checks.

All seven are fixed, three with dedicated regression suites. The part worth mentioning: three of them
were found by taking a defect discovered in one repository and grepping the others for the same
pattern — which is how I discovered my first pass had missed two.

---

### Tools

| Area | Technologies |
|---|---|
| **Languages** | TypeScript · JavaScript · SQL · C++ · Java · Python |
| **Backend** | Node.js · Express · REST · OpenAPI 3.1 · middleware architecture · rate limiting |
| **Data** | PostgreSQL · MongoDB · Drizzle ORM · Mongoose · schema design · indexing |
| **Real-time** | WebRTC · Socket.IO · WebSockets · event-driven services · background schedulers |
| **Security** | JWT · refresh-token rotation · CSRF · bcrypt · RBAC · Zod · Clerk |
| **Testing** | Vitest · Jest · Playwright · Node built-in test runner |
| **Tooling** | Git · Linux · GitHub Actions · pnpm workspaces · Render · Vercel |

---

### Now

Next: building **DevAgent** — an episodic-memory-augmented multi-agent system for autonomous code
generation and debugging. Not started yet.

Also working through DSA (280+ across LeetCode, GeeksforGeeks and HackerRank) and starting to
contribute to open source.

---

[LinkedIn](https://www.linkedin.com/in/udit-singh-31382137a/) · [GitHub](https://github.com/UditSinghChauhan) · uditsinghchauhan720@gmail.com
