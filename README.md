# WashU-Foundations of Analytics-FinalProject-2023

The assignment requires me and teammates of 4 select a problem of interest and prepare an analysis to address the problem. To do the
analysis our group finds at least 2 independent datasets that can be combined.

Our project aims to explore the potential influence of various economic and environmental factors on obesity rates among adults. We hypothesize that there is a significant relationship between these variables, where changes in economic indicators and carbon emissions may correlate with variations in obesity prevalence.

## Datasets

1. Country Economic Indicators: This dataset offers a comprehensive view of the economic health and characteristics of countries. Sourced from the Organization for Economic Co-operation and Development (OECD), it includes indicators like:
```python
gross economic output (MLN_USD)
per capita income (USD_CAP)
average wages (AVWAGE)
fertility rates (FERTILITY)
employment (EMP)
unemployment rates (UR)
average hours worked (HRWKD)
government debt (GGDEBT)
the proportion of young population (YNGPOP)
```

These indicators are pivotal in understanding the economic landscape and demographic dynamics of each country.

2. Emissions by Country: Addressing the environmental aspect, this dataset, obtained from The Global Carbon Project (GCP) quantifies carbon emissions (MtCO2) for each country. Carbon emission levels are a crucial measure of a country’s environmental impact and contribute significantly to global climate change discussions.

3. Obesity among Adults by Country: From the World Health Organization, this dataset provides statistics on the prevalence of obesity (Obesity) among adults in different countries. It's a vital health indicator, reflecting the nutritional and lifestyle aspects impacting the population.

## Hypothesis:

- Null Hypothesis (H0): There is no significant impact of the ten variables (MLN_USD, USD_CAP, AVWAGE, FERTILITY, EMP, UR, HRWKD, GGDEBT, YNGPOP, MtCO2) on adult obesity rates.
- Alternative Hypothesis (H1): At least one of the ten variables (MLN_USD, USD_CAP, AVWAGE, FERTILITY, EMP, UR, HRWKD, GGDEBT, YNGPOP, MtCO2) significantly impacts adult obesity rates.

## Methodology
After the preprocessing, we chose a fixed year (2016) for the data, which resulted in our having 30 distinct countries with features (Year, Obesity, Country_Code, MLN_USD, USD_CAP, AVWAGE, FERTILITY, EMP, UR, HRWKD, GGDEBT, YNGPOP, MtCO2). We also made 2 different attempts on our datasets. One was to delete features that were insignificant from the analysis (Delete_feature + Notable attempts.ipynb), and the other attempt was to combine features rather than delete them to retain more information (Combine_features.ipynb).

- Correlation Analysis
- Linear Regression
  - Assumption Check:
    - Collinearity
    - Linearity
    - Independent Residuals
    - Homoscedasticity
    - Residuals Normality
- Tried other models (Delete_feature + Notable attempts.ipynb):
  -   Adaboosting
  -   Gradient Boosting
  -   Random Forest

## Results
From the hypotheses and results of the study, we rejected the null hypothesis (H0). The results indicate that at least one variable (Government Debt, GGDEBT) has a statistically significant impact on adult obesity rates. Additionally, by comparing attempts 1 and 2, we discovered that combining variables retains more information in the model and improves interpretability, as opposed to simply deleting them.

## Discussion

After collecting relevant materials, we found that the surprising result may reflect complex socioeconomic dynamics (Ogden, C. L. et al, 2010). High government debt may signal broader economic pressures, which may indirectly affect obesity rates in several ways, including reduced access to healthy food, increased pressure on the population, and changes in health-related policies or funding. 

The lower R-squared values (0.49 and 0.53) suggest that the model explains less than 60% of the variability in obesity rates. Obesity is influenced by a multitude of factors including genetic, behavioral, cultural, and environmental influences that may not be fully captured by economic and environmental indicators.

Reference:
Ogden, C. L., Lamb, M. M., Carroll, M. D., & Flegal, K. M. (2010). Obesity and socioeconomic status in adults: United States 1988–1994 and 2005–2008. NCHS data brief, 50, 1-8.



