# SymPress organization metadata agent contract

## Purpose and boundaries

This special repository owns the public organization profile and default community files inherited by repositories without local overrides. It is public: do not add customer context, credentials, internal roadmaps or non-public repository details. Product names already announced on the public roadmap may remain, but do not infer or expose repository visibility from them.

## Read first

- `profile/README.md`: public organization landing page.
- `profile/docs/packages.md`: public package routing map.
- `profile/docs/principles.md`: architectural invariants and non-goals.
- `CONTRIBUTING.md`, `SECURITY.md` and `CODE_OF_CONDUCT.md`: inherited defaults.

## Verification

- Setup: `npm ci`.
- Fast/full local check: `npm run lint:docs`.
- Context helper: `./scripts/sympress-context --repo SymPress/kernel`; this reads repository metadata and never executes suggested commands.
- Helper self-test: `./scripts/sympress-context --self-test`.
- CI also checks every Markdown link; package-map links are therefore executable contracts, not unchecked prose.

## Invariants

- Link only public repositories in the package map. Unlinked roadmap names may describe intentionally public future products without claiming repository availability.
- Prefer links to canonical repository docs over duplicated setup instructions.
- Keep inherited community files generic; repo-specific behavior belongs in that repository.
- Update onboarding, package map and roadmap together when a public package changes status.
- Pin external GitHub Actions and disable persisted checkout credentials.
- Keep private repositories out of agent context unless the operator explicitly passes `--include-private`.

## Cross-repository impact

Changes to root community files may affect every SymPress repository that does not override them. Profile changes affect the public organization page immediately after merge.

## Definition of done

Markdown lint passes, CI link checks can resolve all local and external links, public package claims match current repositories, and no non-public metadata is present.
