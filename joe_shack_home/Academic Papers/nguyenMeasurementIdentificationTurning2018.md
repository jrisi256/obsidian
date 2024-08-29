---
type:
  - Article
author:
  - Holly Nguyen
  - Thomas A. Loughran
journal:
  - Annual Review of Criminology
year: 2018
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Holly Nguyen, Thomas A. Loughran
* **Title**: On the Measurement and Identification of Turning Points in Criminology
* **Date of publication**: 2018
* **Journal**: Annual Review of Criminology
* **Volume**: 1
* **Issue**: 1
* **Pages**: 335-358
* **URL**: [https://doi.org/10.1146/annurev-criminol-032317-091949](https://doi.org/10.1146/annurev-criminol-032317-091949)
* **Tags**: #comps_exam, #theory_advancement, #life_course
* **PDF Attachments**:
  * [nguyenMeasurementIdentificationTurning2018.pdf](zotero://open-pdf/library/items/QV9WRTNX)

## Abstract

Since their introduction to criminology, turning points have been of substantial theoretical and empirical focus for scholars of desistance. In this review, we consider how criminologists have sought to identify change in the criminal career by reflecting on the identification and measurement of turning points. We contend that important life events, such as marriage and employment, are endogenous to the desistance process and as such present challenges for scholars regarding the causal identification of turning points. Specifically, we argue that both selection bias and simultaneity bias are fundamental principles of the life-course framework. We present a formal way to think about the causal identification of turning points in the face of endogeneity and also consider several conceptual issues relating to the definition and measurement of turning points. In the end, we encourage scholars to adopt creative methodological strategies to unpack turning points.

## My notes

### Introduction

* Military service, marriage (increased social bonding and informal social control), and employment (similar arguments) have become three of the most common types of salient life events or turning points theorized to bring about opportunities for change and are capable of altering an individual's behavior trajectory -> [[sampsonCrimeDevianceLife1990]], [[sampsonLifeCourseViewDevelopment2005]], [[laubTurningPointsLife1993]].
	* Other turning points have been identified, though -> parenthood, gang membership, residential change, dropping out of high school.
  
* Key problem -> Life events such as marriage and employment are endogenous and is linked to the problem of [[causal identification]]. [[selection bias]] and [[simultaneity bias]] have not been adequately addressed in the literature.

### Review of turning points

* *Trajectories* are long-term patterns of behavior and *transitions* are embedded within trajectories. Transitions are usually age-graded, span shorter periods of time, and modify trajectories. Three variables which influence trajectories and transitions.
	* **Location in time and place** -> The context in which a person lives their life.
	* **Linked lives** -> One's connections with people and their role in society.
	* **Human agency** -> One's trajectory is constructed by choices and actions made by individuals in response to opportunities and constraints which appear due to the above 2 variables closely linked to the idea of **cumulative disadvantage** or how later transitions are linked to earlier transitions -> trajectories are the accumulation of factors.
	  
* Processual nature of turning points -> cannot be viewed as a singular event.

### Empirical state of turning points

* If turning points are indeed processual, measuring them is quite hard. Are they abrupt shifts or a gradual process? Can they only be identified retroactively in which case how useful are they as a scientific concept?
  
* [[Group-based mixture models]] have been used to identify population heterogeneity in offending over time, but these methods mask any changes happening. These methods cannot uncover any causal effect of turning points.
  
* [[omitted variable bias]], time dependency, and interdependency of turning points.
  
* Robust longitudinal evidence for marriage/employment and desistance. However, this is a causal identification problem. The correlation could be spurious. To qualify as a turning point, it must be demonstrated they cause a change in the behavior trajectory.
	* Stated simply, comparing individuals who get married to those who do not is not an apples-to-apples comparison. The two groups likely differ in important ways before the event and future outcomes may be related to these differences. The event itself (i.e., marriage) may not actually be important, at all.
	* Selection bias -> those who select into marriage are different from those who do not in ways that is important to the outcome of interest.
	* Simultaneity bias and reverse causality -> Offending alters marriage or employment rather than the other way around or in addition to.
	  
* Endogeneity -> Marriage is endogenous. It is an event related to other factors which also likely influence the outcome of interest.
 
### Limitations of current methodological approaches

* One way to address selection is through [[propensity score matching]]. The idea being, based on observable variables, two individuals have the same probability of entering into marriage but one does and the other does not presumably due to random chance or for reasons which would not affect the outcome.
	* Have to believe we are controlling for all the ways in which individuals are meaningfully different.
  
* Other studies use fixed effects for individuals so an individual, in some sense, represents their own counterfactual. Of course, if there are unobserved confounders that are time varying, the interpretation cannot be causal.
	* It is likely that such variables as attitudes and criminal propensity which are important for explaining marriage/employment but also the outcome are time varying.
	  
* [[Experiment]] studies on the effects of employment have come to mixed results concerning the ability for employment to lead to desistance.
  
* However, these approaches, while laudable, do not explicitly model the selection but try to control it away. Furthermore, they cannot deal with reverse causality or simultaneity. Longitudinal studies can control for unmeasured, stable differences across individuals, but they are not as good as capturing dynamic individual-level factors.
	* I.e., dealing with selection bias, only, cannot control for simultaneity.
	* One solution is the identification of an instrumental variable which affects entry into the life event but is unrelated to the outcome (except through the life event). However, identifying valid instruments is really hard.
	  
* Authors argue in some ways, the causal identification of the *turning point* does not do justice to the idea of turning points which are supposedly processual. we should be modeling how these life events and future offending are mutually reinforcing.
	* [[Group-based trajectory models]] -> Social bonds (as signaled by marriage or employment) are like investments which strengthen slowly over time eventually resulting in a strong bond. These events do not represent abrupt changes.
	  
* Causal identification is important but so is:
	* Treatment heterogeneity -> type and circumstance of employment and marriage are different for every individual.
	* Treatment-effect heterogeneity or moderation -> people, depending on some set of variables (and when in the individual's life the event happens), are likely to have different responses to these life events or treatments.
	* How generalizable are our results? Past studies have been implicitly estimating the [[ATT]] or the average effect of the treatment on the treated (among those who were treated, what was the average effect?). This is different from the [[ATE]] or the average treatment effect (what is the average effect, in general, of the treatment?)
		* Instrumental variables introduce another complication -> [[LATE]] or the Local Average Treatment Effect in which effects are only calculated for those who were induced to treatment by the instrument (cannot say anything about the effect for those who were not affected by the instrument).
		* The only way to go from ATT to ATE is to assume constant treatment effect i.e., that the people who got the treatment are similar to those who did not in ways that are relevant to the outcome.

### Future research

* How long must an event cause a change in behavior for it to be recognized as a turning point? This also means the outcome of a turning point should be a new trajectory and not a singular outcome.
	* They really love group-based trajectory modeling.
	  
* In the end, treating [[Life course theory|life-course]] as a causal inference problem is not doing the problem full justice.
	* It is important, of course, to consider problems of selection and simultaneity. But as we move into that realm, we need to be attendant to the assumptions and limitations of such methods, too.