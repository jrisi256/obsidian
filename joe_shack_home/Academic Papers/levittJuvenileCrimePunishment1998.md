---
type: [Article]
author: [Steven D. Levitt]
journal: [Journal of Political Economy]
date: 1998-12
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Steven D. Levitt
* **Title**: Juvenile Crime and Punishment
* **Date of publication**: 1998-12
* **Journal**: Journal of Political Economy
* **Volume**: 106
* **Issue**: 6
* **Pages**: 1156-1185
* **URL**: [https://www.journals.uchicago.edu/doi/10.1086/250043](https://www.journals.uchicago.edu/doi/10.1086/250043)
* **Tags**: #comps_exam, #criminology, #deterrence_rational_choice, #theory_advancement
* **PDF Attachments**:
  * [levittJuvenileCrimePunishment1998.pdf](zotero://open-pdf/library/items/EFRTKCTM)

## Abstract

Over the last two decades Juvenile violent crime has grown almost twice as quickly as that of adults. This paper finds that changes in relative punishments can account for 60 percent of that differential. Juvenile offenders are at least as responsive to criminal sanctions as adults. Sharp drops in crime at the age of majority suggest that deferrence (and not merely incapacitation) plays an important role. There does not, however, appear to be a strong relationship between the punitiveness of the juvenile justice system that a cohort faces and the extent of criminal involvement for that cohort later in life.

## My notes

### Introduction

* Divergence in juvenile and adult crime trends between 1978 and 1993. Juvenile arrest rates are way up and adult arrest rates are slightly down, slightly up, or no change. Why?
  
* Is it due to rational changes in juvenile decision making given the relative differences in punishment for juveniles vs. adults to engage in crime?

### Research Questions

1. To what extent does juvenile crime respond to changes in the punitiveness of the juvenile justice system?
   
2. Can the divergence in juvenile and adult crime be explained by changes in the relative punishments between these two groups?
   
3. Is the response of juvenile crime due simply to incapacitation or deterrence?
   
4. Is criminal involvement later in life affected by the degree of punishment for juvenile offenses?

### Methods #1

* Primary source of data on juvenile corrections comes from censuses of public and private juvenile facilities [[OJJDP]], Office for Juvenile Justice and Delinquency Prevention.
  
* Corresponding data on adult imprisonment rates (from prisons, not jails) are available on an annual basis from the [[BJS]].
  
* Juveniles in adult prisons are also excluded.
  
* No direct measures of the number of crimes committed by age group. They only have official arrest statistics.
	* The number of crimes committed by a juvenile in a given state in a given year **equals** the fraction of arrests for that crime (in a particular state in a particular year) **which were of juveniles** multiplied by the number of reported crimes in that state in that year.
		* E.g., if there are 100 reported robberies, 10 total arrests for robbery, and 3 of those arrests of robbery were of juveniles, then the number of robberies committed by juveniles is standardized to 30.
		* If there are 200 reported robberies, 20 total arrests for robbery, and 5 of those arrests of robbery were of juveniles, then the number of robberies committed by juveniles is standardized to 50.
	* **Implicitly assumes juveniles and adults are arrested at the same rate for a given crime** and **also assumes adults and juveniles tend to commit the same offenses at the same rate**.
	  
* Dependent variable is the natural log of this weird crime rate measure.
* Independent variable is the previous year's juvenile custody rate:
	* The number of juveniles in custody per reported juvenile violent crime.
	* The number of individuals in custody per 15-17 year old.
* Controls for % black, % residing in a metropolitan area, state unemployment rate, legal drinking age, age composition, state and year [[fixed effects]].

### Findings #1

* The lagged juvenile custody variable (measured both ways) is negatively associated with juvenile crime rates.
* The lagged adult custody variable is also negatively associated with adult crime rates.
* Adult crime rates are significant predictors of juvenile crime rates.
* Custody rates in public facilities (which the author contends have harsher conditions) have stronger negative associations compared to private (facilities which tend to be less harsh, the author contends). -> incapacitative effects?

### Methods #2

* If juveniles respond to the incentives of the criminal justice system, then one would also expect to observe abrupt changes in criminal behavior associated with passage into adulthood. The author argues this is more focused test of deterrence because if deterrence is at work, the results will be immediately seen time-wise.
  
* Argues that in states with greater relative differences in juvenile vs. adult punishments, you will see greater declines in criminal activity for the juvenile cohort once they reach adulthood.
  
* Relative punitiveness is defined as the ratio of adult prisoners per reported adult crime **to** juvenile delinquents per reported juvenile crime. #question Are these definitions of crime using the same equation as above?
  
* Divides states into terciles based on how different adult punishments are from juvenile punishments.

### Findings #2

* Table 4 -> As the relative punitiveness increases, the year to year % change in crime for the cohort also increases i.e., as juveniles who live in areas with relatively light punishments (compared to adult punishments) hit adulthood, they become much less likely to commit crime. vs. as juveniles who live in areas with more severe punishments (or as severe as adults) hit adulthood, they become much more likely to commit crime.
  
* Results do not replicate as well in states where adulthood is defined at 17 (vs. 18).
  
* Table 5 formalizes the analysis in a regression equation. Dependent variable is the % change in crime rate from the previous observation.
	* **Key independent variable**: Dummy variable indicates if the cohort are now adults in the given time period interacted with the relative punishment ratio.
	* Same controls as above. Fixed effects for cohort, year, and age. Also try state and cohort fixed effect interactions.
	* Interaction is statistically significant negative across a variety of specifications.

### Methods #3

* Estimate the crime rate for a given age group in a given state in a given year.
* **Independent variables**:
	* Adult custody rate or the punitiveness of the adult system lagged by one year.
	* Juvenile custody rate in the last year that a given cohort was subject to the juvenile courts (i.e., a lagged juvenile custody rate where the lag is differentially applied based on when the cohort was last of juvenile age). **A negative value would imply that harsh punishments while the cohort were juveniles is associated with decreases in crime at their current age**.
	* Other controls introduced in other equations.
* **Limitations** -> Most of the measures are not age-specific but only vary by state and year. Mobility across state lines among juveniles will disrupt the results.

### Findings #3

* Table 6 -> Severity of punishment in the last of year of being a juvenile has no discernible impact on current adult criminal behavior. Juvenile sanctions do not have direct effects on later criminal involvement -> other suggests that long-term deterrent effects and labeling/stigma effects offset each other **or** both are small in magnitude.

### Conclusions

1. Using state-level panel data from 1978-1993, harsher punishments for juveniles are associated with lower rates of juvenile offending. Juveniles respond rationally to harsher sanctions.
	1. Argues that changes in relative punishments for juveniles vs. adults accounts for most of the differential rate of change between juvenile and adult crime rates.
   
2. There does not seem to be a strong relationship between the punitiveness of the juvenile justice system that a cohort faces and the extent of criminal involvement for that cohort later in life.
   
3. Evidence that a substantial fraction of the crime reduction results from deterrence comes from analysis of changes in crime rates around the age of majority. States where juvenile punishments are lenient relative to adult punishments see much greater declines (or smaller increases) in crime as a cohort passes to the adult cohort vs. states with harsher punishments for juveniles tend to see increases in crime rates as the cohort ages into adulthood.

4. Paper argues that taking juveniles into custody is effective at deterring crime. However, this paper cannot make any policy recommendations since the benefits of reduced crime must be measured against the costs of holding juveniles.
	1. Benefits of incarcerating juveniles appears slightly higher but so are the costs of housing them.

#disagree -> large areas of analysis and small sample sizes.