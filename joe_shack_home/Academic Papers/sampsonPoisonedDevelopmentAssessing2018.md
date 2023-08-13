---
type: [Article]
author: [Robert J. Sampson, Alix S. Winter]
journal: [Criminology]
date: 2018
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Robert J. Sampson, Alix S. Winter
* **Title**: Poisoned Development: Assessing Childhood Lead Exposure as a Cause of Crime in a Birth Cohort Followed Through Adolescence
* **Date of publication**: 2018
* **Journal**: Criminology
* **Volume**: 56
* **Issue**: 2
* **Pages**: 269-301
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9125.12171](https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9125.12171)
* **Tags**: #comps_exam, #theory_advancement, #life_course
* **PDF Attachments**:
  * [Sampson and Winter - 2018 - Poisoned Development Assessing Childhood Lead Exp.pdf](zotero://open-pdf/library/items/9DPJSCHB)

## Abstract

The consequences of lead exposure for later crime are theoretically compelling, but direct evidence from representative, longitudinal samples is sparse. By capitalizing on an original follow-up of more than 200 infants from the birth cohort of the Project on Human Development in Chicago Neighborhoods matched to their blood lead levels from around age 3 years, we provide several tests. Through the use of four waves of longitudinal data that include measures of individual development, family background, and structural inequalities in how lead becomes embodied, we assess the hypothesized link between early childhood lead poisoning and both parent-reported delinquent behavior and official arrest in late adolescence. We also test for mediating developmental processes of impulsivity and anxiety or depression. The results from multiple analytic strategies that make different assumptions reveal a plausibly causal effect of childhood lead exposure on adolescent delinquent behavior but no direct link to arrests. The results underscore lead exposure as a trigger for poisoned development in the early life course and call for greater integration of the environment into theories of individual differences in criminal behavior.

## My notes

### Introduction

* Our knowledge of the connections between childhood lead exposure and the [[Life course theory|life-course]] development of crime is quite limited and not much research has been done longitudinally (with direct biological measures of childhood lead exposure) to show the connections. What research that has been done, though, demonstrates a potentially positive association.
  
* Theorize about the mechanisms through which lead exposure in infancy can exert negative long-term consequences. Strive to integrate their findings within the life-course perspective.
  
* Conceive of childhood lead poisoning as an adverse transition of turning point within the life of children.
	* Argue exposure to lead is more exogenous than many of the other commonly discussed turning points and transitions within life-course criminology.
	* Individual differences in character (which predict delinquency) are constituted by the broader environmental context and the structural and historical forces which expose different groups of people to more/less lead.
	* Life-course needs to better consider people's environment in which they live and how it sets you up on a particular trajectory -> goes beyond genetic, family, situational, or neighborhood social environments generating individual differences but also the ecological environment and the structural and historical forces which give rise to these environments.
	  
* Environmental policy is also crime policy (although this study is not a policy study and cannot speak to how much exposure to lead did or did not lead to national reductions in crime). Expand our analysis to beyond criminal justice institutions to understand how *non-crime related institutions* still can affect crime.
	  
* **H1** -> There is a long-term connection between exposure to lead in infancy and self-reported delinquent behavior in adolescence.
* **H2** -> Use multiple analytic strategies to assess the extent to which the relationship is causal.
* **H3** -> Assess the mediators of lead exposure and deviant behavior e.g., impulsive behavior and anxiety/depression.
* **H4** -> Is there an association between childhood lead exposure and official arrests in adolescence?

### Data and Methods

* Data comes from the [[PHDCN-CS]] follow-up of the original birth cohort.
* **Main independent variable** -> childhood lead exposure. Worked with the Chicago Department of Public Health who regularly test children for lead exposure. Use the average reading across test results from years 0 - 5 for the children.
* **Dependent variables**
	* **Self-reported delinquent behavior** -> Ages 16-18 of children. Use the antisocial behavioral scale from the [[Child Behavior Checklist]] (CBCL). Asked the sample member's primary caregivers if they had engaged in a variety of delinquent actions like: bullying, lying, cheating, being disobedient in school, etc.
	* **Official arrest** -> age 21.
* **Mediators** -> Average measures of subject impulsivity and depression in earlier waves.
* **Pre-treatment controls** -> race, sex, parental educational level and poverty status, proportion of individuals in each block group that is Black, Hispanic, below the poverty line, etc.

### Results

* Figure 1 -> Simple correlational analysis indicates a significant positive relationship between lead exposure and future antisocial behavior.
* Table 2 -> [[OLS]] regression indicates a statistically significant association between lead exposure and future antisocial behavior.
* Use [[coarsened exact matching]] to match similar children except on lead exposure (those with lead exposure greater than equal to a high amount vs. those below that amount) table 3 -> indicates effects of lead exposure.
* [[instrumental variable]] -> **Proximity to historic smelting plants** (where the lead remained in the environment particularly the soil) where it is argued that:
	1) It causes childhood exposure to lead in a quasi-random fashion.
	2) It only affects adolescent antisocial behavior through childhood lead exposure.
	3) It is conditionally random when controlled for on observable covariates -> also argue the lingering effects were not known until recently so people were likely not selecting to live/not live in certain areas to avoid being near where a smelting plant used to be.
	4) Effects using linear distance are positive but insignificant.
	5) Effects using log distance are positive and marginally significant.
* Table 5 -> Surprisingly the effects of lead exposure are not really mediated by impulsivity and anxiety.
* Table 6 -> [[negative binomial regression]] to estimate the effects of lead exposure on arrests. Positive and insignificant relationship to violent crime but negative (and sometimes significant) relationship with property crime (very strange).
	* Lead exposure is a weak signal of being arrested in the future -> **authors very puzzled by this result**.