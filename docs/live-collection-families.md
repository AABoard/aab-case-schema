# Live AAB Collection Families

Last checked against live MongoDB: 2026-05-17.

MongoDB is the live operational registry database. This repository is the public collaboration and documentation layer. Counts below are point-in-time inspection values and should be refreshed before publication or migration work.

| Collaboration family | Live MongoDB collection | Count checked | Primary role |
| --- | --- | ---: | --- |
| Cases | `cases_combined` | 140 | Structured AI education implementation cases, source-traced and public-facing where approved. |
| Pilots | `pilots` | 6 | AAB or AAB-authorized structured pilots with phase, readiness, evidence, and registry decision notes. |
| Frameworks | `frameworks` | 62 | AI literacy, education, governance, competency, and crosswalk candidate frameworks. |
| Free resources | `free-resources` | 90 | Free, open, freemium, or eligibility-based resources relevant to AI literacy and education. |
| Initiatives | `initiatives` | 94 | Public, nonprofit, academic, industry, and intergovernmental AI education initiatives. |
| Assessments and credentials | `assessments&credentialing` | 74 | Assessment systems, certificates, badges, competitions, and credentialing models. |
| Policy signals | `policies` | 195 | Country, regional, and subnational AI education policy scan records. |
| Community signals | `community-signals` | 210 | Survey, consultation, teacher, student, parent, and community evidence signals. |
| U.S. state policy signals | `us_state_policies` | 50 | State-level K-12 AI policy signal records. |
| U.S. state community signals | `us_state_community_signals` | 50 | State-level community and public-discourse signal records. |

## Common Field Families

The live collections are not identical, but they share several recurring field groups:

- Stable identity: `id`, `case_id`, `type`, `title`, `display.headline`.
- Public description: `summary`, `display.dek`, collection-specific summary fields.
- Review and publication state: `status`, `publicationStatus`, `reviewStatus`, collection-specific status fields.
- Classification: `category`, `tags`, `audience`, `region`, `statusCode`, signal-level fields.
- Source trace: `sourceUrls`, `sourceFile`, `sourceExcerpt`, `sourceDetails`, `lastVerifiedAt`.
- AAB review/rating notes: `aabRating`, `aabRatingBasis`, collection-specific rating and review fields.

## Documentation Rule

Schema docs and templates should use the live collection names above unless an environment variable explicitly maps a public category to a different MongoDB collection. Historical names such as `cases`, `registry`, `free_resources`, or `assessments_credentialing` may appear in older scripts or documentation, but should not be treated as current without verification.

## Public Claim Rule

Collection inclusion documents a source-traced evidence record. It does not imply AAB endorsement, certification, accreditation, ranking, legal advice, or final standards approval.
