# Milestone 2: Static visualization draft

Judy Chen

- [Notebook: code and all 11 figures](static-draft.ipynb)
- [Draft write-up: 10 main figures and an optional experiment](static-draft.md)
- [Local data setup](data/README.md)

All figures use real data and Altair, with a small shared theme. Figure 10 is an optional alluvial experiment; the other ten figures form the main draft.

Generative AI assistance is documented in [AI.md](AI.md).

The chart functions use explicit encodings, layers, facets, normalized stacks, and rectangular heatmaps. Survey-weighted summaries are calculated before plotting. The UpSet combines bars, rules, and points; the optional alluvial adds area marks for the ribbons.

## Design choices

Blue emphasizes the main comparisons, purple identifies antidepressant use in Figure 08, and orange consistently identifies neither care form in the 2024 section. Heatmaps use sequential colors, with black or white labels chosen for contrast. Small multiples share their scales, bar lengths start at zero, and Figure 09 keeps the orange segment at a common right edge. Figure 07 shows all five medication classes as descriptive percentages. The alluvial remains optional because crossing translucent ribbons make exact comparisons difficult; Figure 11 provides the direct comparison with uncertainty.

## Run

Place the two source files in `data/` following its README.

From this folder:

```sh
uv run jupyter lab
```

Open `static-draft.ipynb` and run all cells in order. Altair exports static PNG images to `figures/` using `vl-convert-python`; the notebook displays the same static charts. `pyproject.toml` lists the required packages.

To rerun without opening Jupyter:

```sh
uv run python -m nbconvert --to notebook --execute static-draft.ipynb --inplace
```

## Analysis notes

CPES uses the NCS-R Part 2 + NLAAS pool (`NCNLWTLG`, `SESTRAT`, `SECLUSTR`). NSDUH uses `ANALWT2_C`, `VESTR_C`, and `VEREP`. The surveys are analyzed separately.

`survey_mean()` calculates weighted means or proportions, then uses Taylor linearization to estimate uncertainty from variation between sampling clusters within strata. It retains the full survey design when estimating a subgroup, and its 95% confidence intervals use a t critical value with cluster-minus-stratum degrees of freedom. This method accounts for the complex samples; ordinary independent-observation error bars would not. Intervals describe sampling uncertainty and do not resolve missing-response bias or questionnaire differences.

Figure 08 combines the former medication-by-interference and disorder-level scatterplot questions into six panels. Within each disorder and score band, both measures use respondents with valid interference, professional-care, and antidepressant responses; their denominators therefore match. Counts are unweighted, percentages are weighted, the measures can overlap, and connecting lines only guide comparison between the three bands. Some agoraphobia bands have fewer than 50 respondents, so their intervals are wide. These estimates describe associations, not the effect of impairment on treatment.

For CPES care, explicit lifetime “never” responses supply a past-year “no” only when the past-year item is skipped. The matched lifetime / past-year variables are `V00995` / `V01013`, `V01874` / `V01891`, `V01357` / `V01394`, `V01583` / `V01621`, and `V01697` / `V01734`. PTSD uses explicit responses to `V04040`; an answer about a selected lifetime event cannot establish past-year care for all events.

Figure 07 shows all 30 weighted medication estimates. Some, particularly stimulant use, are based on relatively few reported users and should be read as exploratory descriptions. Physical-problem-only medication responses are excluded. Unknown responses are never counted as no care or zero interference.
