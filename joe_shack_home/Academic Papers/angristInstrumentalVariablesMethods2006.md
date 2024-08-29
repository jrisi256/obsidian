---
type:
  - Article
author:
  - Joshua D. Angrist
journal:
  - Journal of Experimental Criminology
year: 2006
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
## Metadata

* **Author(s)**: Joshua D. Angrist
* **Title**: Instrumental variables methods in experimental criminological research: what, why and how
* **Date of publication**: 2006-04-01
* **Journal**: Journal of Experimental Criminology
* **Volume**: 2
* **Issue**: 1
* **Pages**: 23-44
* **URL**: [https://doi.org/10.1007/s11292-005-5126-x](https://doi.org/10.1007/s11292-005-5126-x)
* **Tags**: #causal_inference, #comps_exam, #instrumental_variable
* **PDF Attachments**:
  * [angristInstrumentalVariablesMethods2006.pdf](zotero://open-pdf/library/items/DGCKZI27)

## Abstract

Quantitative criminology focuses on straightforward causal questions that are ideally addressed with randomized experiments. In practice, however, traditional randomized trials are difficult to implement in the untidy world of criminal justice. Even when randomized trials are implemented, not everyone is treated as intended and some control subjects may obtain experimental services. Treatments may also be more complicated than a simple yes/no coding can capture. This paper argues that the instrumental variables methods (IV) used by economists to solve omitted variables bias problems in observational studies also solve the major statistical problems that arise in imperfect criminological experiments. In general, IV methods estimate causal effects on subjects who comply with a randomly assigned treatment. The use of IV in criminology is illustrated through a re-analysis of the Minneapolis domestic violence experiment. The results point to substantial selection bias in estimates using treatment delivered as the causal variable, and IV estimation generates deterrent effects of arrest that are about one-third larger than the corresponding intention-to-treat effects.

## My notes

The compliance problem in experiments:

1. Compliers -> Those who comply with their treatment status.
	1. The average causal effect for compliers is the [[Local Average Treatment Effect]] or LATE.
	   
	2. [[instrumental variable]] approach can capture the average causal effect of a treatment on those whose treatment status can actually be changed by the instrumental variable.
	   
	3. Different from the [[treatment effect on the treated]] or TOT (ATET) which estimates the average causal effect only for those treated (which will likely not be equal to the ATE in cases of non-experiments because people are willfully choosing to get the treatment or not and such decisions are likely made on the basis of variables which are correlated with the outcome) -> [[selection bias]] which means treatment status is correlated with the outcome and we cannot cleanly estimate the causal effect of the treatment.
	   
		1. I believe TOT is specifically invoked in cases of one-sided non-compliance (i.e., everyone who is assigned to the treatment receives the treatment while not everyone assigned to the control receives the control). The TOT estimator will then be an average of: **1)** compliers assigned to treatment and **2)** always-takers.
		   
		2. In the case where there are no always-takers (i.e., everyone assigned to the control, receives the control and not the treatment), everyone assigned to treatment has to be a complier (can still have never-takers and defiers, of course). In this case, the LATE is equal to the ATT (TOT, ATET). 
	   
2. Defiers -> Those who will do the opposite of their treatment status.
3. Never takers -> Regardless of treatment status, they never receive the treatment.
4. Always takers -> Regardless of treatment status, they will always get the treatment.

In general, the problem is one of [[treatment dilution]] -> assigned to treatment but you are not treated (could be a rebel or a never taker) and [[treatment migration]] -> assignment to control but receive the treatment (could be a rebel or a always taker).

It is a problem that those who comply in a random experiment are not doing so randomly. E.g., in medicine, it is common for compliers to be much healthier than non-compliers. I.e., the subjects who complied with treatment status did so likely due to some unobserved (potentially observed) features of the situation likely correlated with the outcome. It is a problem of [[endogeneity]] or [[confounders]]. Problem of [[selection bias]].

Most research reports the [[intend-to-treat]] or ITT effect. ITT compares those assigned to treatment to those who were not regardless of whether or not they actually received the treatment. They provide unbiased estimates of the researchers' intention to treat, sometimes known as the policy effect. They are conservative estimates, though, and often too conservative estimates of the [[average treatment effect]] or ATE.

Re-estimates models from the domestic violence experiment talked about in [[walkerTamingSystemControl1993]] and [[berkDeterrentEffectArrest1992]]. Finds that instrumental variables can be useful in recovering the local average treatment effect which may be more useful than the intention to treat effect. 

1. There was considerable selection bias in the decision to not comply with the *coddling treatment* i.e., if you were assigned to arrest, you complied. If you were not assigned to arrest, there were likely reasons (correlated with the outcome of recidivism) why you did not comply.
   
2. Non-compliance was important enough to matter because the instrumental variable results indicate the LATE effect of arrest (which is the same as the ATET of arrest in this case) were about 1/3rd larger than the ITT effects of arrest. The effects of arrest were being slightly diluted by those cases where the officer did not arrest someone even though they were assigned to arrest (very unlikely those individuals would recidivate, I imagine the argument goes) -> but more importantly, they were not including those cases in which an officer did arrest someone even though they were assigned to the not arrest condition.
   
	1. Additionally, the instrumental variable estimates of coddling were about twice as large. This is likely due to the fact that individuals who were coddled were very unlikely to recidivate in the first place, and the effect was biased downwards from those individuals who were assigned to the coddle condition but were rearrested.
	   
3. The deterrent effects were higher than originally estimated as a result of this new analysis.
	1. #question Is a side effect of this analysis that the coddling estimates were also much larger? So that the treatment should be targeted appropriately?