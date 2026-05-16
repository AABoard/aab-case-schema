# Schemas

These JSON Schemas describe the current AAB evidence registry collections. They are compatible with MongoDB JSON documents and can be used by ingestion scripts, website validation, review tooling, and publication workflows.

## Required Pattern

Every registry record should preserve:

- stable `id` or `case_id`
- `type`
- human-readable `title`
- concise `summary`
- review/publication `status`
- source trace through `sourceUrls`, `sourceFile`, `sourcePath`, `lastVerifiedAt`, or equivalent fields

## Validation Approach

The schemas set stable required fields and collection-specific signal fields, while allowing `additionalProperties` for evolving evidence fields. This avoids blocking registry iteration while keeping collaboration data contracts explicit.
