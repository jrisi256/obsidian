---
type: [Article]
author: [Patrick Sharkey, Gerard Torrats-Espinosa, Delaram Takyar]
journal: [American Sociological Review]
date: 2017-12-01
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Patrick Sharkey, Gerard Torrats-Espinosa, Delaram Takyar
* **Title**: Community and the Crime Decline: The Causal Effect of Local Nonprofits on Violent Crime
* **Date of publication**: 2017-12-01
* **Journal**: American Sociological Review
* **Volume**: 82
* **Issue**: 6
* **Pages**: 1214-1240
* **URL**: [https://doi.org/10.1177/0003122417736289](https://doi.org/10.1177/0003122417736289)
* **Tags**: #comps_exam, #crime_policy, #criminology, #social_disorganization, #theory_advancement, #causal_inference
* **PDF Attachments**:
  * [Sharkey et al_2017_Community and the Crime Decline.pdf](zotero://open-pdf/library/items/65ANSKL9)

## Abstract

Largely overlooked in the theoretical and empirical literature on the crime decline is a long tradition of research in [[criminology]] and [[urban sociology]] that considers how violence is regulated through informal sources of social control arising from residents and organizations internal to communities. In this article, we incorporate the “systemic” model of community life into debates on the U.S. crime drop, and we focus on the role that local nonprofit organizations played in the national decline of violence from the 1990s to the 2010s. Using [[longitudinal data]] and a strategy to account for the [[endogeneity]] of nonprofit formation, we estimate the causal effect on violent crime of nonprofits focused on reducing violence and building stronger communities. Drawing on a panel of 264 cities spanning more than 20 years, we estimate that every 10 additional organizations focusing on crime and community life in a city with 100,000 residents leads to a 9 percent reduction in the murder rate, a 6 percent reduction in the violent crime rate, and a 4 percent reduction in the property crime rate.

## My notes

### What is the research question?

* Why did crime decline so much in the 1990's? Most explanations focus on factors external to the communities most affected by crime (e.g., changes in policing, abortion, rates of lead exposure, etc.)
* Focus on sources of informal social control internal to the communities. Community mobilization against violence.
* Uses the [[systemic model]] and focuses on actors, organizations, and institutions which influence social cohesion and the ability for residents to come together to solve common problems within a neighborhood.
* **What role do local nonprofit organizations play in reducing crime?**

### Why is it important?

* Substantively, it is easy to see why it is important.
* Theoretically, many previous studies have not found connections between organizational density and crime/violence. Why?
	* Many studies use measures of organizational density that include a wide range of establishments which do not have a direct relationship to crime and violence. #data_issue
	* No studies have dealt with the [[endogeneity]] of community-oriented organization formation (i.e., it is the case that the same factors causing violence/crime are likely to cause higher rates of community-oriented organization formation -> economic downturns or upturns). #methods_issue
		* Also issue of [[simultaneity bias]] i.e., levels of crime determine the levels of nonprofit formation which further determines the level of crime -> circular.
* While other arguments are important in considering crime decline (look to those people cited who argue incarceration led to less crime), we need to focus on internal community efforts and how they have been effective from a social organization perspective and can help explain national trends in crime decline -> we need better data ultimately to make these national comparisons. #highlight 

### How do you propose to answer your question?

* Using [[fixed effects]] and an [[instrumental variable]].
	* Fixed effects account for any time-invariant unobserved characteristics of cities which might affect the number of nonprofits in a city and the violent crime rate ([[confounders]]).
	* Use the formation of arts, medical research, and environmental protection nonprofits as an instrument for the formation of nonprofits related to violence, crime, and community building. Deals with time-varying confounders.
		* Changes in the prevalence of arts, medical, and environmental nonprofits have no direct effect on crime and violence, but they are associated with changes in the prevalence of nonprofits designed to address violence and rebuild communities.
			* So to be a valid instrument, it must be associated with the main independent variable but conditional on that independent variable (community-oriented organizations) it must have no correlation with the main dependent variable (crime/violence).
	* 264 cities spanning more than 20 years.
* Data comes from the [[UCR]], [[ACS]], and [[National Center for Charitable Statistics]] or NCCS.
* Focus on 300 largest cities in the USA and on organizations formed between 1990 and 2013.
* **Independent variable**: The cumulative number of active community-oriented nonprofits in a given city in a given year.
* **Controls**: Population density, racial composition, education, immigrants, age structure, poverty, unemployment rate, % employed in manufacturing. Use linear interpolation. Robustness tests include the state incarceration rate, the number of police officers per capita in the city, region-by-year fixed effects, and the previous year's crime rate. Results are pretty robust.
* **Equation 1**: (pg 11), Change in crime from 1990 to 2013 is the dependent variable. Change in number of community organizations is the main independent variable. Controls. [[ordinary least squares]].
* **Equation 2.1 and 2.2**": Two-stage regression equation estimation. Estimate the effect of the instrument (number of arts, medical, and environmental nonprofits) on the main independent variable (number of community-oriented nonprofits). Then estimate the effect of the instrument on the main dependent variable (change in crime from 1990 to 2013). Divide the first estimate by the second estimate -> The second stage equation uses only the variation in our main independent variable induced by the instrument in the first stage.
* **Equation 3**: Estimate the effect of the number of community-oriented non-profits at time t on crime at time t = t + 1 while using city and year fixed-effects.
* **Equation 4.1 and 4.2**: Similar to equations 2.1 and 2.2, use an instrumental variable in conjunction with fixed effects.

### What do you find?

* Every 10 additional community-oriented nonprofits in a city with 100,000 residents leads to a 12% reduction in homicide and a 7% reduction in property crime -> long term change.
* Every 10 additional community-oriented nonprofits per 100,000 residents leads to a 9% decline in the murder rate, 6% decline in the violent crime rate, and 4% decline in the property crime rate -> year-to-year change.
* **Figure 4**: Robustness check. Lagged nonprofit creation is significantly associated with reduced crime rates but lead nonprofit creation is not (useful check because it means crime at time t = 0 is not associated with the number of nonprofits at time t = 1).
* **Figure 5**: Break the results down by type of community organization.
* **Table 4**: Interesting the results break down when only including the 100 largest cities, but they remain robust when excluding the 100 largest cities.
	* Changes are driven by less populated cities.