---
title: "Economic decline, incarceration, and mortality from drug use disorders in the USA between 1983 and 2014: An observational analysis"
author:
  - Elias Nosrati, Jacob Kang-Brown, Michael Ash, Martin McKee, Michael Marmot, Lawrence P. King
year: 2019
journal:
  - The Lancet Public Health
type:
  - Article
---
[Zotero entry](zotero://select/items/@nosratiEconomicDeclineIncarceration2019)
**Tags**: #community_effects #incarceration_health #drug_overdose
## Abstract

**Background**: Drug use disorders are an increasing cause of disability and early death in the USA, with substantial geographical variation. We aimed to investigate the associations between economic decline, incarceration rates, and age-standardised mortality from drug use disorders at the county level in the USA. **Methods**: In this observational analysis, we examined age-standardised mortality data from the US National Vital Statistics System and the Institute for Health Metrics and Evaluation, household income data from the US Census Bureau, and county-level jail and prison incarceration data from the Vera Institute of Justice for 2640 US counties between 1983 and 2014. We also extracted data on county-level control variables from the US Census Bureau, the National Center for Health Statistics, and the US Centers for Disease Control and Prevention. We used a two-way fixed-effects panel regression to examine the association between reduced household income, incarceration, and mortality from drug use disorders within counties over time. To assess between-county variation, we used coarsened exact matching and a simulation-based modelling approach. **Findings**: After adjusting for key confounders, each 1 SD decrease in median household income was associated with an increase of 12·8% (95% CI 11·0–14·6; p<0·0001) in drug-related deaths within counties. Each 1 SD increase in jail and prison incarceration rates was associated with an increase of 1·5% (95% CI 1·0–2·0; p<0·0001) and 2·6% (2·1–3·1; p<0·0001) in drug-related mortality, respectively. The association between drug-related mortality and income and incarceration persisted after controlling for local opioid prescription rates. Our model accounts for a large proportion of within-county variation in mortality from drug use disorders (R2=0·975). Between counties, high rates of incarceration were associated with a more than 50% increase in drug-related deaths. **Interpretation**: Reduced household income and high incarceration rates are associated with poor health. The rapid expansion of the prison and jail population in the USA over the past four decades might have contributed to the increasing number of deaths from drug use disorders.

### Introduction

Past research has focused on the effects of increased access to opioids and declining economic health as reasons why opioid overdose have been increasing. The authors posit that the criminal justice system, and in particular, mass incarceration and the war on drugs are also important causal factors in explaining the increase in drug overdoses.

### Data

* **Dependent variable** --> Natural logarithm of the age-standardized mortality rate from drug use disorders.
* **Independent variable** --> Jail and prison incarceration rates from [[Vera Incarceration Trends]]. And also median household income.
* **Sample**: 2,640 USA counties from 1983 to 2014.
* **Controls**: Homicide rate, % Black, % Hispanic, % other non-White, county-level opioid prescription rates (2006 - 2014), % high school graduates, and all-cause mortality.

### Methods

* Linear interpolation used generate values between observations since yearly observations were not available for every variable. Independent variables were standardized. Corrected standard errors using [[autocorrelation-consistent]] and [[heteroskedasticity]]-consistent techniques.
* **Main model**: [[fixed effects]] [[OLS]] regression with fixed effects for county and year.
* They also use [[coarsened exact matching]] and (I think?) match time-averaged counties on income, education, demographics, violent crime rate, and opioid prescription rate. Counties should be similar on average on all these variables except their incarceration rate is either high (above the median) or low (below the median). They then estimated a model(?) and ran simulations based on the model to find the expected increase in the overdose rate as a result of increasing the incarceration rate.
* **Robustness**: Estimate a [[Random effects]] model (which they claim pools within-county and between-county variation) and a [[Multilevel modeling|multilevel modeling]] random intercept model (which they claim allows between-county variation in the intercept term). Although I am not sure what the difference between these two models are.

### Findings

* Income, jail admission, and prison admission all increased the rate of drug overdoses in all 3 model specifications. Effects for income were much larger. Results were robust even when controlling for overall mortality and opioid prescriptions.
* Results from matching procedure also indicate that increases in the incarceration rate lead to higher mortality.
### Discussion and Mechanisms

* Individuals involved with the criminal justice system are more likely to have substance use disorders and to die due to substance abuse.
* Incarceration leads to individuals stigma, poor mental health, and chronic economic hardship which is associated with drug use disorders.
* The incarceration of a family member leads to declining household income, reduced parental investment, unstable social relationships, and increased stress.
* Removes prime working age men from the community contributing to economic hardship in the community.
* **Overall, I find this paper weak**. The mechanisms are not well thought out.