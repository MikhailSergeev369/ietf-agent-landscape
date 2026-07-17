# Contributing to the IETF Agent Landscape

Thank you for considering a contribution. This document exists because the agent-standards space at IETF has grown beyond what any single participant can track alone. Community contributions keep it accurate and current.

## Ground rules

**Neutrality on scope questions.** This document catalogues what exists rather than advocating for specific proposals. Descriptions should be factual. Where a draft's approach is genuinely distinctive, describe the mechanism rather than editorializing about whether it succeeds.

**Attribution accuracy.** Authors, affiliations, and dates should match the Datatracker entry. If a draft has moved from individual submission to WG stream (draft-lastname-* becoming draft-ietf-*), update the reference and note the transition.

**Category placement.** Categories reflect architectural role. A draft that touches multiple areas belongs primarily where its main scope lands, with cross-references to secondary categories. When in doubt, file an issue for discussion before opening a pull request.

## What kinds of changes are welcome

### Additions
- New Internet-Drafts in the agent space (any category)
- New chartered WGs or forming BoFs
- New mailing lists or coordination venues
- New external protocols or industry efforts referenced by IETF work

### Corrections
- Incorrect draft names, author attributions, or affiliations
- Outdated version references
- Superseded drafts (add successor, note history if relevant)
- Miscategorization

### Improvements
- Clearer descriptions of draft approaches
- Better cross-references between categories
- Additional context about venues or coordination efforts
- Style consistency

### Structural changes
- New categories (with justification via issue first)
- Renaming or merging categories (with justification via issue first)
- Adding subcategories

Structural changes should be discussed via issue before pull request to reduce merge conflicts.

## How to contribute

### Filing an issue

For small corrections, missing drafts, or observations, file an issue. Include:
- The change you're proposing
- Reasoning if the change is non-obvious
- Citation to Datatracker if adding a draft

### Opening a pull request

For additions and clear-cut corrections, open a PR directly.

1. Fork the repository
2. Create a branch (`git checkout -b add-draft-example`)
3. Make your edits to `agent-standards-landscape.md`
4. Verify links resolve (all draft references should link to `datatracker.ietf.org`)
5. Verify formatting matches existing entries in the same category
6. Commit with a clear message
7. Open a pull request against `main`

### Adding a draft

The standard format for a draft entry:

```markdown
- [draft-author-topic](https://datatracker.ietf.org/doc/draft-author-topic/) (Author, Affiliation; version and date if notable) — brief description of what the draft does, its architectural approach, and its relationship to other work in the category.
```

Descriptions should be 1-3 sentences typically. Longer descriptions are appropriate for architecturally significant work but should stay factual.

### Style conventions

- All draft references link to `datatracker.ietf.org/doc/draft-name/` (Datatracker auto-redirects to current version)
- Entries within a category are alphabetical by draft name
- Author affiliations use organization name, not personal titles
- Cross-references between categories use "(see Category N)" format
- External protocols and industry efforts go in the separate `**External protocols & industry**` subsection

## Style guide

This document uses IETF-friendly plain prose. Specific conventions:

- No em dashes (use parentheses or restructure)
- Avoid negative contractions (`isn't`, `don't`, `can't`)
- Prefer active voice
- Technical accuracy over marketing language
- Neutral tone on contested categorization questions

## Co-authorship

The current maintainer welcomes co-authors who agree with the general approach of the document. Co-authorship means:

- Named in the document header
- Named in AUTHORS.md
- Named on any I-D snapshots filed to the Independent Submission Stream
- Merge rights on the repository

If you are interested in co-authorship, file an issue titled "Co-authorship inquiry" describing your interest and the perspective you would bring. This is not a lightweight commitment; co-authors are expected to review PRs, respond to issues in their areas of expertise, and help maintain the document over time.

## Code of conduct

Discussion in issues and PRs should be technical, substantive, and respectful. Disagreements about categorization or scope are welcome. Personal attacks, promotional posts, or bad-faith engagement are not.

The IETF Note Well applies to any material that references or is derived from this repository.

## Questions

For questions that aren't covered by an issue, contact the current maintainer directly (see README.md for contact information).
