# AAB Registry Schemas

This repository defines the shared MongoDB document schemas used by the AAB evidence registry. It started as the case schema repository and now acts as the schema package for all registry collections so website, ingestion, review, and publication workflows can collaborate against the same data contract.

## Repository Structure

- `schemas/case.schema.json` - primary AAB case registry record schema.
- `schemas/pilot.schema.json` - pilot registry records derived from case and pilot framework evidence.
- `schemas/framework.schema.json` - frameworks and crosswalk-ready source records.
- `schemas/resource.schema.json` - free resources and curriculum/toolkit records.
- `schemas/initiative.schema.json` - initiatives and collaborative project records.
- `schemas/assessment.schema.json` - assessments, credentials, and measurement systems.
- `schemas/policy.schema.json` - country or jurisdiction-level policy signal records.
- `schemas/community-signal.schema.json` - country-level community signal records.
- `schemas/us-state-policy.schema.json` - U.S. state AI policy records.
- `schemas/us-state-community-signal.schema.json` - U.S. state community signal records.
- `mongodb/search-indexes.json` - recommended Atlas Search index definitions for registry lookup.

## Design Notes

The schemas are intentionally validation-oriented but not overly restrictive. AAB records evolve as evidence improves, so each schema allows additional fields while requiring stable identity, title, summary, status, source trace, and collection-specific signal fields.

The schemas were derived from the current `aab-dynamic-website/data/*.json` MongoDB fallback snapshots. Production MongoDB collection names should match the website README unless explicitly overridden by environment variables.

## Collaboration Guidance

- Make schema changes here first when adding new registry fields.
- Keep source trace fields (`sourceUrls`, `sourceFile`, `sourcePath`, `lastVerifiedAt`) intact.
- Use pull requests for breaking changes to required fields or enum values.
- Keep website data adapters backward-compatible when possible.
