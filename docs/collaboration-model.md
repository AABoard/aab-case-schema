# AAB Data Collaboration Model

AAB uses three connected layers:

1. MongoDB is the live operational registry database.
2. The AAB website is the public publishing layer.
3. GitHub is the collaboration, review, versioning, and transparency layer.

This repository is not the canonical database. It is where contributors can propose data structure changes, review schema assumptions, improve templates, and inspect public snapshots.

## Contribution Lifecycle

1. Intake: contributor opens an issue or pull request.
2. Triage: maintainers label the collection family and review type.
3. Evidence review: reviewers check source trace, public suitability, and privacy risk.
4. Schema review: maintainers check field names, required fields, and compatibility.
5. Database action: approved changes are applied to MongoDB by authorized maintainers.
6. Publication: approved public records appear on the website.
7. Snapshot: public dated exports may be committed here for transparency.

## Collection Families

- Cases
- Pilots
- Frameworks
- Free resources
- Initiatives
- Assessments and credentials
- Policy signals
- Community signals
- U.S. state policy signals
- U.S. state community signals

## Review Status

Recommended status values:

- `draft`: submitted but not reviewed.
- `needs-review`: ready for AAB review.
- `needs-revision`: missing evidence, schema fields, or source trace.
- `public-candidate`: suitable for public registry consideration.
- `published`: approved for public website display.
- `archived`: retained for record but not actively displayed.
- `rejected`: not accepted for registry use.

## Public Claim Rule

Every public claim should trace to at least one of:

- A MongoDB record ID.
- A public source URL.
- A dated export file.
- A standards evidence trace.
- A documented AAB review decision.
