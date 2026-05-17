# MongoDB Search Collaboration

This folder documents search definitions and examples for AAB registry discovery.

## Recommended Approach

Use Atlas Search for public registry lookup, including keyword search, fuzzy matching, faceted filtering, and multi-field search. Do not rely on regex-heavy search for user-facing discovery because it lacks relevance scoring, typo tolerance, and language-aware tokenization.

## What To Store Here

- Atlas Search index definitions.
- Example aggregation pipelines using `$search`.
- Field coverage notes for each collection family.
- Search behavior expectations for title, summary, tags, status, source, geography, age band, and evidence type.
- Notes about fields that should not be indexed publicly.

## Review Checklist

- [ ] The indexed fields exist in the current schema or data dictionary.
- [ ] Dynamic mappings are used intentionally, not accidentally.
- [ ] Private or sensitive fields are excluded.
- [ ] Filters support likely website use cases.
- [ ] Query examples are read-only.

## Source of Truth

Index definitions in this repository are review artifacts. They must be applied to MongoDB Atlas by an authorized maintainer before they affect production search.
