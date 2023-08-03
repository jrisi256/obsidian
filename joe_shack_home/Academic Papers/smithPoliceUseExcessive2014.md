---
type: [Article]
author: [Brad W. Smith, Malcolm D. Holmes]
journal: [Social Problems]
date: 2014-02-01
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Brad W. Smith, Malcolm D. Holmes
* **Title**: Police Use of Excessive Force in Minority Communities: A Test of the Minority Threat, Place, and Community Accountability Hypotheses
* **Date of publication**: 2014-02-01
* **Journal**: Social Problems
* **Volume**: 61
* **Issue**: 1
* **Pages**: 83-104
* **URL**: [https://doi.org/10.1525/sp.2013.12056](https://doi.org/10.1525/sp.2013.12056)
* **Tags**: #comps_exam, #criminology, #crim501, #policing
* **PDF Attachments**:
  * [smithPoliceUseExcessive2014.pdf](zotero://open-pdf/library/items/VR3EH8ZF)

## Abstract

We extend existing research on police use of coercive mechanisms of social control against racial/ethnic minority populations by testing three structural hypotheses regarding excessive force. The minority threat hypothesis maintains that the greater the proportion of minority residents in a city, the greater the use of coercive crime control mechanisms. The place hypothesis argues that spatially segregated minority populations are the primary targets of coercive control. The community accountability hypothesis maintains that organizational characteristics of police departments promote the use of excessive force against minorities. Combining data from several sources for cities with populations of 100,000 or more, we include the key variables of these theoretical models in analyses of sustained excessive force complaints. Findings provide support for the minority threat hypothesis but indicate that place effects are contingent on the existence of a very high degree of racial/ethnic segregation. They offer little support for the community accountability hypothesis.

## My notes

### Results

**Threat Hypothesis** → The greater the number of acts or people threatening to the interests of the powerful, the greater the level of deviance and crime control. Police-citizen relations reflect social divisions rooted in the social structure. Fosters the proclivity of the police to target minorities for aggressive crime control. Police themselves may view minorities as more threatening and respond with more force.
* **Finds support**. [[Minority threat hypothesis]].

**Place Hypothesis** → Spatially segregated minority populations are the primary targets of coercive control. They’re seen as particularly threatening. Police are a distinct social group whose street-level responses to minorities reflect their unique interests. Disadvantaged neighborhoods trigger myriad social psychological responses among police officers making use of force more likely. I.e. it isn't race exactly but interactions of officers with people of a specific race in specific places which triggers an officer to view someone as a threat.
* Finds the strongest support for Black American segregation. No effects, though, for Hispanics.
* Some sense of a segregation tipping point.
* Police response to minority citizens is driven by their unique interests (not necessarily the dominant group) and their unique social psychological processes triggered in interactions with minorities in disadvantaged areas. But may also reflect concerns of White citizens and their perceptions of crime → police departments need resources which get allocated to them.

**Community Accountability Hypothesis** → Imperfect police bureaucracies produce the problem. They’re the primary influencers of street-level police behavior. Inadequate implementation and lack of organizational mechanisms designed to fix police-minority tensions are the cause of violence against minority groups. Characteristics of police agencies account for variable patterns of excessive use of force → formal and informal aspects of the policing department.
* Weakest support. Basically not supported.

Police departments most accountable to the community will have lower counts of excessive force. They do find an effect for increased representation of Black officers.

“Still the effects of percent black and black dissimilarity remain quite large. Simply increasing the representation of Blacks in police departments may not overcome the profound structural inequalities of race and class which characterize many American cities.” #quote #highlight #paper_idea

### Data

Focus on **sustained excessive uses of force complaints** as the dependent variable because general use of force can be classified as justified or not. Minorities may be differentially targeted because they more often represent objective threats (e.g. they are armed more often).

Analyze cities of 100,000 or more residents. [[LEMAS]] has sustained complaint data. Law Enforcement Management and Administrative Statistics Survey. Use [[negative binomial regression]].

* **Controls** → Total population, violent crime rate, region.
  
* **Minority Threat**:
	* Percent black, percent Hispanic. May be linear or quadratic (initially positive then negative once past 50%).
	* Majority/minority income inequality (larger differences, more threatening) → **ratio of median white income to weighted mean of Black/Hispanic median income**.
	  
* **Place** → Black dissimilarity and Hispanic dissimilarity which are measures of segregation.
  
* **Community Accountability** → Ratio of Black officers to citizens, Ratio of Hispanic officers to citizens, Community Policing (index using 8 questions), Citizen complaint review board (present), Early Intervention Systems (present).

### Detailed results

The higher the percentage of Black civilians, the higher the count of excessive force. Same for Hispanic population (but marginally significant). Linear model fits best, not quadratic.

Increase in Black segregation led to higher counts of excessive force. Nonlinear relationship with higher segregation leading to increasingly higher counts of complaints.

As the ratio of Black officers to black civilians increased, counts of excessive force decreased. However, it actually increased for Hispanics.

The more the police practiced community policing, the higher the number of counts of excessive force. Null effects for CCRBs (very few implemented). Marginal effects for early intervention systems but regressions suggest they increase complaints.
