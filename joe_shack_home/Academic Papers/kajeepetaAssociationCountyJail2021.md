---
title: "Association between county jail incarceration and cause-specific county mortality in the USA, 1987-2017: A retrospective, longitudinal study"
author:
  - Sandhya Kajeepeta, Pia M. Mauro, Katherine M. Keyes, Abdulrahman M. El-Sayed, Caroline G. Rutherford, Seth J. Prins
year: 2021
journal:
  - The Lancet. Public Health
type:
  - Article
---
[Zotero entry](zotero://select/items/@kajeepetaAssociationCountyJail2021)
**Tags**: #incarceration #jails #effects_of_incarceration #community_effects #incarceration_health #incarceration_paper 
## Abstract

BACKGROUND: Mass incarceration has collateral consequences for community health, which are reflected in county-level health indicators, including county mortality rates. County jail incarceration rates are associated with all-cause mortality rates in the USA. We assessed the causes of death that drive the relationship between county-level jail incarceration and mortality. METHODS: In this retrospective, longitudinal study, we assessed the association between county-level jail incarceration rates and county-level cause-specific mortality using county jail incarceration data (1987-2017) for 1094 counties in the USA obtained from the Vera Institute of Justice and cause-specific mortality data for individuals younger than 75 years in the total county population (1988-2018) obtained from the US National Vital Statistics System. We fitted quasi-Poisson models for nine common causes of death (cerebrovascular disease, chronic lower respiratory disease, diabetes, heart disease, infectious disease, malignant neoplasm, substance use, suicide, and unintentional injury) with county fixed effects, controlling for all unmeasured stable county characteristics and measured time-varying confounders (county median age, county poverty rate, county percentage of Black residents, county crime rate, county unemployment rate, and state incarceration rate). We lagged county jail incarceration rates by 1 year to assess the short-term, by 5 years to assess the medium-term, and by 10 years to assess the long-term associations of jail incarceration with premature mortality. FINDINGS: A 1 per 1000 within-county increase in jail incarceration rate was associated with a 6⋅5% increase in mortality from infectious diseases (risk ratio 1⋅065, 95% CI 1⋅061-1⋅070), a 4⋅9% increase in mortality from chronic lower respiratory disease (1⋅049, 1⋅045-1⋅052), a 2⋅6% increase in mortality induced from substance use (1⋅026, 1⋅020-1⋅032), a 2⋅5% increase in suicide mortality (1⋅025, 1⋅020-1⋅029), and smaller increases in mortality from heart disease (1⋅021, 1⋅019-1⋅023), unintentional injury (1⋅015, 1⋅011-1⋅018), malignant neoplasm (1⋅014, 1⋅013-1⋅016), diabetes (1⋅013, 1⋅009-1⋅018), and cerebrovascular disease (1⋅010, 1⋅007-1⋅013) after 1 year. Associations between jail incarceration and cause-specific mortality rates weakened as time lags increased, but to a greater extent for causes of death with generally shorter latency periods (infectious disease and suicide) than for those with generally longer latency periods (heart disease, malignant neoplasm, and cerebrovascular disease). INTERPRETATION: Jail incarceration rates are potential drivers of many causes of death in US counties. Jail incarceration can be harmful not only to the health of individuals who are incarcerated, but also to public health more broadly. Our findings suggest important points of intervention, including disinvestment from carceral systems and investment in social and public health services, such as community-based treatment of substance-use disorders. FUNDING: US National Institute on Drug Abuse (National Institutes of Health).

## Mechanisms

* "If the relationship between rates of county jail incarceration and county mortality is causal and not merely a shared consequence of concentrated and racialised disadvantage, we would expect jail incarceration rates to influence deaths from different causes to differing degrees and via differing mechanisms."
	* Jails increase in the community spread of infectious disease thus increases in the jail mortality rate are expected to lead short-term increases in infectious disease mortality.
	* The effects on diseases with longer latency periods like heart disease and cancer are more uncertain.
	* Jail also harms psycho-social and material or economic well-being of communities. Jail incarceration can be linked to psycho-social deaths such as drug overdoses and suicides.
	  
* **Hypotheses**
	* There will be pronounced short-term associations between rates of jail incarceration and deaths by infectious disease, substance use, and suicide. These results will weaken as the time lags increase.
		* Mass incarceration is linked to community infectious disease spread and acute psycho-social and economic deprivation.
		* Chronic respiratory disease --> reflect direct mechanisms of incarceration (e.g., overcrowding and poor ventilation) and indirect (poor housing conditions, smoking, pollution, infections as a child).
	* The associations will strengthen with time for diseases with longer latency periods.
		* **NOT CORRECT. THE EFFECTS ALSO DECLINED OVER TIME.**
		* Although the decline was less pronounced.
		* Perhaps due to the fact that jail incarceration peaked nationwide around 2008?
		  
* **Mechanisms**
	* Direct pathogenic effects of incarceration.
		* People face harmful exposures during incarceration. Jails have high rates of infectious disease and have unhealthy water and air.
		* It is also traumatic and violent.
		* As the rates of jail incarceration increase, the health of an increasing number of individuals is likely affected which would affect the overall county health.
	* Racialised psycho-social pathways.
		* High rates of jail incarceration disrupt social ties and support networks which are protective of community health.
		* Family members of incarcerated are directly affected --> higher divorce rates, separation of children and parents.
	* Racialised economic pathways.
		* Funding is diverted from social services and public health and is redirected into the criminal legal system.
		* Drives job loss, wage inequality, removes working age individuals from the labor force which harms local economies.
	* These mechanisms can become feedback loops which lead to increased rates of jail incarceration.
## Data and Methods

* **Jail incarceration data** comes from the Vera Institute from 1987 to 2017.
* **Controls**: Total population, median age, Black resident population ([[PEP]]), poverty data ([[SAIPE]]), unemployment data ([[LAUS]]), county crime data ([[UCR]]), state incarceration data, and party control of the legislature from the [[National Conference of State Legislatures]]. 
	* Missing data were replaced with data from the previous year.
* **Dependent variable** --> Rates of cause-specific mortality for those younger than 75.
	* 1) cerebrovascular disease, 2) chronic lower respiratory disease, 3) diabetes, 4) heart disease, 5) malignant neoplasm, 6) suicide, 7) and unintentional injury, 8), infectious disease deaths, and 9) substance-induced deaths.
	* Counties with less than 10 deaths are reported as missing.
