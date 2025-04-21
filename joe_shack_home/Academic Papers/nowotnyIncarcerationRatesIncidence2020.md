---
title: Incarceration Rates and Incidence of Sexually Transmitted Infections in US Counties, 2011–2016
author:
  - Kathryn M. Nowotny, Marisa Omori, Melanie McKenna, Joshua Kleinman
year: 2020
journal:
  - American Journal of Public Health
type:
  - Article
---
[Zotero entry](zotero://select/items/@nowotnyIncarcerationRatesIncidence2020)
**Tags**: #community_effects #incarceration #effects_of_incarceration #incarceration_health 
## Abstract

Objectives. To examine rates of sexually transmitted infections as a function of jail and prison incarceration rates across US counties for the years 2011 to 2016. Methods. We used data from several national databases. The outcomes were county-level chlamydia and gonorrhea incidence as reported by the Centers for Disease Control and Prevention (2012–2016). The exposures were lagged specifications of county-level jail and prison incarceration rates as reported by the Vera Institute of Justice (2011–2015). We estimated mixed models to account for the 3 sources of response variable variation occurring across repeated measures collected from counties nested within states. Results. In the final model, jail and prison incarceration rates were associated with a rate increase of 10.13 per 100 000 and 8.22 per 100 000, respectively, of chlamydia incidence. The corresponding rate increases for gonorrhea incidence were 2.47 per 100 000 and 4.40 per 100 000. Conclusions. These findings provide some evidence that the documented differences in chlamydia and gonorrhea incidence between counties may be partially attributable to differences in jail and prison incarceration rates.

### Mechanisms

* Prior individual-level studies find that individuals returning from jail and prison are likely to engage in risky behaviors increasing the likelihood of both transmission and acquisition of STIs.
	* Of course, individuals who are incarcerated tended to have higher incidence STI incidence rates before incarceration, as well.
	  
* There are likely neighborhood-level effects, as well. Imbalanced sex-ratios may lead to men having more power in relationships leading to riskier sex and having sex with higher-risk partners.
  
* There have been a number of prior studies at the census tract level (focused on specific cities) or studies at the county level (focused on specific states) which demonstrated associations between higher incarceration rates and higher rates of teen pregnancy and STI transmission.

### Data and Methods

* County-level data from 2011 to 2016. 2,437 - 2,349 counties (depending on the outcome).
* **Dependent variable** --> Chlamydia and gonorrhea rates came from CDC's [[AtlasPlus]] data.
* **Independent variable** --> Jail and incarceration rates from [[Vera Incarceration Trends]]. I believe these variables are standardized?
* **Controls** --> 1) Urban/rural continuum, 2) Black female-to-male sex ratio, 3) Black-white segregation, 4) % of population that is working age, 5) % children living in poverty, % high school graduates, 6) Categorical variable for year, 7) Categorical variable for US census region. Data came from [[ACS]], [[SAIPE]], [[County Health Rankings and Roadmap tool]], and [[Brown University American Communities Project]].
* Estimated [[Random effects]] [[OLS]] models with [[Clustered standard errors]] for state.
	* Explore 1 and 2 year lags for the incarceration rates. Using a different modeling procedure?
	* Estimate [[mixed effects]] models too?
	* This section is a mess. They do not clearly explain what they are doing.
		* They [[grand mean center]] all their control variables so I am interpreting that to mean they are between-county estimates.
	* I think they [[grand mean center]] time as well. Theoretically, I think that makes it so that you interpret it as STI rates have gone up/down over time, generally.
### Results

Basically, increases in jail and incarceration were associated with increases in the incidence rate of the STIs.