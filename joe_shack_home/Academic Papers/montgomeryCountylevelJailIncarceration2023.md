---
title: County-level jail incarceration, community economic distress, rurality, and preterm birth among women in the US South
author:
  - Brooke E. E. Montgomery, George C. Pro, Don E. Willis, Nick D. Zaller
year: 2023
journal:
  - Journal of Clinical and Translational Science
type:
  - Article
---
[Zotero entry](zotero://select/items/@montgomeryCountylevelJailIncarceration2023)
**Tags**: #community_effects #effects_of_incarceration #incarceration #incarceration_health 
## Abstract

Introduction:The USA has higher rates of preterm birth and incarceration than any other developed nation, with rates of both being highest in Southern states and among Black Americans, potentially due to rurality and socioeconomic factors. To test our hypothesis that prior-year county-level rates of jail admission, economic distress, and rurality were positively associated with premature birth rates in the county of delivery in 2019 and that the strength of these associations is greater for Black women than for White or Hispanic women, we merged five datasets to perform multivariable analysis of data from 766 counties across 12 Southern/rural states.Methods:We used multivariable linear regression to model the percentage of babies born premature, stratified by Black (Model 1), Hispanic (Model 2), and White (Model 3) mothers. Each model included all three independent variables of interest measured using data from the Vera Institute, Distressed Communities Index, and Index of Relative Rurality.Results:In fully fitted stratified models, economic distress was positively associated with premature births among Black (F = 33.81, p < 0.0001) and White (F = 26.50, p < 0.0001) mothers. Rurality was associated with premature births among White mothers (F = 20.02, p < 0.0001). Jail admission rate was not associated with premature births among any racial group, and none of the study variables were associated with premature births among Hispanic mothers.Conclusions:Understanding the connections between preterm birth and enduring structural inequities is a necessary scientific endeavor to advance to later translational stages in health-disparities research

### Data and Methods

* **Unit of analysis** --> 766 counties in 12 Southern states in 2019.
* **Dependent variable** --> Percentage of births which were preterm births. Data comes from the CDC's [[National Environmental Public Health Tracking System]]. Data is [[Log transform]].
* **Independent variable** --> Jail admission data from [[Vera Incarceration Trends]].
	* Lag the variable by 1 year.
* **Controls**:
	* Use the [[Distressed Communities Index]] which pools observations from 2015 - 2019: 1) education, 2) unemployment, 3) poverty, 4) median household income, 5) percentage of unoccupied habitable housing, 6) percent change in the number of available jobs, 7) percent change in the number of business establishments.
	* Also use the [[Index of Relative Rurality]]. 1) Population size, 2) Population density, 3) Distance to nearest metropolitan area, and 4) percent of total land area that is urbanized or built-up.
* **Methods** --> They use [[OLS]] regression. They also stratify their models by race (White, Black, Hispanic).

### Results

* Jail admission rates were not significantly associated with preterm births when including the control variables for any of the racial groups. By itself, it was only associated with higher preterm births for White mothers.