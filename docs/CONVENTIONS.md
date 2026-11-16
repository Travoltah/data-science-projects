# Conventions

Rules that keep every project in this repository consistent, safe to publish, and easy to follow.

## Naming
- Project folders: `NN-short-kebab-name` (e.g. `02-mobile-money-sentiment-analysis`), numbered by project type: machine learning first, then dashboards.
- Notebooks: `NN-what-it-does.ipynb` when there is more than one, numbered in the order they should be run.
- File names never contain student numbers, staff numbers or other personal identifiers.

## Privacy checklist (before every commit)
Notebook **outputs** are the usual leak: a `df.head()` or a printed API response is published with the notebook.

- [ ] No API keys, tokens or passwords in code or outputs. Credentials are read from environment variables (`os.environ[...]`).
- [ ] No personal data in outputs: names of private individuals, social-media handles, phone numbers, emails, account or loan numbers. Mask them (`@user`, `LN-00001`) or clear the output.
- [ ] No confidential data from employers or clients. Name an organisation only when the data is public; otherwise describe it (e.g. "a commercial bank").
- [ ] Raw datasets are only committed when their licence allows it and they hold no personal data. Otherwise the README says where the data came from.
- [ ] Images: only your own charts and screenshots, or images whose licence allows reuse. No unrelated stock photos or third-party branding.
- [ ] Run a secret scan before pushing: `docker run --rm -v "$PWD:/repo" zricethezav/gitleaks:v8.21.2 dir /repo`.

## Documentation standard
Every project README answers, in this order:
1. **What and why**: the question in plain language, and who would use the answer.
2. **Approach**: data, cleaning decisions, method, with a Mermaid diagram of the flow.
3. **Results**: real numbers from the notebook, compared with a simple baseline (majority class, naive forecast).
4. **What's in this folder** and **how to run it**.
5. **Data, privacy & limitations**: sources and licences, what was masked, and what the results can't support.
6. **Next steps.**

Only publish numbers that the notebook actually produced. If a result is weak, say so and say why; that is more useful than a flattering number.

## Commit messages
[Conventional Commits](https://www.conventionalcommits.org/): `feat(loan): add class-weighted model`, `fix(sentiment): mask phone numbers in outputs`, `docs: update project table`.
