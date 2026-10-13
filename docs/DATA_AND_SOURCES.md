# Contact data and source strategy

## The foundational constraint

A search interface is not a data source. QuickConnect cannot discover people from an unrestricted professional directory unless it has permission and technical access to that directory.

Begin with a small useful pool of records the user is permitted to use. A dataset that supports a private contact organizer may not support redistribution, public indexing, AI processing, or commercial enrichment. Evaluate each intended use separately.

## Source classes

| Source | Possible use | Required check |
| --- | --- | --- |
| User-authored contacts | Private organization and drafting | User's authority and appropriate data handling |
| User-provided CSV | Mapping, preview, filtering | Provenance and permission; file availability is not blanket permission |
| Opt-in directory | Discover consenting members | Explicit visibility/use settings and revocation |
| Partner/API directory | Approved discovery | Granted scopes, terms, permitted storage and processing |
| Institution/event directory | Potential future contact pool | Actual publication/use terms, consent, and freshness |
| LinkedIn | Only supported approved integrations | No unrestricted scraping or invitation entitlement assumed |

Public visibility alone does not establish permission to scrape or reuse a directory. Even an official export can carry use restrictions. Do not label any import “compliant” merely because it came from the user.

## Initial collection strategy

The first pilot uses synthetic fixtures followed by a small user-controlled authorized contact pool. Manual entry and previewed CSV import are sufficient to prove campaigns, matching, drafting, and reminders.

Discovery connectors are a later gate. Before building one, establish access, permitted fields, storage limits, refresh behavior, onward use, and deletion obligations. If no partner source is available, the product remains an organizer for known contacts.

## Fact-level provenance

A person has facts with individual sources rather than one opaque profile blob. School, role, company, topic, and hiring status may come from different evidence.

Each fact records value, normalized value, source type/reference, observed date, validity period if known, verification status, confidence where appropriate, and permitted-use metadata. A user correction can supersede a fact without erasing its source history.

The evidence UI explains what supports a match. Private notes remain separate from externally asserted facts.

## Imports

Upload preview is a separate stage from committing records. Map known columns, show unknown columns, identify required fields, validate row count/size, and let the user review duplicates/conflicts.

Preserve missing values as missing. Never fill absent employers, schools, or hiring signals through invented AI enrichment.

Report accepted, rejected, skipped, and duplicate rows. Assign a batch ID and stable row outcomes. Retrying an import should not duplicate accepted rows. Offer undo where it can be performed coherently without deleting unrelated later user edits.

## Identity resolution

Same name is not sufficient identity. Use available stable source IDs and permitted identifying fields; uncertain matches go to review. A single person can change employer or title without becoming a new contact.

Do not silently merge private notes for two uncertain people. Merge decisions need a preview and recoverable history. Exports must preserve enough identity context to remain understandable.

## Freshness and conflicts

An undated title is not recently verified. A dated hiring signal becomes stale based on its type and purpose. A person's explicit update can supersede an older directory fact.

Conflicting values are displayed or resolved through documented source precedence. “Unknown,” “not present,” and “contradicted” are distinct. Removing a fact invalidates dependent match explanations and prompts review of affected drafts.

## Source withdrawal

If source authorization expires, stop new collection. Determine what existing records may be retained under that source's terms. Revoke derived discovery access as necessary. Show users which matches or drafts are now stale/unsupported.

User-created relationship notes may have a different lifecycle from imported source claims; define it explicitly rather than deleting everything indiscriminately or retaining everything forever.

## Private versus shared data

Workspace records are private by default. A future shared community directory requires a separate visibility model and consent flow. Users must not accidentally publish a contact by adding them to a campaign.

Source credentials and access tokens stay out of the code repository. Development seeds use fictional people and organizations or clearly licensed test fixtures.

## Data-source acceptance gate

A connector is ready only when its access has been established, field provenance is retained, permission limits are enforced, errors are explained, and authorization withdrawal produces correct behavior. “We can scrape it” is not a release criterion.

