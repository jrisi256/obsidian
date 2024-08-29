---
type:
  - Article
author:
  - John R. Hipp
  - Daniel K. Yates
journal:
  - Criminology
year: 2009
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: John R. Hipp, Daniel K. Yates
* **Title**: Do Returning Parolees Affect Neighborhood Crime? A Case Study of Sacramento*
* **Date of publication**: 2009
* **Journal**: Criminology
* **Volume**: 47
* **Issue**: 3
* **Pages**: 619-656
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1745-9125.2009.00166.x](https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1745-9125.2009.00166.x)
* **Tags**: #comps_exam, #incarceration, #parole, #recidivism #neighborhood_context 
* **PDF Attachments**:
  * [hippReturningParoleesAffect2009.pdf](zotero://open-pdf/library/items/HJYN9WQB)

## Abstract

This study used a unique data set that combines information on parolees in the city of Sacramento, CA, over the 2003–2006 time period with information on monthly crime rates in Sacramento census tracts over this same period, providing us a fine-grained temporal and geographical view of the relationship between the change in parolees in a census tract and the change in the crime rate. We find that an increase in the number of tract parolees in a month results in an increase in the crime rate. We find that more violent parolees have a particularly strong effect on murder and burglary rates. We find that the social capital of the neighborhood can moderate the effect of parolees on crime rates: Neighborhoods with greater residential stability dampen the effect of parolees on robbery rates, whereas neighborhoods with greater numbers of voluntary organizations dampen the effect of parolees on burglary and aggravated assault rates. Furthermore, this protective effect of voluntary organizations seems strongest for those organizations that provide services for youth. We show that the effect of single-parent households in a neighborhood is moderated by the return of parolees, which suggests that these reunited families may increase the social control ability of the neighborhood.

## My notes

#paper_idea -> Important to consider for people returning to their communities.
### Research Question

* What is the effect on neighborhood crime rates of returning parolees from jail/prison?
* Does the type of neighborhood of a parolee return to matter in terms of crime?
* Does the type of parolee matter? E.g., if the release of a parolee leads to the reunification of a family, will that have a negative effect on the crime rate?
  
	* **Increase crime?**:
		* Parolees are more crime prone and their increased presence within a neighborhood will lead to more crime because they themselves are causing more crime. See [[Routine activity]] theory.
		* Parolees cause others to commit more crime through the rekindling of ties with fellow co-offenders and sharing knowledge gained in jail/prison. See [[differential association]].
		* They may also cause residential instability (influx of new people, perhaps other people leaving) -> strain existing social ties.
		  
	* **Decrease crime?**:
		* [[Mass incarceration]] had the effect of breaking up families and households leading to a breakdown in the informal social control mechanisms of the neighborhood. Returning parolees, to the extent it leads to the reunification of families, will lead to lower crime rates as informal social control increases.
			* Some families *are* better off when a parent is incarcerated which provides a counterpoint.
	  
	* **Neighborhoods with higher social cohesion can better handle the influx of parolees.**
	  
		* For example, neighborhoods with more [[Local organizations and voluntary associations|local organizations and voluntary associations]] dedicated to helping to the parolees may be able to better integrate them.
		  
		* Additionally, neighborhoods with more informal ties and social cohesion may be able to better accommodate the influx of parolees.

### Data and Methodology

#### Data

Data on parolees in San Francisco from 2003 - 2006 with monthly crimes at the census tract level.

**Dependent variable** -> Police-reported crime aggregated to the census tract/month level. [[Type 1]] crime.

**Independent variable** -> The number of parolees per capita in a given tract in a given month. Other variables include:

* Total number of prior arrests of parolees.
* Use a weighted sum to capture the aggregate *seriousness* of parolees living in the neighborhood.
* Number of Black parolees per capita.

**Moderators**
* Percent single-parent households.
* Average length of residence in households.
* Number of voluntary organizations per 100,00. Data comes from the [[National Center for Charitable Statistics]]. Also categorized them by services provided.

#### Methods

* Use [[negative binomial regression]].
* Use census tract population as an [[offset variable]].
* [[Incidental parameter bias]] does appear to be a problem for negative binomial regression models.
* Use [[spatial regression]] techniques specifically spatial lags to account for the fact there are likely spillover effects in neighboring census tracts.
* Use [[fixed effects]] for the month/year combination.
	* Robustness checks also include fixed effects for census tract.

### Results

**Table 2**

* The logarithmic of the number of parolees per capita has a strongly positive association with robbery and burglary (not aggravated assault or murder). This suggests there are diminishing returns concerning the effect of returning parolees on the crime rate.
  
* The effect of the spatial lag is large for robbery but only marginally significant. The effect on burglary is negative but imprecisely estimated.

**Table 3**

* The type of parolees being released matters. It seems as if violent parolees have positive effects on burglary and marginally on murder (after controlling for parolees per capita overall).
  
* No specific effects for serious nonviolent offenses or *churners* (parolees with high number of prior arrests).
  
* Black parolees have specific effects for increasing aggravated assaults and burglaries.
* #question -> Strange to control for overall number of parolees and then the specific sub-type?

**Table 4** -> Type of neighborhood matters

* While the number of parolees being released does increase the crime rate, there is a negative interaction effect with the percentage of single-parent households (assault and burglary).

* Same for number of voluntary organizations.
	* The type of organization matters -> crime and disorder-focused organizations specifically (geared at reducing crime and disorder and helping youth).
  
* Same for residential stability (only robbery). 
### Limitations

Hard to verify if parolees are living where it is officially reported they are living.