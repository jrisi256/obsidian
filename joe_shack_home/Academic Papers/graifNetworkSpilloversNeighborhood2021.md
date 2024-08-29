---
type:
  - Article
author:
  - Corina Graif
  - Brittany N. Freelin
  - Yu-Hsuan Kuo
  - Hongjian Wang
  - Zhenhui Li
  - Daniel Kifer
journal:
  - Justice Quarterly
year: 2021
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Corina Graif, Brittany N. Freelin, Yu-Hsuan Kuo, Hongjian Wang, Zhenhui Li, Daniel Kifer
* **Title**: Network Spillovers and Neighborhood Crime: A Computational Statistics Analysis of Employment-Based Networks of Neighborhoods
* **Date of publication**: 2021-02-23
* **Journal**: Justice Quarterly
* **Volume**: 38
* **Issue**: 2
* **Pages**: 344-374
* **URL**: [https://doi.org/10.1080/07418825.2019.1602160](https://doi.org/10.1080/07418825.2019.1602160)
* **Tags**: #comps_exam, #computational_social_science, #neighborhood_context, #social_network_analysis #social_disorganization #routine_activities 
* **PDF Attachments**:
  * [graifNetworkSpilloversNeighborhood2021.pdf](zotero://open-pdf/library/items/6SRJHMQC)

## Abstract

Research on communities and crime has predominantly focused on social conditions within an area or in its immediate proximity. However, a growing body of research shows that people often travel to areas away from home, contributing to connections between places. A few studies highlight the criminological implications of such connections, focusing on important but rare ties like co-offending or gang conflicts. The current study extends this idea by analyzing more common ties based on commuting across Chicago communities. It integrates standard criminological methods with machine learning and computational statistics approaches to investigate the extent to which neighborhood crime depends on the disadvantage of areas connected to it through commuting. The findings suggest that connected communities can influence each other from a distance and that connectivity to less disadvantaged work hubs may decrease local crime – with implications for advancing knowledge on the relational ecology of crime, social isolation, and ecological networks.

## My notes

### Research question

Does exposure to work places (as measured by commuting ties) of higher disadvantage increase local crime above and beyond the role of local disadvantage?

* Recent work has suggested that disadvantage outside of a neighborhood is also associated with local crime -> connected to the idea that people spend a lot of time outside of their residential neighborhood.
  
* Other research has demonstrated spillover effects or how geographic proximity of high disadvantage neighborhoods affects local residents in adverse ways.
  
	* The underlying individual spatial links have always been assumed, though. The mechanisms has never been specified.
	  
* Important implications for policy because interventions in one neighborhoods will have their effects moderated by that neighborhood's connections to other neighborhoods.

### Prior research
#### Internal neighborhood mechanisms

* Social ties and interaction.
* Norms and [[Collective efficacy|collective efficacy]].
* Institutional resources like [[Local organizations and voluntary associations|local organizations + voluntary associations]].
* [[Routine activity]].

#### Spatial spillovers and network spillovers

* Disadvantage effects spill over between geographically proximate neighborhoods.
  
* The focus on this paper is understanding the mechanisms through which such an effect could happen i.e., commuting ties.
  
	* Leads to the idea that connected neighborhoods (explicitly measured this time) over relatively larger geographic distances could be affecting each other.
	  
* The above 4 mentioned internal neighborhood mechanisms could all spill over.

### Current research

1) The disadvantage of work communities connected to the focal community through commuting will be associated with crime in the focal community i.e., network disadvantage spillovers.
   
2) The association between work disadvantage and local crime may be explained by local disadvantage effects i.e., homophily.
   
3) The association between network disadvantage and local may be explained by spatial proximity to disadvantage and crime i.e., surrounding crime spillovers.
   
4) The association between work network disadvantage and local crime may be due to crime spillovers i.e., network crime spillovers.

### Data

* Data comes from 2001 - 2013.
* Data aggregated to the [[Chicago community area]] level.
* Police-reported crime in Chicago.
* [[Concentrated disadvantage]] measures come from the Census.
* Commuting data comes from the [[Longitudinal Employer Household Dynamics]] or LEHD.

**Dependent variable** -> overall crime, violent crime, property crime.

**Independent variable**

* Network spillovers of disadvantage or Work network disadvantage index (focal area's disadvantage is a weighted average of disadvantage levels in all works connected to it with weights based on the strength of the commuting flow).
  
* Internal [[concentrated disadvantage]] -> uses [[Principal Component Analysis]], as per usual, using the usual variables.
	* Also use residential stability, population density, and measure racial/ethnic diversity using [[Herfindahl Index]].
	  
* Geographic spillovers for **disadvantage** and **crime**.
  
* Network spillovers of crime.
  
* Temporal spillovers of crime (crime lag variables).

### Methods

* Estimate [[negative binomial regression]] models and gradually include more predictor variables.

* Compare accuracy of models using [[mean absolute error]], [[mean relative error]], and [[AIC]] on [[train/test]] splits specifically by using [[leave-one-out cross-validation]] (estimate a model N - 1 times on N - 1 data points. evaluate on the one held-out data point, and average the performance metrics across N - 1 models).
  
* Use [[permutation tests]] (randomly permute values for the variable, measure error for each permutation (refit the model and measure accuracy), create a distribution of errors, then see where one's estimate lies on the distribution) to evaluate statistical significance of individual model variables.

### Results

* Network disadvantage retains its predictive and statistical significance across a variety of model specifications -> disadvantage levels in the areas where people work predicts levels of crime in people's home communities.
  
* Spatial (crime and disadvantage) spillover effects were also found, above and beyond networked disadvantage spillover effects. Crime network effects were also found but did not explain away network disadvantage.
  
* Network disadvantage remained significant even while controlling for internal disadvantage.
  
* Network disadvantage remained significant and more predictive even when controlling for prior levels of local crime.

### Robustness checks

* Segregation, median household income, retail business, income and age differences.
  
* They found some non-linearity based when separating neighborhoods into percentiles with stronger effects for network disadvantage in predicting crime in higher percentiles -> more research needed.

### Conclusions

* Neighborhoods are not closed systems and are not simply affected by spillovers from surrounding (geographically) areas.

#question -> What are the policy implications of this? How do we foster connections between disadvantaged and advantaged neighborhoods? Do we believe that by, for example, finding work in advantaged areas for people living in disadvantaged areas, it would decrease crime in the focal community?