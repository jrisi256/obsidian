---
title: "Mass incarceration and public health: The association between black jail incarceration and adverse birth outcomes among black women in Louisiana"
author:
  - Lauren Dyer, Rachel Hardeman, Dovile Vilda, Katherine Theall, Maeve Wallace
year: 2019
journal:
  - BMC Pregnancy and Childbirth
type:
  - Article
---
[Zotero entry](zotero://select/items/@dyerMassIncarcerationPublic2019)
**Tags**: #community_effects #effects_of_incarceration #incarceration #incarceration_health 
## Abstract

A growing body of evidence is beginning to highlight how mass incarceration shapes inequalities in population health. Non-Hispanic blacks are disproportionately affected by incarceration and criminal law enforcement, an enduring legacy of a racially-biased criminal justice system with broad health implications for black families and communities. Louisiana has consistently maintained one of the highest rates of black incarceration in the nation. Concurrently, large racial disparities in population health persist. We conducted a cross-sectional analysis of all births among non-Hispanic black women in Louisiana in 2014 to identify associations between parish-level (county equivalent) prevalence of jail incarceration within the black population and adverse birth outcomes (N = 23,954). We fit a log-Poisson model with generalized estimating equations to approximate the relative risk of preterm birth and low birth weight associated with an interquartile range increase in incarceration, controlling for confounders. In sensitivity analyses, we additionally adjusted for the parish-level index crime prevalence and analyzed regression models wherein white incarceration was used to predict the risk of adverse birth outcomes in order to quantify the degree to which mass incarceration may harm health above and beyond living in a high crime area. There was a significant 3% higher risk of preterm birth among black women associated with an interquartile range increase in the parish-level incarceration prevalence of black individuals, independent of other factors. Adjusting for the prevalence of index crimes did not substantively change the results of the models. Due to the positive significant associations between the prevalence of black individuals incarcerated in Louisiana jails and estimated risk of preterm birth, mass incarceration may be an underlying cause of the persistent inequities in reproductive health outcomes experienced by black women in Louisiana. Not only are there economic and social impacts stemming from mass incarceration, but there may also be implications for population health and health inequities, including the persistence of racial disparities in preterm birth and low birth weight.

### Data

* All births from non-Hispanic Black women in Louisiana in 2014 (N = 23,954).
* **Dependent variable**:
	* % of births that were preterm births.
	* % of births that were low birthweight.
* **Independent variable**: Black jail admission rate data from [[Vera Incarceration Trends]]. Standardized by its [[interquartile range]]. Available at the county level.
* **Controls**: **INDIVIDUAL**: Type of insurance, mother's age, woman's first birth or not, [[Kotelchuck Index of Prenatal Care Adequacy]] (Ratio of observed prenatal visits to the number expected based on dates of care initiation and delivery). **COUNTY**: [[Gini coefficient]], racial income inequality (absolute difference in white and black median income), % of Black individuals with a Bachelor's degree or higher, urban/rural continuum, index crime rate. Data comes from 2014 [[ACS]] and [[UCR]].

### Models

* Estimate [[Poisson regression]] models (maybe [[quasi-Poisson]] models). Used [[generalized estimating equations]] to account for clustering within counties (alternative to [[Multilevel modeling]]).

### Results

* Generally indicate that increases in jail incarceration rates are associated with worse birth outcomes.