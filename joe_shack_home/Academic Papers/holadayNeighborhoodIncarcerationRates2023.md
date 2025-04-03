---
title: Neighborhood Incarceration Rates and Adverse Birth Outcomes in New York City, 2010-2014
author:
  - Louisa W. Holaday, Destiny G. Tolliver, Tiana Moore, Keitra Thompson, Emily A. Wang
year: 2023
journal:
  - JAMA Network Open
type:
  - Article
---
[Zotero entry](zotero://select/items/@holadayNeighborhoodIncarcerationRates2023)
**Tags**: #incarceration #community_effects #effects_of_incarceration #incarceration_health #incarceration_paper 
## Abstract

The US has high rates of adverse birth outcomes, with substantial racial disparities augmented by stress and neighborhood disadvantage. Black people are more likely to live in neighborhoods with high rates of incarceration, which is a source of both stress and neighborhood disadvantage and, thus, may contribute to adverse birth outcomes. To determine whether neighborhoods with high incarceration rates also have higher rates of adverse birth outcomes compared with neighborhoods with lower rates. This cross-sectional study used publicly available data from the New York City Department of Health (2010-2014). Censored Poisson regression, with the US Census tract as the unit of analysis, was used to examine the association of neighborhood incarceration rate and birth outcomes. Multivariable models included percentage of births aggregated to the Census tract by maternal factors (age, parity, singleton vs multiple birth, insurance, and race) and neighborhood factors (poverty, education, and violent crime). Analyses were performed between May 2021 and October 2022. Neighborhood incarceration rate, categorized into quintiles. The primary outcome was the incidence rate ratio (IRR) of preterm birth and low birth weight. Secondary outcomes were IRRs of very preterm birth, extremely preterm birth, and very low birth weight. Hypotheses were formulated before data collection. Among 2061 Census tracts with 562 339 births, incarceration rates varied from 0 to 4545 people incarcerated per 100 000, and high-incarceration neighborhoods had more residents of Black race (54.00% vs 1.90%), living in poverty (32.30% vs 10.00%), and without a general educational development equivalent (28.00% vs 12.00%) compared with low-incarceration neighborhoods. In fully adjusted models, high-incarceration neighborhoods had a 13% higher IRR of preterm birth (IRR, 1.13; 95% CI, 1.08-1.18), 45% higher IRR of very preterm birth (IRR, 1.45; 95% CI, 1.24-1.71), 125% higher IRR of extremely preterm birth (IRR, 2.25; 95% CI, 1.59-3.18), 10% higher IRR of low birth weight (IRR, 1.10; 95% CI, 1.05-1.16), and 52% higher IRR of very low birth weight compared with low-incarceration neighborhoods (IRR, 1.52; 95% CI, 1.28-1.81). Neighborhood incarceration rate was positively associated with adverse birth outcomes, particularly those associated with infant mortality. Black people were significantly more likely to live in high-incarceration neighborhoods, suggesting that mass incarceration may contribute to racial disparities in birth outcomes.

## Mechanisms

"People living in high-incarceration neighborhoods experience increased stress, disruption of family and social ties, and loss of financial and social resources and collective power. Living in high-incarceration neighborhoods is independently associated with worse mental health and lower life expectancy. Thus the indirect effects of mass incarceration on non-incarcerated individuals living in high-incarceration neighborhoods could influence birth outcomes through neighborhood disadvantage, a more stressful environment for pregnant people, and decreased availability of social or economic resources." #quote 

Why the census tract level? People's social networks and neighborhood resources may be more accurately reflected at the smaller geographic level.

## Data and Methods

* **Independent variable**: Incarceration data came from the Prison Policy Initiative and reflects state prison incarceration rates in NYC as of 2010. Modeled incarceration as a categorical variable to reflect non-linearity of its effects.
* **Dependent variables**: Preterm birth and low birthweight. Census tracts with less than 50 births from 2010 - 2014 were excluded.
* **Controls**:
	* Percentage of births that were teen births, percentage of births to women over 40, other birth variables concerning the types of births. Censored tracts were given a value of 0.
	* Percentage of births to Black individuals. Censored tracts were assigned the percent of individuals in the neighborhood who are Black.
	* Tract-level insurance rates among women ages 18 - 45 from the ACS.
	* Poverty.
	* Percent of the population without a GED or equivalent.
	* Violent crime rate derived from geocoding NYC police department data from 2010.
	* I do not understand this decision fully --> "we tested all neighborhood covariates as quadratic terms to determine whether to include these as continuous or categorical variables..."
* **Methods**
	* [[Kruskal-Wallis test of difference between mean ranks across groups]].
	* Censored [[Poisson regression]].
* Data uses 2010 for some variables and 2010 - 2014 for other variables for 2,061 census tracts in New York City.
* Results generally indicate that higher incarceration rates are associated with worse birth outcomes.
	* "Adverse birth outcomes in neighborhoods with high rates of incarceration cannot be attributed to newborns whose parent was incarcerated during gestation. The highest incarceration neighborhoods had a median of less than 1% of the population incarcerated at a given time."