# Juan Francisco Paez

### Full-stack engineer who ships production AI — Java/Spring · React/React Native · Claude agents

Self-taught developer from Mar del Plata, Argentina. I build backends, web, mobile, and LLM agents, and I ship them end to end. I designed the architecture and can defend every line; AI accelerated the build. Currently learning Python / FastAPI.

🏆 Top 8 — Anthropic & Kaszek Buenos Aires Hackathon 2026
🌎 Fully remote (UTC-3, strong US-hours overlap) · open to remote LATAM / USD roles

---

### What I build

**🤖 [ai-booking-receptionist](https://github.com/juanfranpaezz/ai-booking-receptionist)** — *public, runnable*
The AI core of my shipped WhatsApp booking agent — the sanitized layer extracted from my production app (VINDA).
- Bounded agentic tool-use loop over the Anthropic Messages API — hand-written, not the SDK's `tool_runner` or an agent framework
- 6 JSON-schema tools behind an allow-list
- Two-layer prompt-injection guard (regex pre-filter + stored-data sanitizer), both layers unit-tested
- 7 deterministic eval cases + prompt-cache wiring

*Python.*

**💸 [LedgerMind](https://github.com/juanfranpaezz/ledgermind)** — *public · [live demo](https://ledgermind-odlf.onrender.com) (free tier, ~60–90s cold start)*
A double-entry payments core in Java/Spring. Append-only ledger (money as integer cents), idempotent transfers, and optimistic-locking concurrency. Verified by a 50-concurrent-transfer money-conservation test on real PostgreSQL (Testcontainers). Ships with a read-only MCP audit interface secured by OAuth2.1 (an AI agent can read the ledger, never move money), a SHA-256 hash-chain for tamper-evidence, Docker, and CI on every push.

**📅 VINDA** — *production SaaS (private repo)*
A multi-tenant scheduling & payments platform I built and shipped solo, full-stack:
- **Backend** — Java 21 / Spring Boot, Spring Security + JWT, WebSocket (STOMP) real-time chat & notifications, MercadoPago + Google Calendar integrations, Hibernate row-level multi-tenancy.
- **Production Claude agent** — the AI receptionist above, built on the raw Anthropic Messages API over the JDK HttpClient (no SDK client), plus per-tenant monthly LLM cost caps, an automatic Sonnet→Haiku degradation once a tenant's daily token usage runs high (cost control), and a Resilience4j circuit breaker.
- **Frontend** — React 18 SPA (booking, credits, chat, onboarding) with defensive XSS hardening (DOMPurify + server-side jsoup allowlist).
- **Mobile** — Expo / React Native app in **TypeScript** (biometric login, push notifications, multi-role routing).
- **DevOps** — Docker, nginx/Caddy, Prometheus + Grafana observability.

Across VINDA, the architecture and invariants are mine; AI accelerated the implementation.

*(The public repos above are self-contained; VINDA stays private.)*

---

### Tech

**Languages:** Java · JavaScript · TypeScript (mobile) · SQL · learning Python
**Backend:** Spring Boot · Hibernate/JPA · REST · Spring Security / OAuth2.1 · Spring AI (MCP) · learning FastAPI
**Frontend & Mobile:** React · React Native / Expo · HTML · CSS
**Data & Infra:** PostgreSQL · Flyway · Docker · GitHub Actions (CI) · Prometheus + Grafana · nginx/Caddy
**AI:** Anthropic / Claude API (agentic tool-use loops, prompt-injection defense, evals)
**Testing:** JUnit · Testcontainers · Playwright · Vitest / Jest
**Security posture:** defensive — parameterized queries (JPA), XSS sanitization, prompt-injection guards, auth gates

---

### Reach me

📧 juanfranciscopaezz@gmail.com · 💼 [LinkedIn](https://linkedin.com/in/juanfranciscopaez) · 🐙 [GitHub](https://github.com/juanfranpaezz) · CV on request
