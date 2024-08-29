---
type:
  - Article
author:
  - Joscha Legewie
  - Jeffrey Fagan
journal:
  - American Sociological Review
year: 2019
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Joscha Legewie, Jeffrey Fagan
* **Title**: Aggressive Policing and the Educational Performance of Minority Youth
* **Date of publication**: 2019-04-01
* **Journal**: American Sociological Review
* **Volume**: 84
* **Issue**: 2
* **Pages**: 220-247
* **URL**: [https://doi.org/10.1177/0003122419826020](https://doi.org/10.1177/0003122419826020)
* **Tags**: #comps_exam, #policing, #racial_inequality 
* **PDF Attachments**:
  * [legewieAggressivePolicingEducational2019.pdf](zotero://open-pdf/library/items/CSM5Y7WN)

## Abstract

An increasing number of minority youth experience contact with the criminal justice system. But how does the expansion of police presence in poor urban communities affect educational outcomes? Previous research points at multiple mechanisms with opposing effects. This article presents the first causal evidence of the impact of aggressive policing on minority youths’ educational performance. Under Operation Impact, the New York Police Department (NYPD) saturated high-crime areas with additional police officers with the mission to engage in aggressive, order-maintenance policing. To estimate the effect of this policing program, we use administrative data from more than 250,000 adolescents age 9 to 15 and a difference-in-differences approach based on variation in the timing of police surges across neighborhoods. We find that exposure to police surges significantly reduced test scores for African American boys, consistent with their greater exposure to policing. The size of the effect increases with age, but there is no discernible effect for African American girls and Hispanic students. Aggressive policing can thus lower educational performance for some minority groups. These findings provide evidence that the consequences of policing extend into key domains of social life, with implications for the educational trajectories of minority youth and social inequality more broadly.

## My notes

### Research Question

* Investments into policing are credited with reductions in crime but we know little about the social costs of such expansions.
  
* What are the consequences of increasing the presence of police in minority communities for minority youths' educational performance?
  
	* **H1** -> Policing has a positive effect because it reduces the neighborhood level of crime and violence which in turns increases school performance.
	  
	* **H2** -> More policing and more aggressive policing may undermine trust in authorities (including schools and teachers) due to constant conflict with the police. This can lead to withdrawal and [[system avoidance]] (the avoiding of formal institutions which keep formal records of an individual), induce stress or other health problems, and eventually lead to decreased educational performance. [[Legal cynicism]].

* Focus on NYPD's Operation Impact which increased the intensity of [[Broken windows hypothesis]] policing in selected neighborhoods. Targeted disorderly behaviors through strict enforcement of low-level crimes and extensive use of pedestrian stops. Led to a substantial increase in policing activity and a modest decrease in violent crime.
  
* Improves upon prior research:
  
	* Prior research on the link between the criminal justice system and child development focuses on parental incarceration AND not on law enforcement.
	  
	* There has been much research concerning the effects of police stops and a variety of outcomes, but the consequences of policing for youth have largely been ignored. Youth are particularly important to study because they are the age group most likely to come into contact with the police, and this contact has the potential to shape long-term outcomes for the youth.
	  
	* Prior research has focused on direct contact with the criminal justice system but not enough attention has been paid to police contact's effects on the whole community.
		* Indirect contact (e.g. through friends) can shape views of law enforcement and shape [[Legal cynicism]].
	* #highlight #paper_idea #papers_to_read

### Data and Methods
  
* Operation Impact had a staggered release in which the number of officers in high-crime areas were rapidly increased at different times.
  
	* From 2004 to 2012, the NYPD continuously modified the program over 15 phases by expanding, moving, removing, or adding *impact zones* generally every 6 months.
	  
	* Impact zones varied in such from very small areas (residential buildings or public housing) to very large areas such as entire precincts. On average, these areas would remain an impact zone for about a year (a lot variation).
	  
	* High concentration of officers led to a substantial increase in policing activity which returned to previous levels after the area was no longer designated an impact zone.
	  
	* They have the shape file data on which areas of the city were impact zones and during which periods of time were these areas of land designated as an impact zone.
	  
* Have data on stops, arrests, and number of reported crimes to the police.
	  
* Link impact zones with administrative data from the NYCDOE on public-school students.
  
	* Student level records for all public-school students in NYC in grades Kindergarten through 8th grade. Includes demographic information, eligibility for free school lunch, English-learner status, yearly test scores for students in grades 3 through 8, and student residential neighborhood.
  
* They use a [[difference in differences]] approach to make causal claims with their longitudinal data.
  
	* Simple observational analyses cannot deal with confounders since these neighborhoods were chosen specifically for having high crime. Thus, variables like poverty may be both causing the treatment as well as the outcome causing confounding.
  
	* Focusing on a students' home residence, they compare changes in test scores before, during, and after treatment in those neighborhoods which were exposed to the treatment to those neighborhoods which were not exposed to the treatment (but eventually would become designated as impact zones).
	  
	* They condition on prior crime for each neighborhood and fixed effects of the neighborhood, and I assume they will argue the neighborhoods are exchangeable otherwise and will have similar trends in educational outcomes prior to the treatment.
		* Model adjusts for all time-constant differences across neighborhoods.
		  
	* Core assumption is that in the absence of Operation Impact and conditional on the control variables, changes in test scores of students exposed to the treatment would be the same as changes in test scores in the control group i.e., [[parallel trends assumption]].
	  
		* Main threat are time-varying, neighborhood level variables related to the selection of impact zones and student outcomes and not captured in the models -> figure 2, no pre-treatment trends.
	  
* Analysis is at the student-level. The sample is restricted to areas designated as an impact zone at least once.
  
* ~285,000 students with ~828,000 student-year observations. Model is restricted to Black and Hispanic students because too few White and Asian students are exposed.
  
#### Model

There are 2 models. The first model does not include any student-level variables. The second model does. [[Clustered standard errors]] at the neighborhood level. Use [[fixed effects]] and [[OLS]].

Models are estimated separately by race and gender.

**Dependent Variable**

* English and math test scores for a specific student in a specific neighborhood in a specific year in a specific grade.

**Independent Variables**

1. Student fixed effects.
2. Time-varying student level control variables.
	1. Eligibility for free and reduced price lunch.
	2. English learner status.
	3. Age
3. **Treatment variable at the neighborhood-year level** is the number of a days a student lived in an impact zone.
4. Neighborhood fixed effect.
5. Grade by year interacted fixed effect.
6. Time-varying variables at the neighborhood-level
	1. Number of violent and property crimes in the six months prior to the selection of impact zones.
7. Lead and lag terms for estimating test scores prior to the impact zone designation (e.g., for lag terms, variable = 1 for those time periods prior to the intervention.
8. Neighborhoods are defined by splitting the 76 police precincts into 1,257 areas with at least one student based on the boundaries of the impact zones.

#### Mediation Analysis

* Estimate the effect of Operation Impact on crime at the neighborhood level using [[negative binomial regression]].
  
* Estimate the effect of Operation Impact on school-related attitudes (as obtained from administrative data surveys) and on school attendance at the individual level (or student).

### Results

* They find that Operation Impact lowered the educational performance of Black boys.
	* Figure 1 -> As Black boys get older, their test scores suffer more and more as a result of exposure to Operation Impact.
	  
	* Figure 2 -> Effects attenuate but persist up to 2 years after the exposure has ended (thankfully there is no pre-treatment difference).
	  
	* Figure 4 -> Results mirror trends in police contact for student demographic groups (i.e., this result is consistent with the hypothesized causal mechanism, police contact).
	  
	* Figure 5 -> Goes along with figure 4. Crime has a consistent negative influence on student achievement across all demographic groupings. Thus, it would suggest that crime is not confounding the results. If it were, you would expect to see negative results across the board (or even positive results since crime is theoretically declining).
  
* The effect size was small and insignificant for other groups -> figure 3.
  
* Operation Impact reduced crime, but it also reduced school attendance.
  
	* Figure 6 -> If crime were driving the results, you would expect to positive effect on student achievement (even though this figure shows declining crime). Effects on crime were also short-lived as areas returned to previous levels of crime within 6 months. Only found effects for violent crime.

	* Figure 7 -> No impact on school attitudes. Decreased school attendance.
  
* Aggressive policing tactics can lower educational performance and perpetuate racial inequity.

### Joe Thoughts

#paper_idea 
* You have to be careful with these moderation analyses to not go fishing for results. These results make me a little suspicious because results were found for only one sub-group. Of course, theoretically it is the subgroup you would expect to find results for.
  
* Gets at ideas of [[cumulative disadvantage]] as found in [[kurlychekCumulativeDisadvantageAmerican2019]].
  
* [[Social costs of policing]] -> see page 21 and the paper cited #papers_to_read 