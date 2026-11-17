# CAPP 30239: Data Visualization

Judy Chen

Course labs and visualization projects.

## Current submission: D3 Lab

Start with the [D3 Lab index](d3-lab/index.html), which links to all three parts:

- [Part 0: SVG Practice](d3-lab/part0.html) — SVG face and population bar charts.
- [Part 1: D3 Practice](d3-lab/part1.html) — scales, data joins, axes, and hover highlighting.
- [Part 2: Chart Replica](d3-lab/part2.html) — stacked bars comparing depression-related care by impairment group, with a legend and hover details showing respondent counts.

Part 2 uses NSDUH 2024 data. Bar percentages are weighted shares; hover counts are the unweighted numbers of survey respondents.

To view the pages, download or clone this repository and open `d3-lab/index.html` with VS Code Live Preview. GitHub file links display the HTML source rather than the rendered page.

Alternatively, run this command from the repository root and visit <http://localhost:8000/d3-lab/>:

```sh
python3 -m http.server
```

## Other course work

- [HTML/CSS Lab: Art Gallery](html-lab/index.html) — 15 artworks and an SVG house. See [artwork sources](html-lab/artwork-sources.md).
- [Altair Lab](altair-lab/altair_lab.ipynb) — visualization exercises in a Jupyter notebook. See [setup instructions](altair-lab/README.md).
- [Interactive Visualization Project](interactive-viz-project/README.md) — project overview and [Milestone 1 proposal](interactive-viz-project/milestones/interactive-proposal.md).

## File tree

Main files for the course work listed above. This section stays in the README and should be updated when coursework is added or reorganized. Archived coursework and dependency files are omitted.

```text
.
├── README.md
├── d3-lab/
│   ├── README.md
│   ├── index.html
│   ├── part0.html
│   ├── part1.html
│   ├── part2.html
│   ├── style.css
│   ├── figure8-reference.png
│   └── js/
│       └── d3.v7.js
├── html-lab/
│   ├── README.md
│   ├── index.html
│   ├── artwork-sources.md
│   └── images/
├── altair-lab/
│   ├── README.md
│   ├── altair_lab.ipynb
│   ├── data/
│   └── imgs/
└── interactive-viz-project/
    ├── README.md
    ├── data/
    │   └── README.md
    └── milestones/
        ├── interactive-proposal.md
        ├── mockup-01-disorder-overlap.png
        ├── mockup-02-life-domains.png
        └── mockup-03-care-gap.png
```
