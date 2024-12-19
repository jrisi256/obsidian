---
title: County Jail Incarceration Rates and County Mortality Rates in the United States, 1987–2016
author:
  - Sandhya Kajeepeta, Caroline G. Rutherford, Katherine M. Keyes, Abdulrahman M. El-Sayed, Seth J. Prins
year: 2020
journal:
  - American Journal of Public Health
type:
  - Article
---
[Zotero entry](zotero://select/items/@kajeepetaCountyJailIncarceration2020)
**Tags**:
## Abstract

Objectives. To evaluate the relationship between changes in county jail incarceration rates and subsequent county mortality rates across the United States. Methods. We analyzed county jail incarceration rates from the Bureau of Justice Statistics from 1987 to 2016 for 1884 counties and mortality rates from the National Vital Statistics System. We fit 1-year-lagged quasi-Poisson 2-way fixed-effects models, controlling for unmeasured stable county characteristics, and measured time-varying confounders, including county poverty and crime rates. Results. A within-county increase in jail incarceration rates from the first to second quartile was associated with a 2.5% increase in mortality rates, adjusting for confounders (risk ratio RR = 1.03; 95% confidence interval CI = 1.02, 1.03). This association followed a dose–response relationship and was stronger for mortality among those aged 15 to 34 years (RR = 1.07; 95% CI = 1.06, 1.09). Conclusions. Within-county increases in jail incarceration rates are associated with increases in subsequent mortality rates after adjusting for important confounders. Public Health Implications. Our findings add to the growing body of empirical evidence of the harms of mass incarceration. The criminal justice reform and decarceration movements can use these findings as they develop strategies to end mass incarceration.

## Background

* Incarceration has spillover effects on communities --> community-level exposure. Multiple pathways link to incarceration to negative health outcomes at the community level --> destruction of community social and economic resources.
	* Prison cycling strains social service systems and disrupts local economies.
		* Removes workers from the economy and then erects barriers to gaining employment post-release contributing to inter-generational poverty.
		* Lack of adequate reentry places strain on communities social services.
	* Impedes social integration and ability for individuals to form social ties.
		* Affects community mistrust and perceived safety --> affects psychological health.
	* Inhibited social and economic resources prevent communities from developing.

## Data and Methods

* **Independent variable** --> Jail incarceration as the daily average population which comes [[Census of Jails]] and [[Annual Survey of Jails]]. from Modeled as a continuous variable and as quartiles (measured across all years across all counties).
	* Lagged by 1 year.
* County population totals come from [[PEP]].
* **Dependent variable**:
	* All-cause mortality rate across all ages.
	* Age-specific all-cause mortality.
* 29,241 county-years available for analysis (1,884 unique counties).
* **Controls** --> median age, poverty, crime, % Black, unemployment, state incarceration rate, and political party control of the state legislature.
	* Lagged by 2 years to ensure they were not mediating the effect of incarceration on mortality.
* See [[kajeepetaAssociationCountyJail2021]] as the model is very similar.
* Use [[quasi-Poisson]] regression with [[fixed effects]] for county and year.
* Sensitivity analysis (do not change results):
	* Using different jail incarceration data from [[Vera Incarceration Trends]].
	* [[Multilevel modeling]].
	* Lag party control by 3 and 4 years instead of 2.

## Results

* Higher rates of incarceration (continuous and quartile) cause higher mortality rates.
* Effects are strongest for youngest all the way up to middle age (~54). Effects begin to decline in magnitude as one looks at older age groups.
	* Larger effects for the young may reflect the direct effects of incarceration as this age group is more likely to have recently been incarcerated.

## Limitations

* How reliable is the crime data?
* Results generalize only to counties who experienced substantive changes in their jail incarceration rate.
* The county may be too large an area to accurately capture effects of incarceration.
* Auto-correlation between confounders at different time periods leading to an underestimate of the true effect? Not sure I completely understand.