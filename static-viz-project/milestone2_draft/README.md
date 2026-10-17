# Milestone 2: Static visualization draft

Judy Chen

- [Notebook: code and all 11 figures](static-draft.ipynb)
- [Draft write-up: 10 main figures and an optional experiment](static-draft.md)
- [Local data setup](data/README.md)

All figures use real data and Altair, with a small shared theme. Figure 10 is an optional alluvial experiment; the other ten figures form the main draft.

Generative AI assistance is documented in [AI.md](AI.md).

The chart functions use explicit encodings, layers, facets, normalized stacks, and rectangular heatmaps. Survey-weighted summaries are calculated before plotting. The combination chart combines bars and a dot matrix; the optional alluvial adds area marks for the ribbons.

## Design choices

The figures are intended to be read together. Each keeps a short source line; shared methods appear once in the notebook introduction and draft, with figure-specific context in the accompanying text.

One shared [ColorBrewer Dark2 palette](https://colorbrewer2.org/?type=qualitative&scheme=Dark2&n=6) assigns a fixed hue to each disorder in Figures 01, 03, 04, 05, 06, and 08. The assignments are defined once in `DISORDER_COLORS`. In the combination plot, colored dots identify disorders present, pale gray dots indicate disorders absent, and faint row bands repeat the fixed disorder colors. Gray bars represent exact combinations. In Figure 08, color identifies the disorder, while solid circles and dashed triangles distinguish professional care and antidepressant use. Heatmap colors represent numeric percentages, and the 2024 figures use a separate palette for care categories, with orange consistently identifying neither care form. Figure 04 aligns the six interference distributions in one column, with dots at the observed scores and gently curved guides between them; every row uses the same percentage scale. Small multiples share their scales and bar lengths start at zero. The alluvial remains optional because crossing translucent ribbons make exact comparisons difficult; Figure 11 provides the direct comparison with uncertainty.

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
