# Decisions and open questions

## Accepted direction

QuickConnect helps find relevant professional contacts in permitted data, explains matches, prepares editable introductions, and tracks relationships. The user accepted this pivot from filtered automatic invitations.

Campaigns, People, and Follow-ups are the proposed daily surfaces. Users review matches and send initial outreach directly in their chosen service. Approved sending integrations can follow later.

## Proposed baseline

| Proposal | Why |
| --- | --- |
| Responsive web app | Desktop planning and phone review without native dependencies |
| Small private workspace | Prove personal usefulness before community cold start |
| Manual/CSV permitted records first | Avoid dependence on unavailable directory access |
| Deterministic explained filters | Stable evidence and transparent criteria |
| Optional AI drafts | Useful even without an inference account |
| Shared person history across campaigns | Avoid duplicate outreach and fragmented notes |
| In-app reminders first | Establish state before notification infrastructure |

## Unresolved choices

| Decision | Working default | Resolve by |
| --- | --- | --- |
| Public brand/name availability | QuickConnect as working name | Before public launch |
| Software license | Unselected | Before distribution/external contributions |
| First real data pool | User-controlled permitted contacts | Product/data proof |
| Hosted vs self-hosted | Architecture supports evaluation of both | Deployed prototype |
| Authentication provider | Established solution | Auth prototype |
| AI provider and funding | Optional supported user/project access | Drafting milestone |
| Directory partnerships | Deferred | Before discovery claims |
| Automatic sending | Deferred pending approved access | Integration milestone |
| Team workspaces | Deferred | After individual pilot |
| Retention duration | Configurable bounded policy | Pilot readiness |

## Risks

| Risk | Mitigation |
| --- | --- |
| No permitted discovery source | Useful organizer mode and honest source availability |
| Weak matching | Labeled cases, explicit criteria, evidence-backed reasons |
| Hiring inference errors | Separate signals, freshness, and uncertainty |
| Wrong person merge | Stable IDs, review, recoverable decisions |
| Fabricated introductions | Selected evidence and unsupported-claim checks |
| Missing cross-workspace checks | Server authorization and real database tests |
| Personal data in public Git | Synthetic fixtures and prepublication inspection |
| Duplicate reminder/send | Distinct state and idempotent retry; no sending MVP |
| Platform restrictions | Approved adapter gate, no scraping fallback |
| Scope growth | Vertical slices and milestones |
| Brand collision | Name/domain/trademark review before launch |

## What is not claimed

No live application, unrestricted LinkedIn access, approved sending API, discovered directory, benchmark, reply-rate improvement, deployed database, or created GitHub repository is established by writing the blueprint.

A copied introduction is not sent. A sent report is not confirmed delivery. A company vacancy is not a person's hiring authority. A public code repository is not public access to its application's data.

