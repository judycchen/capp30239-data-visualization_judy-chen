# Judy Chen

> Proposal starter — incomplete. Replace all TODO items and add a mockup before submitting.

## Description

I plan to build an interactive project about mental health and access to care, reusing the CPES 2001–2003 and NSDUH 2024 datasets from my static visualization project.

TODO: Define the audience, main question, and what readers should learn through interaction.

## Technical Plan: Option B

I chose Option B because my data covers several aspects of mental health, including prevalence, co-occurrence, daily-life interference, and care. One large visualization could blur these different results. Separate interactive charts would give readers more room to explore each aspect.

I also want to start with a short matching activity to draw readers into the topic. Readers could match symptom descriptions with disorder names, then see an explanation. This would introduce the terminology before moving into the survey results. The exact format is still undecided.

The main section will include at least three visualizations, with controls in at least two—for example, selecting disorders or comparing care across groups.

TODO: Specify the three visualizations and their controls, and confirm the libraries.

### Inspiration

1. **[Wordwall — Match Up](https://wordwall.net/):** Players drag terms next to their matching definitions. I could use this layout for readers to match disorder names with short symptom descriptions, then check their answers.

2. **[Wordwall — Matching Pairs](https://wordwall.net/resource/81597861/match-the-words-to-their-definitions):** Readers select related pairs of terms and descriptions. This offers an alternative to dragging: click a symptom-description card, then its matching disorder.

Both examples could inform a short opening activity that introduces the disorders before readers explore the survey results.

## Mockup

TODO: Add at least one image file in this folder and embed it here. Show the planned charts, controls, and how the view changes when a reader interacts. A hand-drawn sketch is acceptable.

## Data Sources

Dimensions and descriptions below are carried over from the static project proposal.

### Data Source 1: Collaborative Psychiatric Epidemiology Surveys (CPES), 2001–2003

URL: https://doi.org/10.3886/ICPSR20240.v9

Size: 20,013 rows, 5,543 columns

CPES combines NCS-R, NLAAS, and NSAL respondent-level surveys. It includes disorder classifications, daily-life interference, care, and demographics. The static project explored disorder prevalence, overlap, interference, and reported care. Its main treatment analysis used the NCS-R Part 2 and NLAAS sample of 10,341 respondents because question eligibility differs by survey. The interactive will need appropriate survey weights and eligibility checks as well.

TODO: Identify the specific variables and comparisons to reuse in the interactive.

### Data Source 2: National Survey on Drug Use and Health (NSDUH), 2024

URL: https://www.samhsa.gov/data/data-we-collect/nsduh-national-survey-drug-use-and-health/datafiles/2024

Size: 58,633 rows, 2,632 columns

NSDUH includes depression, functional impairment, treatment, and demographics. The static project examined adult depression and reported care using this dataset. Differences in questionnaires and disorder definitions mean CPES and NSDUH should remain separate analyses rather than a direct time trend.

TODO: Identify which contemporary comparisons will be included in the interactive.

## Questions

TODO: Add numbered questions for course staff, or state that there are none.
