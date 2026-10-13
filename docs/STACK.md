# Proposed technology stack

## Status

Components below are proposals for implementation. No packages have been installed and no application has been built. Select supported versions during the initial proof and pin them after testing.

| Layer | Proposed choice | Reason | Gate |
| --- | --- | --- | --- |
| Application | Next.js with App Router | One responsive web app with server-side application routes | Validate deployed runtime, auth, and background-job separation |
| UI | React and TypeScript | Typed campaign, contact, and draft state | Accessible keyboard behavior and clear ownership |
| Styles | CSS design tokens; Tailwind candidate | Consistent responsive presentation | Avoid a heavy component library before need |
| Validation | Zod candidate | Shared typed input validation | Server validates independently of browser |
| Database | PostgreSQL | Structured criteria, transactions, full-text search | Workspace isolation, indexes, backup/restore |
| Data layer | Prisma candidate | Typed records and reviewed migrations | Evaluate full-text query path and transaction behavior |
| Auth | Established OIDC solution; exact provider TBD | Avoid custom password/session implementation | Server authorization and recovery flows |
| AI | Optional provider interface | Drafting and evidence-based summaries | Supported access, private-data boundaries, budgets |
| Imports | Robust CSV parser | User-controlled mapping and preview | Encoding, quoting, duplicates, formulas, partial failure |
| Jobs | Database-backed job runner when necessary | Durable reminder/import work | Idempotency, retries, timezone behavior |
| Tests | Vitest plus Playwright | Domain logic and representative browser workflows | Real database isolation checks where needed |
| Deployment | Standard Node web host plus database | Familiar operating model | Cost, environment secrets, deploy/rollback |

## Search first

Begin with structured fields, normalization, and database full-text search. Exact university/company mappings and controlled role categories solve many initial cases.

Do not introduce a vector database simply because the app includes AI. Embeddings may help topical relevance later, but they cannot create missing facts, establish source permission, or prove a hiring claim.

If semantic matching is added, preserve deterministic hard filters and show which evidence contributed. Evaluate it against a labeled synthetic/contact set and retain a fallback.

## AI optionality

Users can create campaigns, filter contacts, inspect explanations, edit templates, and track follow-ups without model access. Optional model use improves wording and topic summaries.

Provider choice should be configuration, not part of person identity. Keep provider keys on the server or in a suitably protected self-hosted environment. Browser local storage is not a credential vault.

A subscription/login route needs explicit supported entitlement. An API key route may incur usage charges. No unlimited-free inference promise.

## Web versus other forms

| Form | Planning position |
| --- | --- |
| Responsive web app | Primary release target |
| Installable PWA | Consider after basic browser behavior is reliable |
| Browser extension | Defer; only add a permitted integration with independent value |
| Desktop wrapper | Defer; no native PC-control requirement |
| Native mobile app | Defer unless mobile browser/PWA limitations block use |

A public web app does not mean a public contact directory. Private-by-default workspace semantics apply regardless of deployment format.

## Alternatives

A Vite/React frontend with a separate FastAPI backend is reasonable if the maintainer strongly prefers Python domain logic. It introduces another runtime and contract boundary, so choose it only if that tradeoff improves implementation.

Supabase can be evaluated as an integrated database/auth host. Its row policies, service credentials, provider terms, and pricing need explicit review. Do not assume managed auth replaces application authorization.

SQLite can support a single-user local prototype but is not the default hosted multi-user recommendation. A prototype's persistence shortcut should not be mistaken for completed hosted tenancy.

## Tooling and packaging

Use one package manager with a committed lockfile. Keep formatting, linting, and type checks small and consistent. Add CI once executable application code exists; planning badges must not imply test success.

Maintain reviewed migrations and synthetic seed data. Do not commit live contact exports, personal messages, provider tokens, or database dumps.

## Version and dependency review

Check supported Next.js/runtime versions, ORM compatibility, authentication package maintenance, dependency licenses, and the deployment environment before implementation. Revalidate external API availability at integration time.

Do not ship a notification or message-delivery dependency until the associated consent, retry, opt-out, and delivery-state behavior is defined. The first release can keep reminders inside the app.

