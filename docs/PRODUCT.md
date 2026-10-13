# Product vision and detailed description

## Purpose

QuickConnect helps a user translate a networking goal into relevant people, understandable choices, and continuing relationships. It should reduce the work of searching a permitted contact pool, comparing profiles, composing first messages, and remembering follow-ups.

The accepted pivot moves away from connection-volume automation. The product's value is the quality of the shortlist and the usefulness of the next step. Users should be able to explain why they contacted a person without referring to an unexplained AI score.

## Product form

A responsive web application is the proposed first form. It supports desktop planning and phone review with the same workspace. A browser extension is deferred because the accepted workflow does not require modifying another platform's website. Desktop packaging is deferred because the initial product has no need for whole-computer control.

Public source code is distinct from public application data. Contact lists, drafts, notes, and campaigns belong to private workspaces unless a user deliberately shares them through a future supported feature.

## Primary users

| User | Goal | Useful outcome |
| --- | --- | --- |
| Early-career professional | Meet relevant recruiters, practitioners, and alumni | A specific introduction and organized follow-through |
| Researcher/student | Identify colleagues or potential mentors | Evidence of topic overlap and a focused question |
| Professional changing fields | Build relationships in a new domain | A manageable campaign with progress |
| Conference attendee | Continue relevant event conversations | Notes, reminders, and context preserved |
| Small professional community | Help opted-in members discover each other | A permission-backed directory, if later validated |

Start with an individual user managing a small contact pool. Team administration and a shared opt-in directory are later products, not hidden MVP requirements.

## Campaign model

A campaign captures purpose, target criteria, exclusions, message style, and a manageable contact review queue. Example: alumni in autonomy and robotics, prioritizing relevant practitioners and recruiting contacts in chosen companies.

Criteria can be required, preferred, or excluded. “Must have attended this university” differs from “shared university is a bonus.” The UI needs to display that distinction.

A campaign is not a bulk-send job. It does not schedule invitations or infer outreach authority. It organizes the user's goal and evidence.

## Key journeys

### Build a targeted shortlist

The user selects an existing permitted contact pool or adds authorized records, creates a goal, sets criteria, and inspects results. Each match card displays criteria met, unknowns, evidence dates, and why it was surfaced. The user saves a shortlist or dismisses a match with a reason.

A revised campaign generates a new match snapshot without rewriting the underlying relationship history.

### Organize known contacts

The user imports contacts they are permitted to use. QuickConnect previews columns, maps fields, identifies conflicts, and offers duplicate review. It does not silently merge two people who share a name.

Imported facts have origin and freshness. A current employer field without a date is not presented as recently verified.

### Prepare an introduction

The user chooses a person and a purpose. QuickConnect selects confirmed facts and generates an optional AI-assisted draft or deterministic template. The user edits it. Shared school, research overlap, or event context must be supported.

The user sends directly through their chosen service and records the result. Copying a draft is not proof of sending. Draft preparation remains available even when an AI provider is unavailable.

### Maintain a relationship

The user logs a reply, conversation, or meeting; adds a private note; and chooses a next step. Follow-ups are reminders to the user, not automatic repeated messages to the recipient.

A contact appearing in two campaigns shares one relationship history inside that workspace. Campaign-specific intentions remain separate.

### Interpret hiring information

The user filters for recruiting relevance. QuickConnect distinguishes an explicit recent hiring post, a recruiting job title, documented hiring responsibility, and company vacancies. These are different signals.

A company with open positions does not make every employee a hiring manager. A stale hiring statement is labeled rather than used as unquestioned truth.

## Initial scope

Campaign CRUD, permitted manual/CSV records, structured filters, evidence-backed match explanations, person detail, editable drafts, user-recorded outreach status, relationship notes, and due-date follow-ups.

No unrestricted LinkedIn discovery, unauthorized profile extraction, automated invitation sending, personal email discovery, hidden data enrichment, or guaranteed reply probability.

External APIs, mailbox synchronization, notifications, team collaboration, and semantic matching are separate increments with their own acceptance gates.

## Success metrics

Measure time to a useful shortlist, incorrect identity merges, unsupported statements in drafts, corrections to match explanations, reminders acted on, and user-reported useful conversations. A connection count alone is a weak proxy.

Observe whether the user can find fewer but more relevant contacts, explain the match, prepare a concise honest note, and remember a next step. Do not frame ranking as a measure of someone's worth or guaranteed willingness to respond.

## Empty and failure states

No source pool means no discovered people. Missing fields create unknowns. Provider failure leaves filters and manual templates working. A deleted source can invalidate a derived claim. A lost notification does not delete its underlying follow-up.

The app should remain useful as a lightweight relationship organizer even if external discovery access never arrives.

## Business direction

The first version can be an individual productivity tool with optional AI usage. Hosting, authentication, database, AI inference, and notifications still have operating costs. Pricing is not selected.

An optional community directory is a different business with an onboarding/cold-start challenge. Evaluate it only after the individual workflow is useful.

## Release promise

Make a narrow honest promise: organize a permitted contact pool, explain relevance, prepare introductions, and track relationships. Broader discovery and sending capabilities are advertised only after access and behavior are verified.

