# Repository and contribution plan

## Requested repository

Owner: EvanGUTK. Repository: [EvanGUTK/Quickconnect](https://github.com/EvanGUTK/Quickconnect). Visibility: public for code and documentation. No real contact data or private networking history belongs in that repository.

The initial blueprint is published on main, with a matching planning snapshot on docs/quickconnect-product-blueprint. Repository visibility and the published file tree are checked during publication.

## Publication approach

The owner created the public repository. Publish the original planning documents on main and retain docs/quickconnect-product-blueprint as a reviewable planning snapshot. Preserve the documentation as the starting point for later milestones.

The current package contains no application code. Do not imply its folder plan exists as implementation.

## Future layout

| Planned path | Responsibility | Owner |
| --- | --- | --- |
| apps/web/ | Next.js interface and server entry points | Frontend/Backend |
| packages/domain/ | Campaign, person, relationship rules | Backend |
| packages/contracts/ | Versioned schemas | Designated contract owner |
| packages/matching/ | Filter semantics and explanations | Matching |
| packages/drafting/ | Templates and provider abstraction | Drafting |
| packages/sources/ | Permitted adapters and provenance | Data/Integrations |
| packages/jobs/ | Durable reminder/import jobs when needed | Backend |
| db/ | Reviewed schema, migrations, synthetic seeds | Backend/Data |
| tests/fixtures/ | Fictional data and source scenarios | Relevant owner |
| tests/acceptance/ | Representative workflows | Validator |
| docs/ | Product, decisions, release evidence | Chief/Specialists |
| assets/brand/ | Original future branding | Product/UX |

Keep modules within the application until extraction has clear benefits. This is an ownership plan, not a command to scaffold every package immediately.

## Branch strategy

main is the accepted project baseline. feature/<task> holds a bounded change. integration/<milestone> assembles dependent work if needed. docs/quickconnect-product-blueprint captures planning. fix/<failure> handles a specific validator finding.

Do not auto-merge solely because a feature branch exists or an implementer reports success.

## Worktrees

Use one isolated worktree per concurrent bounded task. Keep shared contract changes under one owner. Each worktree uses separate synthetic database state and process/port configuration.

A Git worktree does not isolate shared databases or provider credentials automatically. Do not run integration tests against the user's live networking data.

## Atomic commits

A coherent behavior plus its relevant tests/docs belongs in one commit. Avoid broad mixed changes across import, matching, auth, and UI without clear review boundaries.

Commit lockfiles when implementation starts. Exclude secrets, personal CSVs, database dumps, provider payloads containing personal information, and generated build artifacts.

Documentation is a coherent initial planning snapshot. It should not receive a passing-build badge before executable checks exist.

## Review contract

A PR identifies the problem, behavior change, touched domain boundary, actual verification, and limitations. Validator findings reference a tested commit. Chief checks compatibility and integrated behavior.

Source integrations require explicit evidence of permitted use and actual capability. Drafting changes require grounding tests. Ownership-sensitive changes require cross-workspace checks.

## README presentation

Use centered identity, a clear promise, truthful planning badges, scenarios, principle tables, compact diagrams, and direct links to deeper documents. Later screenshots must show the actual original application and use synthetic contacts.

Brand and software license remain decisions before distribution/contributions. Public visibility is not itself an open-source license.

