# Interface and visual direction

## Identity

QuickConnect should feel purposeful, calm, and easy to scan. Proposed identity: midnight/slate foundations, teal primary accent, blue navigation cues, lilac evidence highlights, and amber uncertainty. All state colors have text/icon equivalents.

The README follows Toby's presentation approach: centered identity, short promise, truthful badges, practical examples, tables, and compact diagrams. It does not contain fake screenshots or borrowed branding.

The application's public working name is QuickConnect. Brand/domain availability remains unverified.

## Daily navigation

| Surface | Main content | Primary action |
| --- | --- | --- |
| Campaigns | Goal, criteria, source pool, progress | Create or refine campaign |
| People | Filtered shortlist, evidence, relationship context | Review a person |
| Follow-ups | Due/overdue next steps and recent interactions | Act or reschedule |

Settings and import management are supporting surfaces. Avoid making users learn a CRM's full complexity before they can prepare one introduction.

## Onboarding

Explain what the app can do with a permitted contact pool. Offer synthetic demo data, manual entry, or a permitted CSV import. Do not imply a connected LinkedIn login grants universal search.

Create one campaign with a guided purpose, required/preferred criteria, and communication style. Show the resulting filter sentence in ordinary language.

AI connection is optional. Users can skip it and still use filters, templates, and follow-ups. Publishing the code does not publish their contact data.

## Campaign detail

Show purpose, required criteria, preferred signals, exclusions, source status, and last result generation. Provide a shortlist rather than an overwhelming wall of every possible person.

Filter editing previews how many supported records remain. An empty result explains whether the pool is empty, filters are too strict, or fields are missing.

Show explicit differences between “must match” and “prefer.” The user should not need to understand scoring algorithms to configure a useful campaign.

## Person card and detail

A card shows name, supported role/company, shared context, match explanation, freshness, and relationship status. Missing facts are visible and do not become empty decorative badges.

Person detail separates source-backed facts, user notes, campaign membership, drafts, and interactions. Evidence links have dates and source labels. Duplicates and conflicts open a review rather than silently rewriting the person.

## Introduction workspace

Use a side-by-side layout on desktop: draft and selected evidence. On mobile, use clear stacked sections. Provide editable text, tone/length controls, copy, and explicit “record as sent.”

The interface explains that copy is preparation. Future sending controls appear only when the connector's capability is established. No decorative “connected” label for an integration that merely signs the user in.

## Follow-ups

Group due today, overdue, upcoming, and completed. Each item shows who, why, last interaction, and suggested next step. Completing a reminder does not imply a message was sent.

Respect timezone and user-selected dates. Rescheduling is easy. Avoid pressure language implying a recipient owes a response.

## Empty and unavailable states

| Situation | Message direction |
| --- | --- |
| No contacts | Add authorized contacts or try synthetic demo |
| No matches | Explain filters and missing evidence |
| AI unavailable | Continue with manual template |
| Source expired | Existing facts may be stale; stop new collection |
| No sending integration | User sends directly and records the outcome |
| Unknown hiring status | Do not present as hiring |

## Accessibility

Keyboard-complete filter controls, labeled criteria, visible focus, scalable text, readable contrast, captions where media exists, and text equivalents for status. Evidence should not require hovering.

Tables and lists become usable cards on narrow displays. Draft editing must not lose content when switching tabs or returning from a mobile app.

## Prototype review

A user should be able to explain the campaign logic, understand a match, identify uncertain facts, prepare a truthful introduction, record outreach, and find the next step without developer assistance.

Do not optimize visual decoration at the expense of explaining evidence and uncertainty.

