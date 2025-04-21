---
title: Incarceration and mortality in the United States
author:
  - Elias Nosrati, Jacob Kang-Brown, Michael Ash, Martin McKee, Michael Marmot, Lawrence P. King
year: 2021
journal:
  - SSM - Population Health
type:
  - Article
---
[Zotero entry](zotero://select/items/@nosratiIncarcerationMortalityUnited2021)
**Tags**: #community_effects #incarceration_health #effects_of_incarceration #incarceration #instrumental_variable #matching #fixed_effects
## Abstract

The ongoing COVID-19 pandemic has spotlighted the role of America's overcrowded prisons as vectors of ill health, but robust analyses of the degree to which high rates of incarceration impact population-level health outcomes remain scarce. In this paper, we use county-level panel data from 2927 counties across 43 states between 1983 and 2014 and a novel instrumental variable technique to study the causal effect of penal expansion on age-standardised cause-specific and all-cause mortality rates. We find that higher rates of incarceration have substantively large effects on deaths from communicable, maternal, neonatal, and nutritional diseases in the short and medium term, whilst deaths from non-communicable disease and from all causes combined are impacted in the short, medium, and long run. These findings are further corroborated by a between-unit analysis using coarsened exact matching and a simulation-based regression approach to predicting geographically anchored mortality differences.

### Mechanisms

* Worse individual health for incarcerated individuals due to increased exposure to infectious diseases and increased vulnerability in the first two weeks of release via stress-related mechanisms.
  
* Family members have lower income, lower parental investment, and unstable social relationships.
  
* Incarceration leads to the removal of prime-age working men from local communities causing the fragmentation of family relationships and the erosion of community social ties. "... the material and symbolic fabric of social life is eroded..." #quote 

## Data

County-level from 1983 to 2014.

* **Dependent variables**
	* Communicable disease mortality rate.
	* Non-communicable disease mortality rate.
	* All-cause mortality rate.
	* I will note that they said they got their data from the [[Institute for Health Metrics and Evaluation]]. When I investigated, I could not find the data they were referencing concerning mortality broken down by cause (because they do not do a very good job distinguishing between communicable vs. non-communicable).
* **Independent variables**
	* Prison admissions data from [[Vera Incarceration Trends]].
	* As they detail in [[nosratiEconomicDeclineIncarceration2019]], they drop Alaska, Connecticut, Delaware, Hawaii, Rhode Island, and Vermont because they have joint jail + prisons. They also exclude Virginia because they had consistently changing county boundaries.
	* **Controls**: Median household income, high school graduation rates, % Black, % Hispanic, % non-White other ([[ACS]]) and violent crime rate [[UCR]].

### Methods

* [[fixed effects]] for county and year using [[OLS]] regression. Independent variables are standardized. Standard errors calculated using [[robust standard errors]] (which is unclear what that means exactly).
  
* Use an [[instrumental variable]] where the first stage equation predicts the incarceration rate where the instrument is the main independent variable, and the second stage equation uses the predicted incarceration to predict the outcome.
  
* The instrument is an interacted variable that is $\overline{T_{i}} \times C_{t}$ where $\overline{T_{i}}$ is the average incarceration rate for county $i$ (across all years) and $C_{t}$ is the aggregate per capita expenditure on the construction and maintenance of correctional facilities nationally for year $t$ (data comes from [[Bureau of Justice Statistics' Justice Expenditure and Employment series]]). Missing data is imputed using a spline function.
  
* They also use [[coarsened exact matching]] to estimate the between-county effect of incarceration. Treatment, in this case, is defined as the having a *high incarceration rate* (above the mean) or having a *low incarceration rate* (below the mean). Unmatched units are pruned from the data. Using the matched data set, they regress the outcome variable on the binary incarceration variable using [[OLS]].
	* They then adopt a simulation-based approach to translate the coefficients into real estimates of how much a change in incarceration rates between counties could affect mortality. It seems to me akin to [[bootstrapped standard errors]] where you just do random pulls using your estimated model parameters and associated standard errors.
	* They then conduct a sensitivity analysis to determine the amount of confounding there would need to be to eliminate the estimated treatment effect.
	* Let $U$ be an unmeasured, binary confounder, and its effect is the same across treatment states (i.e. no interactions). The bias factor $B$ is the difference in $\beta$ (estimated treatment effect) and what $\beta$ would have been had $U$ been controlled for.
	* $\gamma = E(Y | U = 1, T, X) - E(Y | U = 0, T, X)$ --> The effect of the unmeasured confounder on the outcome.
	* $\delta = P(U = 1 | T = 1, X) - P(U = 1|T = 0, X)$ --> The difference in the prevalence of the unmeasured confounder between the treatment and control groups.
	* $B = \gamma * \delta$.
	* How large would $\gamma$ have to be to reduce $\beta$ to 0?
	* They also estimate a cross-sectional model on 2014 alone where they have access to residential segregation, unemployment, poverty, and inter-generational income mobility. Data comes from the [[Opportunity Insights]].

## Results

* From the instrumented fixed effects model, increases in the incarceration rate cause higher all-cause mortality and non-communicable mortality at the 1, 5, and 10 year mark. Also, increases in the incarceration rate cause higher (albeit much smaller) communicable mortality at the 1 and 5 year mark. Results at the 10 year mark are non-significant.
	* Results generally hold when estimating non-instrumented models.
* Between-county effects generally match the fixed effects model estimates (although they are a bit larger).
	* Robustness checks suggest that the effect of $U$ would have to be very large to eliminate the effect of $T$ even in cases where $\gamma$ is high (i.e., $U$ is much more prevalent among treated members vs. non-treated members).
	* Cross-sectional analysis also largely matches overall results (although they could only add one variable at a time due to high amounts of collinearity).

## Future work

* **Mechanisms** --> Are increases in mortality driven by incarcerated individuals or other individuals in the community being affected by higher rates of incarceration?
* How do people on probation and parole figure into this?
* Is the composition of these neighborhoods changing?
* Why are there differences across different types of mortality? And using different time lags?
* **Treatment heterogeneity** --> Are some neighborhoods more affected than others?