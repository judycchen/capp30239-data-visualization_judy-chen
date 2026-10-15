# Milestone 2: Static visualization draft

Judy Chen

- [Working notebook](static-draft.ipynb)
- [Draft write-up](static-draft.md)
- [Local data setup](data/README.md)

This is a starter in progress. Figures 1–4 are implemented using real CPES data;
the remaining nine sections follow the agreed 13-figure development plan.
It is not yet the complete 8–12-image milestone submission.

## Run the notebook

Put the two source files in `data/` as described above. Alternatively, set
`CPES_DATA_PATH` and `NSDUH_DATA_PATH` to existing local files, or use
`MENTAL_HEALTH_DATA_DIR` for a directory containing both expected filenames.

From this folder, launch Jupyter with the project dependencies:

```sh
uv run jupyter lab
```

Open `static-draft.ipynb`, select the Python environment for this project, and
restart the kernel and run all cells in order. Figures are also saved in `figures/`.

To execute and save all notebook outputs without opening the editor:

```sh
uv run python -m nbconvert --to notebook --execute static-draft.ipynb --inplace
```

## Analysis conventions

- CPES: official NCS-R Part 2 + NLAAS pool; `NCNLWTLG`, `SESTRAT`, `SECLUSTR`.
- NSDUH: adults with a past-year major depressive episode, with appropriate care-response eligibility;
  `ANALWT2_C`, `VESTR_C`, `VEREP`.
- The two surveys remain separate analyses; they do not establish a historical trend.
- Never count unknown responses as no care or missing impairment as zero.
- The notebook displays aggregates rather than respondent-level extracts.

## Remaining work

Complete Figures 5–13, including CPES treatment-skip reconstruction, confidence intervals,
care comparisons, and the new alluvial and closing waffle figures. Review all images,
select 8–12 with at least five distinct types, and update the write-up before submission.
