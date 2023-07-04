---
type: [Article]
author: [Stephanie Ann Wiley, Lee Ann Slocum, Finn-Aage Esbensen]
journal: [Criminology]
date: 2013
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Stephanie Ann Wiley, Lee Ann Slocum, Finn-Aage Esbensen
* **Title**: The Unintended Consequences of Being Stopped or Arrested: An Exploration of the Labeling Mechanisms Through Which Police Contact Leads to Subsequent Delinquency
* **Date of publication**: 2013
* **Journal**: Criminology
* **Volume**: 51
* **Issue**: 4
* **Pages**: 927-966
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9125.12024](https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9125.12024)
* **Tags**: #comps_exam, #criminology, #labeling_theory, #theory_advancement
* **PDF Attachments**:
  * [wileyUnintendedConsequencesBeing2013.pdf](zotero://open-pdf/library/items/YVG85WGF)

## Abstract

Much debate has taken place regarding the merits of aggressive policing strategies such as “stop, question, and frisk.” [[labeling theory|Labeling theory]] suggests that police contact may actually increase delinquency because youth who are stopped or arrested are excluded from conventional opportunities, adopt a deviant identity, and spend time with delinquent peers. But, few studies have examined the mechanisms through which police contact potentially enhances offending. The current study uses four waves of longitudinal data collected from middle-school students (N = 2,127) in seven cities to examine the deviance amplification process. Outcomes are compared for youth with no police contact, those who were stopped by police, and those who were arrested. We use propensity score matching to control for preexisting differences among the three groups. Our findings indicate that compared with those with no contact, youth who are stopped or arrested report higher levels of future delinquency and that social bonds, deviant identity formation, and delinquent peers partially mediate the relationship between police contact and later offending. These findings suggest that programs targeted at reducing the negative consequences of police contact (i.e., poor academic achievement, deviant identity formation, and delinquent peer associations) might reduce the occurrence of secondary deviance.

## My notes

### Introduction

Early labeling theorists were dismissed due to the lack of empirical findings upholding their predicted results. [[paternosterLabelingPerspectiveDelinquency1989]] suggested the theory was not being properly tested, and the mechanisms leading to delinquency needed to be properly elaborated upon. Argued criminal justice contact affects later offending through a complex process in which labeled youth may (this is not inevitable) -> the important first step is social exclusion:

* be barred from access to conventional others -> societal rejection or withdrawal from others. Attachment to social bonds are cut off (see [[Social control theory|social control]]).
* develop a deviant identity -> reorganization of behavior and attitudes as the person's values and norms shift.
* become involved in delinquent groups.

#### Selection effects

* Individuals with justice system contact may have characteristics and attributes which predispose them to future delinquency. Thus the relationship between labeling and future delinquency is confounded by these higher order variables.

### Data and methods

* Four waves of longitudinal data to assess the effects of police stops and arrests relative to no police contact as well as police arrests vs. police stops. It seems like the four waves were annual?
  
* Propensity score matching is used to match similar individuals wherein it is argued, conditional on the observed variables, assignment to the treatment (police contact or arrest) is as good as random. Use [[multinomial]] [[probit]] regression modeling.
  
* Uses [[Structural equation modeling]] to understand mediators. Use [[bootstrapped standard errors]].
  
* Data comes from the [[Gang Resistance Education and Training]] program -> middle schools across the country.
  
* Control measures and measures used to create the propensity score are measured at T1. Police contact is measured in T2 and T3. Mediators are measured at T3. Delinquency is measured at T4.
  
* **Dependent variable** -> Delinquency. How many times int he last 6 months did you participate in 14 different delinquent activities? Summed to create a frequency score. [[Log transform]] the dependent variable and add 1 (negative binomial does not play well with SEM). Use robustness checks of [[negative binomial regression]] and also a variety score of delinquency.
  
* **Independent variable** -> Police respondents were asked how many times in the past 6 months had you been stopped by the police and arrested? Dichotomized into binary variables.
  
* **Mediators**:
	* **Social exclusion/attenuated bonds** -> school commitment, academic achievement, involvement in various prosocial activities.
	* **Deviant Identity** -> survey questions (acceptability of crime).
	* **Deviant group involvement** -> Asked about friends involvement in delinquency.

### Results

* Most students had not had any police contact. Descriptively, as contact severity increased, respondents reported less commitment to school, worse grades, more social exclusion, more delinquent attitudes, greater involvement with deviant peers, and higher levels of delinquency.
  
* Being stopped or arrested (vs. no police contact) was associated with higher levels of delinquency and weakened conventional bonds and exclusion from prosocial others, more delinquent attitudes, and more involvement with delinquent peers.
	* Did find that being arrested vs. being stopped was associated with higher delinquency. Arrested youth also tend to fare worse on several of the mediators including school commitment and achievement and associations with delinquent peers (but no difference in neutralization techniques, involvement with prosocial others).
	  
* Associating with delinquent peers appears to be the strongest mediator.
* "... simply being stopped by the police has negative ramifications for the youth." #quote 
  
* Mediating mechanisms:
	* Social bond measures did not seem to be important mediating mechanisms. Only academic achievement as measured by grades emerged as a significant mediating mechanism. Perhaps a result of the sample? Youth look up to their delinquent peers thus social exclusion is less of a factor.
	* Support for changes in identity as measured by beliefs and attitudes.
	* Delinquent peer group? ***Commitment to your negative peer group*** It is only a significant mediator in stopped vs. no contact (not in arrest vs. no contact nor in arrest vs. stopped). Stops and arrests lead to more delinquency via different pathways?
		* Statistical artifact because the arrest group is so small.
		* Regardless, ***time spent with delinquent peer group*** is largest and most significant mediator across all conditions.

### Limitations and Policy Considerations

* Omitted variable bias still a concern.
* *Interesting policy recommendations* to say the least:
	* How does contact with the police transform into worse grades? Absence from school? Differential treatment by teachers? Need to address this.
	* Programs designed at changing attitudes and views around crime.
	* **Do not recommend** programs designed to help them make more prosocial friends or engage in more prosocial activities.
		* Instead, curtail their associations with deviant peers.
* Why do some individuals undergo a labeling transformation?