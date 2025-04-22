---
title: County-level jail incarceration and preterm birth among non-Hispanic Black and white U.S. women, 1999–2015
author:
  - Jaquelyn L. Jahn, Jarvis T. Chen, Madina Agénor, Nancy Krieger
year: 2020
journal:
  - Social Science & Medicine
type:
  - Article
---
[Zotero entry](zotero://select/items/@jahnCountylevelJailIncarceration2020)
**Tags**: #community_effects #effects_of_incarceration #incarceration #incarceration_health #multilevel_modeling 
## Abstract

Jail incarceration is widely prevalent in the United States, with disproportionate impacts on communities of color, yet little research has quantified its health consequences for communities. We assess county-level jail incarceration as a contextual stressor for individual-level preterm birth among non-Hispanic Black and White U.S. women, the vast majority (>99%) of whom were not incarcerated, between 1999 and 2015. We linked county jail incarceration rates to birth certificate data for all births to resident non-Hispanic Black and White U.S. women (N = 41, 911, 094). Using multilevel logistic regression models, we estimated the association between quintiles of county jail incarceration rates and the odds of preterm birth, adjusting for maternal- and county-level covariates and state fixed effects. Women living in counties in the highest quintile of jail incarceration rates had 1.08 (95% Confidence Interval (CI): 1.07–1.09) times greater odds of preterm birth, adjusting for covariates, compared to women living in counties with the lowest quintile of jail incarceration rates. Taken together with other research, these findings suggest policies to lower jail incarceration rates could potentially help prevent preterm birth and other adverse population health consequences of mass incarceration.

### Data

* All births to resident non-Hispanic Black and White women in the USA from 1999 to 2015 (N = 41,911,094).
	* Removed states which had integrated jails and prisons. Had 2,711 - 3,069 counties depending on the year.
	  
* **Dependent variable**: Preterm birth.
* **Independent variable**: Jail incarceration rate and categorize it into quintiles.
* **Controls**: **INDIVIDUAL**: Mother educational attainment, marital status, mother's age, mother's race/ethnicity. **COUNTY**: Urban/rural continuum, [[UCR]] crime index, % unemployed, % high school educated, [[index of concentration at the extremes]]. Data comes from [[ACS]] and values were [[linearly interpolated]].
* Sensitivity analyses where they use [[inverse probability weighting]] to address missing data and include paternal factors (high degree of missing) did not change results substantially.
### Models

* Uses [[Multilevel modeling|multilevel modeling]] [[Logistic regression]].
* Year was centered in 1999.
* State [[fixed effects]] were included.
* Random intercepts for counties.
* Random slopes for year and maternal race/ethnicity.

### Results

* For Black and White women, living in a county with a higher jail incarceration was associated with a higher likelihood of giving birth preterm.
* Estimate race-stratified models using race-specific incarceration rates and find:
	* Positive associations between race-specific incarceration rates and likelihood of race-specific preterm births.
* Estimate a new model where the key independent variable is the difference in incarceration rates between White and Black individuals and find:
	* Larger differences in incarceration rates tend to produce higher likelihoods of preterm births for Black mothers vs. White mothers, but it generally increases for both.
	* Not sure if the coefficients are significantly different.
	* At lower levels of difference in incarceration rates, there is no significant effect on preterm births on either Black or White women.