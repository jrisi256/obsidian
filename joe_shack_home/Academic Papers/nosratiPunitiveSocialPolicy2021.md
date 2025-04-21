---
title: Punitive Social Policy and Vital Inequality
author:
  - Elias Nosrati, Lawrence P. King
year: 2021
journal:
  - International Journal of Health Services
type:
  - Article
---
[Zotero entry](zotero://select/items/@nosratiPunitiveSocialPolicy2021)
**Tags**: #community_effects #incarceration_health #effects_of_incarceration #incarceration #instrumental_variable #matching #fixed_effects 
## Abstract

Geographical inequalities in life and death are among the world's most pronounced in the United States. However, the driving forces behind this macroscopic variation in population health outcomes remain surprisingly understudied, both empirically and theoretically. The present article steps into this breach by assessing a number of theoretically informed hypotheses surrounding the underlying causes of such spatial heterogeneity. Above and beyond a range of usual suspects, such as poverty, unemployment, and ethno-racial disparities, we find that a hitherto neglected explanans is prison incarceration. In particular, through the use of previously unavailable county-level panel data and a compound instrumentation technique suited to isolating exogenous treatment variation, high imprisonment rates are shown to substantially increase the population-wide risk of premature death. Our findings contribute to the political economy of population health by relating the rise of the carceral state to the amplification of geographically anchored unequal life chances.

### Mechanisms

1. Incarceration, as a policy affecting neighborhoods, causes groups of people to experience downward social mobility. It subjects groups of people to physical seclusion and marks them with a criminal record causing material and symbolic stigma. These neighborhoods also experience the removal of working-age men causing economic disruption and inhibiting the formation of social ties within communities and across communities.
2. Incarceration amplifies already existing disadvantages --> e.g., individuals who have been incarcerated are at much, much higher risk of winding up homeless.
3. Closely related to point 1, incarceration leads to the corrosion of neighborhoods. It causes a decline in social cohesion and disrupts social networks and leads to an increase in neighborhood violence, ultimately.

Incarceration operates through two different time-horizons:
1. Acute effects --> E.g., adverse experiences of parental incarceration on children.
2. Chronic effects --> Chronic exposure to the stressors of everyday life in communities harmed by high rates of mass incarceration leads to higher wear and tear. It causes biological burdens. High, chronic stress is embedded in the neuroendocrine system.

### Data and methods

* **Dependent variables** --> 1) Life expectancy at birth, 2) probability of dying between ages 25 and 45, and 3) probability of dying between ages 45 and 65. Data comes from the [[Institute for Health Metrics and Evaluation]].
* **Independent variables** (varies depending on the exact model being estimated): 1) Median household income, 2) unemployment, 3) labor force participation, 4) poverty, 5) income mobility (percent of children who earn more than their parents), 6) income inequality (Gini index), 7) residential segregation by race, 8) % Black, 9) % Hispanic, 10) % other non-White, 11) % high school graduate, 12) % without health insurance, 13) violent crime rates, and 14) **prison incarceration rates**. Data comes from the [[ACS]], [[UCR]], [[Opportunity Insights]], and [[Vera Incarceration Trends]].
	* They also included a hand-coded binary indicator of whether a state is a former slave state or not.
* The exact methods and sample construction are very similar (if not exactly the same) as [[nosratiIncarcerationMortalityUnited2021]].
	* Independent variables are standardized.
	* Prison incarceration is lagged for 1 year, 5 years, and 10 years.
	* Dependent variables are log-transformed.
	* They say standard errors are "... [[autocorrelation-consistent]], [[heteroskedasticity]]-consistent, and [[Clustered standard errors]]". Not sure what this means, exactly.

### Findings

* Instrumented fixed effect models indicate that increases in the incarceration rate cause declines in life expectancy and increases in the probability of death.
	* Confounding sensitivity analysis suggests any unmeasured confounders would have to have a large effect (or it would have to way more prevalent in treated counties). If you believe the confounder is much more prevalent in treated counties, the effect of the confounder would only have to be roughly equal to the effect of incarceration.
	  
* Results from the matching process given a between-county causal estimator which also suggests incarceration has negative effects on community health.
	* Confounding sensitivity analysis has similar conclusions as the sensitivity analysis conducted using the fixed effects approach.