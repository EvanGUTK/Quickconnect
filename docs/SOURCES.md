# Primary sources

Inspection date: 2026-10-13. External documentation changes; recheck at implementation and release.

## Platform access

- [LinkedIn prohibited software and extensions](https://www.linkedin.com/help/linkedin/answer/a1341387): unauthorized scraping, appearance modification, and activity automation restrictions.
- [LinkedIn automated activity](https://www.linkedin.com/help/linkedin/answer/a1341543): platform guidance on automation.
- [LinkedIn API access](https://learn.microsoft.com/en-us/linkedin/shared/authentication/getting-access): open permissions versus explicitly approved programs.
- [LinkedIn communication APIs](https://learn.microsoft.com/en-us/linkedin/shared/integrations/communications/overview): invitation/message APIs are documented, but their documentation does not establish access for QuickConnect.
- [LinkedIn connections API](https://learn.microsoft.com/en-us/linkedin/shared/integrations/people/connections-api): connection data scope is not an unrestricted person-discovery directory.

The accepted pivot avoids relying on unapproved profile discovery or invitation automation. Even user-provided or publicly visible data needs suitable use rights.

## Technical references

- [Next.js App Router](https://nextjs.org/docs/app): proposed application foundation.
- [Next.js Route Handlers](https://nextjs.org/docs/app/getting-started/route-handlers): proposed server boundary.
- [PostgreSQL full-text search](https://www.postgresql.org/docs/current/textsearch.html): proposed search foundation.
- [PostgreSQL search functions](https://www.postgresql.org/docs/current/functions-textsearch.html): text query/ranking facilities.
- [Prisma documentation](https://www.prisma.io/docs): data-layer candidate.
- [Vitest documentation](https://vitest.dev/guide/): unit/domain verification candidate.
- [Playwright documentation](https://playwright.dev/docs/intro): browser acceptance candidate.

The architecture, staffing, user experience, estimates, and acceptance targets are original design proposals. They are not vendor guarantees or completed work.

