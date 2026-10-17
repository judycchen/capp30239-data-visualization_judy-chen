# Mental disorders, daily-life interference, and reported care

Judy Chen

## Milestone 2 submission

- [Draft write-up and all 11 images](static-draft.md)
- [Notebook with Python code and executed figures](static-draft.ipynb)
- [Data sources and local file setup](data/README.md)
- [AI-use disclosure](AI.md)

The draft contains ten main figures and one optional alluvial experiment at the end. All images use real data. Chart types include bars, heatmaps, a disorder-combination matrix, ridgeline distributions, connected-dot plots, line charts, and an alluvial diagram.

Figures 01–08 compare six disorders using CPES 2001–2003. Figures 09–11 use NSDUH 2024 as a separate depression case study because its questionnaire links depression, impairment, and care. The surveys are not treated as a trend over time.

## Run the notebook

Use Python 3.11 or newer. From this folder, install the packages and open JupyterLab:

```sh
python -m pip install "altair>=6.3,<7" numpy pandas scipy vl-convert-python jupyterlab ipykernel nbconvert
python -m jupyterlab
```

Place the two source files in `data/` as described in its [README](data/README.md). Open `static-draft.ipynb`, restart the kernel, and run all cells in order. The notebook displays the figures and saves PNG copies in `figures/`.

To run without opening JupyterLab:

```sh
python -m nbconvert --to notebook --execute static-draft.ipynb --inplace
```

## Design and analysis notes

All figures use a shared Arial theme with white backgrounds and light gridlines. A fixed [ColorBrewer Dark2 palette](https://colorbrewer2.org/?type=qualitative&scheme=Dark2&n=6) identifies disorders. Figure 09 uses green for both care forms, blue for professional contact only, red for medication only, and gray for neither. Figure 10 keeps gray for neither; Figure 11 uses sage, ochre, and plum for its columns, with blue and gray care ribbons.

Percentages and means use survey weights; n counts actual respondents. Error bars show survey-design 95% confidence intervals calculated by `survey_mean()`. CPES uses `NCNLWTLG`, `SESTRAT`, and `SECLUSTR`; NSDUH uses `ANALWT2_C`, `VESTR_C`, and `VEREP`.

Unknown responses are excluded rather than counted as no care. In Figure 08, both care measures use the same respondents within each disorder and interference band; counts appear beneath the score labels. CPES medication use may concern another condition, and PTSD questions cover a narrower event-specific subset. The draft write-up explains these limitations alongside the figures.
