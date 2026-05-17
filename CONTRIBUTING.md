# Contributing to AAB Data and Schema

Thank you for helping improve the AAB registry data model. This repository is for public collaboration on schemas, templates, exports, search definitions, and validation rules. It is not the live MongoDB database.

## Contribution Types

- New or revised schema fields.
- Data dictionary corrections.
- Case, pilot, framework, resource, assessment, policy, or community-signal submission templates.
- Public export organization.
- Validation script improvements.
- Atlas Search field coverage and query examples.
- Source-quality and review-status documentation.

## Do Not Submit

- MongoDB credentials, API keys, `.env` files, or private connection strings.
- Private student information or personally identifiable data.
- Unpublished partner or pilot records that have not been cleared for public review.
- Bulk scraped data without source, license, or review notes.

## Review Expectations

Every material data contribution should identify:

- The affected collection family.
- The field, schema, or record type being changed.
- The source or evidence basis.
- Whether the change is backward-compatible.
- Whether website rendering, MongoDB ingestion, search indexes, or standards evidence traces are affected.

## Pull Request Checklist

- [ ] The change has a clear source or rationale.
- [ ] Schema changes are documented in `docs/`.
- [ ] Breaking changes are called out explicitly.
- [ ] Examples or templates are updated when field names change.
- [ ] No credentials or private data are included.

## Record Status Language

Use cautious status language. Registry inclusion documents a source-traced record; it does not automatically mean endorsement, certification, accreditation, or final AAB position.
