# Data Dictionary Starter

This file defines common fields that should stay consistent across AAB registry collections. Collection-specific fields should be documented in the relevant schema file.

## Common Identity Fields

| Field | Meaning |
| --- | --- |
| `id` | Stable public or internal record identifier. |
| `type` | Registry record family, such as `case`, `pilot`, `framework`, `policy`, or `community_signal`. |
| `title` | Human-readable record title. |
| `summary` | Short public-facing summary. |
| `status` | Review or publication status. |
| `publicationStatus` | Public display readiness when separate from review status. |

## Source Trace Fields

| Field | Meaning |
| --- | --- |
| `sourceUrls` | Public URLs used to support the record. |
| `sourceFile` | Local or archival source file reference when applicable. |
| `sourcePath` | Path to source evidence in an AAB workspace or export. |
| `lastVerifiedAt` | Date when source evidence was last checked. |
| `reviewNotes` | Public-safe review notes or limitations. |

## Date Fields

Use ISO date strings where possible. If the exact date is unknown, preserve the source wording in a separate note rather than inventing precision.

## Status Caution

Status fields must not imply endorsement, certification, accreditation, or final AAB approval unless an explicit governance or standards process has approved that language.
