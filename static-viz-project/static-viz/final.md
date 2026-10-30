# Mental disorders, daily-life interference, and reported care

Judy Chen

## What is your current goal? Has it changed since the proposal?

My goal is still to compare six mental disorders: how common they were, how much they interfered with daily life, and what care people reported. Most figures use CPES from 2001–2003. The last three use NSDUH 2024 to look at depression more recently, because it asks about depression, impairment, and care together.

## Are there data challenges you are facing? Are you currently depending on mock data?

All 11 figures use real data. CPES has 20,013 respondents, and I use the 10,341 in the NCS-R Part 2 + NLAAS sample. NSDUH has 58,633 respondents, including 5,205 adults with past-year depression.

The main challenges are skipped questions and missing answers. PTSD care and interference questions cover a smaller, event-specific group. In NSDUH, 197 respondents with depression have unknown care status and are excluded, leaving 5,008. I analyze the surveys separately because their questionnaires differ.

Percentages and averages use survey weights; n counts respondents, and error bars show 95% confidence intervals. Interference scores run from 0 (none) to 10 (very severe) and describe the worst period of the past year. Here, agoraphobia refers to the diagnosis without panic disorder.

## Key terms

**The six disorders**

- **Depression** (major depressive disorder): at least two weeks of low mood or lost interest in most activities, with other symptoms such as sleep or concentration problems.
- **Generalized anxiety** (generalized anxiety disorder): persistent, hard-to-control worry about many everyday things.
- **Panic disorder**: repeated, unexpected panic attacks, with ongoing worry about having more.
- **Social phobia** (also called social anxiety disorder): intense fear of social or performance situations where a person might be judged.
- **Agoraphobia**: fear and avoidance of places where escape or help might be hard, such as crowds or public transport. Here it means agoraphobia *without* panic disorder.
- **PTSD** (post-traumatic stress disorder): lasting distress after a traumatic event, such as intrusive memories, avoidance, and feeling on edge.

**How to read the numbers**

- **Past-year prevalence**: the share of adults who met the criteria for a disorder at some point in the 12 months before their interview.
- **Survey weights**: the survey did not sample everyone with equal chance, so each answer is weighted to make the results represent U.S. adults. "Weighted" percentages and averages use these weights.
- **95% confidence interval**: the range of values consistent with the data, given that this is a sample. Wider intervals mean less certainty, usually because fewer people answered.
- **Co-occurring disorders**: having more than one of the six disorders in the same year. A person can appear in several disorder groups, so the groups overlap.
- **Interference score**: how much a disorder got in the way of daily life during its worst period in the past year, from 0 (none) to 10 (very severe). It is asked separately for home management, close relationships, and social life.
- **n**: the number of survey respondents behind an estimate.

## Describe each of the provided images with 2-3 sentences to give the context and how it relates to your goal.

### Figure 1: Past-year prevalence

![Past-year prevalence](figures/1.png)

Depression and social phobia were the most common of the six disorders. Prevalence is weighted, so the shares estimate how many U.S. adults had each disorder in the past 12 months; black lines show 95% confidence intervals. The chart spells out post-traumatic stress disorder (PTSD) and agoraphobia without panic disorder (see Key terms). This gives a starting point for comparing how many people were affected and what care they reported.

### Figure 2: Which disorders occurred together?

![Which disorders occurred together?](figures/2.png)

Each row starts with people who had one disorder and shows what percentage also had each other disorder, so a row reads left to right from the label at its start to the column labels across the top. The percentages differ across the diagonal because each row starts with a different group of people. This shows common overlaps before the next figure breaks down exact combinations.

### Figure 3: Which disorder combinations were most common?

![Which disorder combinations were most common?](figures/3.png)

This shows the ten most common exact combinations among 754 respondents with at least two selected disorders; the remaining combinations account for 36.5%. Colored, connected dots show which disorders belong to each combination, and each disorder name matches its dot color. For example, the first bar represents depression and social phobia without any of the other four selected disorders.

### Figure 4: Social-life interference distributions

![Social-life interference distributions](figures/4.png)

These rows show how social-life interference scores, from 0 (none) to 10 (very severe), were spread within each disorder. Scores are whole numbers, so each one gets its own bar, and a dashed line marks each group's average. Every group spans the full scale; averages range from 4.4 for panic disorder to 5.9 for agoraphobia.

### Figure 5: Daily-life domains

![Daily-life domains](figures/5.png)

This compares average interference with home management, close relationships, and social life for each disorder. Each symbol is one domain's average: a house for home management, a heart for close relationships, and a star for social life. Each domain sits on its own line within a row, so the symbols do not overlap. The shaded strip spans each group's lowest to highest domain average; it is not a confidence interval. For social phobia, social life was more affected than home management, with average scores of 5.1 and 2.5.

### Figure 6: Disorder-specific professional care

![Disorder-specific professional care](figures/6.png)

Among respondents with known care answers, this shows the percentage who reported professional help for their disorder in the past year; black lines show 95% confidence intervals. Social phobia had the lowest reported rate of care.

### Figure 7: Medication classes

![Medication classes](figures/7.png)

Antidepressants were the most frequently reported medication class in all six groups. People may have used medication for another condition, so this does not tell us what each prescription was for. Some medication categories have few reported users.

### Figure 8: Interference and reported care

![Interference and reported care](figures/8.png)

Each disorder is split into three social-life interference groups (0 = none, 10 = very severe), with the respondent count above each score range. Solid lines show professional help for that disorder; dashed lines show antidepressant use, which may have been for another condition. Both lines describe the same people, and vertical lines show 95% confidence intervals. Antidepressant use is the one medication question asked of everyone, so it gives a broader view of treatment next to disorder-specific professional help. Both were reported more often in the highest score group than in the lowest for all six disorders.

### Figure 9: Depression-related care in 2024

![Depression-related care in 2024](figures/9.png)

These bars show the combinations of professional contact and prescription medication reported for depressive feelings among adults with past-year depression in 2024. Neither was reported by 29.5% of those with severe impairment and 41.2% of those without severe impairment.

### Figure 10: Insurance and reported care

![Insurance and reported care](figures/10.png)

Among adults with depression and severe impairment, 61.1% of uninsured adults reported neither care form, compared with 25.9% of insured adults. Black lines show 95% confidence intervals. This compares two groups; it does not show that insurance caused the difference.

### Figure 11: Impairment, insurance, and care

![Impairment, insurance, and care](figures/11.png)

These ribbons connect impairment, insurance, and reported care for the same people. Their widths show shares of the full sample, so they should not be read as treatment rates within each group.

## What form do you envision your final narrative taking? (e.g. An article incorporating the images? A poster? An infographic?)

I plan to make an HTML or PDF article, starting with how common the disorders were and how often they overlapped, then moving to daily-life interference and care. A short final section will look at depression in 2024.

Sources: [CPES](https://www.icpsr.umich.edu/web/ICPSR/studies/20240) and [NSDUH 2024](https://www.samhsa.gov/data/data-we-collect/nsduh-national-survey-drug-use-and-health/datafiles/2024). The [notebook](../src/static_viz.ipynb) contains the code and run instructions; [data/README.md](../data/README.md) lists the source files.
