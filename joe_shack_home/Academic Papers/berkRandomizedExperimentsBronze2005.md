---
type:
  - Article
author:
  - Richard A. Berk
journal:
  - Journal of Experimental Criminology
year: 2005
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Richard A. Berk
* **Title**: Randomized experiments as the bronze standard
* **Date of publication**: 2005-12-01
* **Journal**: Journal of Experimental Criminology
* **Volume**: 1
* **Issue**: 4
* **Pages**: 417-433
* **URL**: [https://doi.org/10.1007/s11292-005-3538-2](https://doi.org/10.1007/s11292-005-3538-2)
* **Tags**: #causal_inference, #comps_exam, #experiments
* **PDF Attachments**:
  * [berkRandomizedExperimentsBronze2005.pdf](zotero://open-pdf/library/items/CN7XI4EJ)

## Abstract

In this paper, the strengths and weaknesses of randomized field experiments are discussed. Although it seems to be common knowledge that random assignment balances experimental and control groups on all confounders, other features of randomized field experiments are somewhat less appreciated. These include the role of random assignment in statistical inference and representations of the mechanisms by which the treatment has its impact. Randomized experiments also have important limitations and are subject to the fidelity with which they are implemented. In the end, randomized field experiments are still the best way to estimate causal effects, but are a considerable distance from perfection.

## My notes

Are randomized experiments always good? There are some ways they can fail:

### Stable Unit Treatment Value

* [[Stable unit treatment value]] or SUTVA is particularly troublesome (the idea that the treatment status of one unit does not affect the outcome of another unit):
  
	* In the example of randomizing youths to boot camp or to juvenile detention, one can imagine that if a substantial number of rival gang members are randomly selected to go to the same camp, that would bias one's results.
	  
	* Suppose (different experiment) that some youth in juvenile detention are randomly assigned to drug treatment. The skills they learn in the treatment get passed on to other cellmates who did not participate in the treatment.
	  
	* The only known way to combat interference is if one can accurately model the interference.
	  
* Suppose you then shift the unit of analysis to facilities rather than individuals, the interactions of juveniles within a given facility no longer matter.
  
	* However, the substantive research question has changed. What is the effect of treatment on the facility as a whole? It also leads to a reduction in sample size and a lose in statistical precision.

### Interaction Effects

* Suppose the effect of treatment (sending a youth to boot camp or juvenile detention) had different effects depending on the age of the boy.
  
	* Age is likely correlated with other relevant variables (e.g., criminal history) which are also correlated with the outcome variable (in this example, recidivism). Author argues this leads to a resurfacing of the problem of [[confounders]].
	  
		* I would agree this is a problem which can arise during the search for [[treatment heterogeneity]] -> This is not a problem with calculating the [[ATE]], the question here would be is it age or criminal history which is an important [[moderator]] of the treatment? In such instances, a [[fully blocked randomized experiments]] would be quite useful.
		  
		* The author does indeed go on to talk about this. They mention though that any post-hoc moderation analysis should be considered exploratory at best.

The main point being that more can learned from an experiment than just the average treatment effect (e.g., speculation concerning how the effect is generated and attempting to account for that).

### Non-statistical benefits and costsof experiments

**Benefits**
1. Easy to explain to funders.
2. They can be seen as fair since everyone has an equal chance.
3. The analysis is often more simple and straightforward thus easier to present to a lay audience.

**Costs**
1. The methodology is inflexible and has to be followed rigidly -> if not, it has to fully accounted for beforehand.
2. Stakeholders might claim they already know what works.

### Generalizability concerns

* Individuals may behave differently if they know they are in an experiment.
* Attempting to hide the fact that participants are in an experiment, or what the experiment is, can be unethical.

**How to generalize**:
1. Probability sample of subjects.
2. Use a suite of studies with different mixes of subjects, in different settings, with related outcomes.
3. Compare experiments, quasi-experiments, and observational studies.
4. Use theory to better understand how results might generalize.

### Implementation concerns

* Attrition problems if people do not show up or drop out of the experiment -> bias results and loss of power.
  
* There can be issues around the randomization procedure being faithfully followed.
  
* Compliance issues.
  
* The outcome variable might be poorly measured (e.g., if the assignment variable is correlated with the outcome variable such as if an individual's self-reported crime levels are dependent upon the treatment received).