# Milestone 2: Static visualization draft

Judy Chen

- [Notebook: code and all 13 figures](static-draft.ipynb)
- [Draft write-up: 12 selected figures](static-draft.md)
- [Local data setup](data/README.md)

All figures use real data and a shared custom theme. Figure 02 remains in the notebook as an additional comparison; the write-up selects the other 12 for review.

## Run

Place the source files in `data/` following its README. Alternatively, set `CPES_DATA_PATH` and `NSDUH_DATA_PATH` to their locations.

From this folder:

```sh
uv run jupyter lab
```

Open `static-draft.ipynb` and run all cells in order. Images are saved in `figures/`. `pyproject.toml` lists the required packages; it is a reproducibility aid, not a Milestone 2 requirement.

To rerun without opening Jupyter:

```sh
uv run python -m nbconvert --to notebook --execute static-draft.ipynb --inplace
```

## Analysis notes

CPES uses the NCS-R Part 2 + NLAAS pool (`NCNLWTLG`, `SESTRAT`, `SECLUSTR`). NSDUH uses `ANALWT2_C`, `VESTR_C`, and `VEREP`. Confidence intervals use Taylor linearization with the released strata and clusters. The surveys are analyzed separately.

For CPES care, explicit lifetime “never” responses supply a past-year “no” only when the past-year item is skipped. The matched lifetime / past-year variables are `V00995` / `V01013`, `V01874` / `V01891`, `V01357` / `V01394`, `V01583` / `V01621`, and `V01697` / `V01734`. PTSD uses explicit responses to `V04040`; an answer about a selected lifetime event cannot establish past-year care for all events.

Medication cells require at least 50 valid responses, at least five users and five nonusers, and a relative standard error no greater than 30%. Other cells are gray. Physical-problem-only medication responses are excluded. Unknown responses are never counted as no care or zero interference.
