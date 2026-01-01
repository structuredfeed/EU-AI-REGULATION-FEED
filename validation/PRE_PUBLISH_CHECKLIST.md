
## Release Validation Checklist

Before tagging a release, the following checks MUST pass:

### Structural Validation
- JSON validates against the locked schema (see Section 2)
- All required fields are present (nullable allowed where defined)
- No extraneous top-level keys exist

### Temporal Validation
- publication_date ≤ release cutoff date
- latest.json points to the most recent qualifying instrument
- Archive entries are immutable

### Source Integrity
- official_url resolves to an authoritative government source
- source is explicitly declared (e.g. legislation.gov.uk, eur-lex.europa.eu, congress.gov)
- EU legislative texts are reused under the EU Open Data Directive / EUR-Lex reuse policy; metadata, summaries, and links only
- No scraped or derived-only sources included

### Jurisdiction Validation
- All entries belong to the repository’s jurisdiction
- Devolved instruments are permitted and clearly labeled
- Retained EU law is permitted when clearly identified and jurisdictionally scoped
- Cross-jurisdictional instruments are excluded unless retained in law

### Semantic Validation
- AI / Digital / Data relevance flags are conservatively applied
- No record is removed solely due to uncertainty
- False positives are documented, not deleted

✔ Only after all checks pass may the repository be tagged.
