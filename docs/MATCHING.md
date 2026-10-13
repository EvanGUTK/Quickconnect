# Explainable matching

## What a match means

A match indicates how available evidence fits the user's declared networking goal. It is not a prediction of a person's worth, hiring power, willingness to respond, or likelihood of giving the user a job.

Separate strict filters, preferred relevance, evidence quality, and relationship context. Users should understand all four.

## Criteria semantics

| Criterion | Example | Behavior |
| --- | --- | --- |
| Required | Must have attended a selected school | Include only records with supporting evidence; unknowns shown separately |
| Preferred | Robotics experience is useful | Adds ranking contribution when supported |
| Excluded | Already contacted in this campaign | Excludes or hides according to user selection |
| Informational | Current relationship status | Display context without inventing relevance |
| Freshness | Recent explicit hiring signal | Evaluate evidence date and signal type |

Filters are AND across distinct required criteria by default, OR within a selected set such as several companies. Exclusions take precedence. Display the actual logic in ordinary language before applying it.

Unknown values do not pass a strict filter. Offer an “include unknowns for review” option with clear labels; never turn unknown into true.

## Normalization

Normalize school aliases, company names, and common role terms using a reviewed mapping. Preserve original values. Exact title text and broader role category remain distinct.

Example: “Talent Acquisition Partner” can be categorized as recruiting, but it does not prove hiring responsibility for a particular team. Topical tags need evidence and source dates.

## Ranking

Start with deterministic weighted contributions selected by campaign purpose. A prototype could consider role fit, topic overlap, shared institution, company relevance, and evidence freshness.

The exact weights are provisional. Avoid presenting a 92% score as a calibrated probability. Prefer “strong fit,” “partial fit,” or a clearly labeled relative relevance score with contributions.

A transparent conceptual formula is the sum of supported criterion contributions, adjusted for evidence uncertainty/freshness. Required eligibility is evaluated first and is not overridden by a large preference score.

## Evidence cards

Each match card includes the relevant criteria, supporting facts, source references, dates, missing fields, and contradictory evidence. Its explanation is generated from the actual ranking contributions.

A polished AI explanation may not add reasons that the deterministic result did not contain. Changes to criteria or facts create a new snapshot. Previous explanations retain their version so the UI can show when they became stale.

## Hiring signals

| Signal | What it supports | What it does not prove |
| --- | --- | --- |
| Recruiting title | Recruiting is part of the person's role | Their current requisitions or authority over a team |
| Explicit hiring statement | Person recently stated a hiring need | The opening is still available indefinitely |
| Documented team responsibility | Relevant management responsibility | They personally control every hiring decision |
| Company vacancy | Employer has an advertised opening | Any given employee is the hiring contact |
| User note | User's own observation | Externally verified fact |

Display separate filters for these signals. Preserve source/date and allow stale-signal exclusion. Do not use personal characteristics unrelated to the declared professional purpose as relevance proxies.

## Relationship context

Already contacted, replied, declined, or do-not-contact states affect the review queue. A contact can fit the goal and still be inappropriate to approach again.

Keep ranking separate from contact authority. A high fit does not justify another message, sharing private notes, or adding a person to a public directory.

## Feedback

Allow “relevant,” “not relevant,” “wrong fact,” and “already know this person” feedback. A factual correction updates source/fact state. A campaign preference updates that campaign first.

Do not automatically generalize one rejection into a global preference or continuously train on private user records. Start with explicit preference updates and measured ranking changes.

## Semantic matching later

Embedding/topic models can identify overlap beyond exact words. They need evaluated inputs, permitted processing, explanation grounding, and a deterministic fallback. They must not relax a required school or invent work history.

Measure ranking usefulness with labeled examples, including near matches, contradictory records, aliases, missing data, stale signals, and existing relationships. Collect user feedback without treating reply rates as unbiased labels of relevance.

## Acceptance

The same facts and campaign version produce stable deterministic results. Every surfaced reason has a source. Required/excluded rules behave predictably. Unknowns remain labeled. Removing a fact invalidates affected reasons. Company vacancies never promote all employees into “hiring.”