* **Unit of analysis**: County. Included all counties with at least 2 years of complete data for all nine causes of death. Sample size of 1,094 counties with 31 years representing 33,882 county-years.
* [[fixed effects]] for county and year.
* Use [[quasi-Poisson]] regression models to deal with [[overdispersion]].
* Use 1-year lags to assess short-term effects, 5-year lags to asses medium term effects, and 10-year lags to assess long-term effects.
* **Sensitivity Analysis**
	* Replaced all the cause-specific mortality counts which were suppressed with 0 and then with 9. **Similar results with higher variability (although still mostly statistically significant)**.
	* Use [[Multilevel modeling|multilevel modeling]] and estimate random intercepts rather than fixed effects. **Results remain largely unchanged**
	* Estimated the 1-year and 5-year lagged models using only data from 1987 - 2008 (to make results more comparable to 10-year lagged model). **Results remain largely unchanged**.
* Interpretation must be focused on non-rural and larger counties (unless you include sensitivity analyses which you could).

## Results

Ranked from strongest to weakest effects.

**Strongest at 1-year lag and 5-year lag**
* **Infectious disease**: Effect decreases over time (significant up to 10-year lag).
* **Respiratory**: Effect decreases over time (significant up to 10-year lag).
* **Substance use**: Effect decreases over time (significant up to 10-year lag).
* **Suicide**: Effect decreases over time (**becomes insignificant** at 10-year lag). In terms of coefficient size, flip-flops sometimes with lower ranked causes of death in the 5 and 10 year lags.
* **Heart disease**: Effect decreases over time (significant up to 10-year lag).
* **Injury**: Effect decreases over time (significant up to 10-year lag).
* **Cancer**: Effect decreases over time (significant up to 10-year lag).
* **Diabetes**: Effect decreases over time (**becomes insignificant** at 5-year lag).
* **Heart disease**: Effect decreases over time (significant up to 10-year lag).

By the 10-year lag, the estimates for the effect of jail incarceration have become much more similar to each other.

Authors argue the causes of death with shorter latency periods experienced greatest relative declines in effect size consistent with their hypothesis.