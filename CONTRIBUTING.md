# Contributing

Thanks for helping keep this index useful. The value of this repository is its filter, not its size — please help keep the bar high.

## Acceptance criteria

An entry is accepted only if it meets **both**:

1. **Public, working code.** The `[Code]` link must resolve to a live, non-empty repository. A README-only repo, a dead link, or "code available on request" does not qualify.
2. **Top-tier venue.** A CORE A*/A conference, or a Q1/Q2 journal (JCR). arXiv preprints are accepted only if the work is already accepted at such a venue, or is demonstrably influential (widely cited baseline).

Check ranks here:

- Conferences: https://portal.core.edu.au/conf-ranks/
- Journals: https://www.letpub.com.cn/index.php?page=journalapp
- Author/venue verification: https://dblp.org

## How to add a paper

1. Fork this repository.
2. Add your row to the correct table, keeping alphabetical/chronological order within the section.
3. Use this exact column format:

```
| Title | Affiliation | Venue | Rank | Year | [Paper](url), [Code](url) |
```

4. In your PR description, state:
   - The venue's CORE rank or JCR quartile
   - Confirmation that you opened the code link and it is non-empty
5. Open the pull request. One paper per PR is preferred.

## Reporting a broken link

Open an issue titled `[Broken link] <paper title>`. Dead code links are removed, since a dead link breaks criterion 1.

## Adding a new section

Open an issue first to discuss scope. This repository covers **security and privacy in federated recommender systems** — general federated learning, or non-federated recommender systems, are out of scope unless the work is a directly used baseline.
