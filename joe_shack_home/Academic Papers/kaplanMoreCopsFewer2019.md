---
type: [Article]
author: [Jacob Kaplan, Aaron Chalfin]
journal: [Criminology & Public Policy]
date: 2019
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Jacob Kaplan, Aaron Chalfin
* **Title**: More cops, fewer prisoners?
* **Date of publication**: 2019
* **Journal**: Criminology & Public Policy
* **Volume**: 18
* **Issue**: 1
* **Pages**: 171-200
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9133.12424](https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9133.12424)
* **Tags**: #comps_exam, #criminology, #policing
* **PDF Attachments**:
  * [kaplanMoreCopsFewer2019.pdf](zotero://open-pdf/library/items/YZLSNTRQ)

## Abstract

The results reported in a large amount of the criminology literature reveal that hiring police officers leads to reductions in crime and that investments in police are an efficient means of crime control compared with investments in prisons. One concern, however, is that because police officers make arrests in the course of their duties, police hiring, albeit efficient, is an inevitable driver of “mass incarceration.” In this article, we consider the dynamics through which police hiring affects downstream incarceration rates. Using state-level panel data as well county-level data from California, we uncover novel evidence in favor of a potentially unexpected and yet entirely intuitive result: that investments in law enforcement are unlikely to increase state prison populations markedly and may even lead to a modest decrease in the number of state prisoners. As such, investments in police may, in fact, yield a “double dividend” to society by reducing incarceration rates as well as crime rates.

## My notes

### Introduction

* Empirical tests of the claims of [[naginDeterrenceTwentyFirstCentury2013]] and [[durlaufImprisonmentCrime2011]] -> deterrence is inexpensive relative to incapacitation as it reduces incarceration costs and crime costs so we should cut funding to prisons and increase funding to the police.

	* Additionally, policy makers worried about the trade-offs between incapacitation vs. the criminogenic effects of incarceration should also be pulled towards deterrence.

* On the other hand, people argue given that police make arrests and more police leads to more arrests, they must be contributing to the growth in incarceration.
  
	* People are also more sensitized to the social costs of incarceration.

### Data and Methods

* State-level panel data and county-level panel data from California. They estimate the effect of increases in police expenditures on actual and expected new prison entries.

* They use investments in fire safety as an [[instrumental variable]] for investments in policing. They argue the power of public-sector unions and the citizen desire for government services cause these two variables to co-vary.
  
* Variation in police spending explained by spending on fire safety is a valid instrument so long as expenditures on fire safety are uncorrelated with prison admissions except through police spending. The authors argue any remaining correlation between fire safety spending and prison admissions is likely to be positive (given that a place has a *safety first* approach to governing).

	* As a result, they argue their estimates represent a conservative estimate of police spending on prison admissions to the degree that the fire safety variable is positively related to prison admissions (as police spending is negatively related to prison admissions).

	* One must argue fire safety spending is negatively related to prison admissions to argue the estimate is an overestimate.
	  
* Data are from 1997 to 2015.
	* Prison data comes [[National Prisoner Statistics]] program.
	* State budget data comes from the [[Annual Survey of Public Employment and Payroll]].
	* Arrest data comes from the [[UCR]].
	* They use the [[ACS]] for demographic and economic variables.

### Theoretical Model

* Increasing the police force could only lead to more prisoners if the probability of apprehension or the probability of prison commitment given apprehension moderately increased which existing research does not tend to support.

### Empirical Model

* **Dependent variable** -> Number of new prison commitments.
* **Independent variables**
	* One year lag of police expenditures.
	* Time-varying control variables for each state (or county).
	* State fixed effect.
	* Year fixed effect.
* **Problem** -> The same factors influencing police spending may also be influencing crime creating a positive correlation between police spending and prison admissions. The authors note though they are skeptical to the degree that [[endogeneity]] may be a problem here.
	* [[OLS]] and [[two stage least-squares regression]] estimates are pretty similar.
	* So they also estimate a 2SLS using the lagged fire safety spending as the instrument.
* Results are not sensitive to using population weights.
* [[Clustered standard errors]] at the state level as well as [[bootstrapped standard errors]].

### Results

* Descriptively, we see spending on officers increases while crimes and arrests decrease over time. Additionally, prison commitments increases from 1997 to roughly 2006/2007 before declining.
  
	* Officers may do a great deal to reduce crime through things like maintaining visibility, they make very few serious arrests in a year.
	  
	* Arrests are unlikely to lead to a prison spell.
	  
	* Because of this, officers are unlikely to incapacitate a large number of individuals.
	  
* **Main results in Table 4**
  
	* Increases in police expenditures cause less crime. In the OLS model, it is associated with fewer actual prison spells.
		* No significant relationship with expected prison spells but the effect size is negative -> even the most extreme estimate finds modest increases in prison commitments as police spending increases. It is unlikely increases in police spending led to mass incarceration.

	* This is because increased police expenditures are not statistically significantly related to arrests.
	  
* Results replicated very neatly on California counties although the results are more imprecisely estimated.

### Limitations

* Effect of police size on prison population will depend on how the police are used (e.g., used in such a way as to produce more arrests).
  
* Increases in police expenditures may lead to more difficult relationships between disadvantaged communities and the police.
  
* May increase jail admissions to the extent that the net is widened. 