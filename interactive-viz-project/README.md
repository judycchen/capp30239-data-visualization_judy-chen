# Mental Health and Access to Care: Interactive Visualization

Judy Chen

## Description

CAPP 30239 interactive visualization project using the same CPES 2001–2003 and NSDUH 2024 datasets as the static visualization project.

Selected approach: **Option B — Dynamic Ensemble**. Plan for at least three distinct visualizations, with at least two supporting interactions beyond hover or tooltips. The proposal covers disorder overlap, daily-life interference, and reported care.

## Proposal

See [milestones/interactive-proposal.md](milestones/interactive-proposal.md) for the proposal, inspiration examples, and three mockup figures. The mockups use illustrative values; the implementation and library choices remain tentative.

Assignment: https://notes.jpt.sh/30239/interactive.html#milestone-1-proposal

## Data Sources

- Alegría, M., Jackson, J. S., Kessler, R. C., & Takeuchi, D. (2007). *Collaborative Psychiatric Epidemiology Surveys (CPES), 2001–2003 [United States]* (Version 9). https://doi.org/10.3886/ICPSR20240.v9
- Center for Behavioral Health Statistics and Quality. (2025). *2024 National Survey on Drug Use and Health*. https://www.samhsa.gov/data/data-we-collect/nsduh-national-survey-drug-use-and-health/datafiles/2024

See [data/README.md](data/README.md) for existing local file paths and download instructions.

## Environment

The Python dependency file follows the static project's environment and includes Altair for a possible Python-based Option B implementation. From this folder, run `uv sync` when ready to start analysis. No notebook or website has been implemented yet.

## Files

- `data/`: source-file instructions; raw files stay local.
- `milestones/`: proposal, three mockup images, and future draft documentation.
- `pyproject.toml`: Python environment dependencies.

Add an embedded screenshot and website/run instructions once the interactive exists.

AI assistance: Codex organized the project ideas into proposal text and created the illustrative mockup figures. Dataset descriptions and dimensions were carried over from the static project.
