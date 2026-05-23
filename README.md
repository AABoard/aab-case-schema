# AABoard Data and Schema

This repository is the public collaboration layer for AABoard registry data structures. MongoDB remains the live operational database, and the AABoard website remains the public publishing layer. This repository documents how records are structured, reviewed, exported, searched, and improved before changes become official registry content.

## What Belongs Here

- JSON Schemas for AABoard registry collections.
- CSV and Markdown submission templates.
- Field definitions and data dictionary notes.
- Public dated exports from MongoDB when AABoard chooses to publish snapshots.
- Validation scripts and examples for contributors.
- Atlas Search index definitions and example query patterns.
- Review status definitions and source-quality rubrics.

## What Does Not Belong Here

- MongoDB credentials or `.env` files.
- Private reviewer notes or unpublished sensitive pilot data.
- The canonical live database.
- Website application code.

## Repository Structure

- `schemas/` - JSON Schema files for registry records.
- `templates/` - contributor-facing submission and review templates.
- `examples/` - small sample records that demonstrate schema shape.
- `exports/` - dated public snapshots exported from MongoDB.
- `search/` - Atlas Search index definitions and search examples.
- `validation/` - scripts for checking submitted records.
- `docs/` - data dictionary, workflow, status, and source-review documentation.
- `.github/ISSUE_TEMPLATE/` - issue forms for submissions and schema changes.

## Collaboration Flow

1. Contributors open an issue or pull request with a proposed record, schema change, or data correction.
2. AABoard data reviewers check source trace, schema fit, evidence status, and publication risk.
3. Accepted records are entered into MongoDB by maintainers or approved data operators.
4. The AAB website publishes approved public records from MongoDB.
5. Public exports may be committed here as dated snapshots for transparency and research reuse.

## MongoDB and Search Notes

Use Atlas Search for registry keyword, fuzzy, faceted, and multi-field search. Avoid regex-heavy search patterns for public registry discovery. Search index definitions belong in `search/` so collaborators can review field coverage before changes are applied to MongoDB Atlas.

## Current Record Families

AABoard currently organizes records around cases, pilots, frameworks, free resources, initiatives, assessments and credentials, policy signals, community signals, U.S. state policy signals, and U.S. state community signals.

## Contributing

Start with `CONTRIBUTING.md`, then use the relevant issue template. Breaking schema changes should be proposed before implementation because they can affect MongoDB ingestion, website rendering, exports, and standards evidence traces.
