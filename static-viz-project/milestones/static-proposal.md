# Description

My policy area is mental health and access to care. I want to explore how common different mental disorders are, how they affect daily life, and what treatment people with these disorders receive.

My main research question is: **How did reported mental health care vary by disorder type and interference with daily life among U.S. adults in 2001–2003?**

I plan to focus on major depressive disorder, generalized anxiety disorder, panic disorder, social phobia, agoraphobia without panic disorder, and PTSD. I will explore their prevalence, how often they occurred together, and whether people reporting greater interference also reported more professional help or medication use.

I envision an article in HTML or PDF with 8–10 static visualizations, moving from prevalence and overlap to daily-life impairment and care. Possible charts include prevalence bars, a co-occurrence heatmap, impairment distributions, and comparisons of care across impairment levels. I hope to see whether the most common disorders also carried the greatest burden, and how care varied with that burden. CPES will provide the historical analysis, with NSDUH 2024 adding a separate section on depression and treatment.

# Data Sources

## Data Source 1: Collaborative Psychiatric Epidemiology Surveys (CPES), 2001–2003

URL: https://www.icpsr.umich.edu/web/ICPSR/studies/20240

Size: 20,013 rows, 5,543 columns

CPES combines three adult household surveys: the National Comorbidity Survey Replication (NCS-R), National Latino and Asian American Study (NLAAS), and National Survey of American Life (NSAL). Each row represents a person. The surveys used modified versions of the WHO World Mental Health Composite International Diagnostic Interview, which asks about symptoms, duration, and timing to identify patterns meeting diagnostic criteria.

The data include disorder classifications, 0–10 ratings of interference with daily activities, professional help, medication use, and demographics such as age, education, income, and race/ethnicity. Interference measures functional impairment rather than a common clinical symptom-severity scale.

CPES is suitable for this project because it combines categorical variables, such as disorder and medication type, with numeric measures of impairment, age, and income. This supports several kinds of visualization: comparisons of prevalence, distributions of impairment scores, patterns of co-occurring disorders, and care across impairment levels or demographic groups. These layers provide enough variety for a connected suite of visualizations, with the same respondent as the common unit of analysis.

The file has been downloaded and its dimensions and relevant variables checked. I plan to use the NCS-R Part 2 and NLAAS sample of 10,341 respondents for the main analysis, since several disorder-specific treatment questions were not asked in NSAL. I will use the appropriate survey weights and check question eligibility. Medication use will describe what people with a disorder reported taking, without assuming it was prescribed for that disorder.

## Data Source 2: National Survey on Drug Use and Health (NSDUH), 2024

URL: https://www.samhsa.gov/data/data-we-collect/nsduh-national-survey-drug-use-and-health/datafiles/2024

Size: 58,633 rows, 2,632 columns

NSDUH is an annual survey of substance use, mental health, and treatment among people aged 12 and older. I will focus on adults. Its questionnaire includes depressive symptoms, major depressive episodes, interference with daily activities, professional contact and prescription medication for depressive feelings, and demographics.

NSDUH is suitable because it combines categorical variables, such as treatment receipt and age groups, with numeric ratings of depression-related interference. These measures support comparisons of professional contact and medication use across impairment levels and demographic groups. Having these answers in the same respondent record allows me to explore their relationships directly, providing several visualization options for the contemporary section.

The file has been downloaded and its dimensions verified. I will examine whether depression-related treatment differed between adults with and without severe functional impairment in 2024. This will be a separate analysis: differences in questionnaires and disorder definitions mean I will not merge respondents or present CPES and NSDUH as a direct trend over time.

# Questions

1. Is an institution-accessible ICPSR public-use dataset acceptable, and how should I provide course staff access when the original file exceeds 100 MB and redistribution is restricted?
2. Is a historical CPES analysis with a separate NSDUH 2024 section a reasonable narrative structure?
