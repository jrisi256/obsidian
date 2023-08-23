---
type: [Article]
author: [Robert J. Sampson]
journal: [Journal of Quantitative Criminology]
date: 2010-12-01
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Robert J. Sampson
* **Title**: Gold Standard Myths: Observations on the Experimental Turn in Quantitative Criminology
* **Date of publication**: 2010-12-01
* **Journal**: Journal of Quantitative Criminology
* **Volume**: 26
* **Issue**: 4
* **Pages**: 489-500
* **URL**: [https://doi.org/10.1007/s10940-010-9117-3](https://doi.org/10.1007/s10940-010-9117-3)
* **Tags**: #causal_inference, #comps_exam
* **PDF Attachments**:
  * [sampsonGoldStandardMyths2010.pdf](zotero://open-pdf/library/items/R2TC5Z4D)

## My notes

### Problems or myths of experiments

#### Sample selection and compliance

* Our samples are not random (e.g., prisoners, courts, high-crime neighborhoods) even if the randomization procedure itself is random. Since treatment effects are not homogeneous and depend upon the distribution of traits in a neighborhood, it is unclear how well the results from experiments generalize.

	* #disagree -> I do not know how much of a problem this is. It is a problem, but I do not think it is always a big problem. Think of [[judge instrumental variables]]. We cannot say anything about the effects of incarceration for those unlikely or very likely to be incarcerated (although we can probably imagine), but the policy-relevant and theory-relevant sample is already for the sample under study.
	  
* Humans exert choice in whether or not they accept the treatment/control, anticipate future outcomes, and discuss the treatment with fellow subjects. This is going to bias your results, and experiments can no longer be assumption-free as people would like them to be -> [[Stable unit treatment value]].
  
* Causal inference cannot explain the mechanisms which are driving the observed changes. Explaining mechanisms requires theory. We have been too devoted to thinking like a lab physicist and not enough like an evolutionary biologist (e.g., Darwin came up with his theories using no experiments) -> science is not about method but about principles and procedures for the systematic pursuit of empirical knowledge -> draw rigorous conclusions on the basis of data from a variety of sources.

#### Assumptions

As outlined above, experiments still require assumptions. Author takes particular aim at SUTVA -> rules out contagion, information diffusion, jealousy, and most importantly learning.

* E.g., See [[Moving to Opportunity]]. Suppose I was a complier in a poor origin neighborhood and moved to a wealthy neighborhood. Suppose then I talked to friends back in the original neighborhood after moving (who also have vouchers), about how great (or bad) the move was. This would influence their outcomes and also compliance.
  
* To tackle SUTVA requires more theory specifically being able to model the interference.
  
* Changing the analysis level to groups presents its own problems like interference among groups (e.g., see classrooms in a school) but also how stable the group is.

#### Policy relevance

* See [[naginRealGoldStandard2019]] for an extended discussion of this issue. This issue can be thought of as an extended problem of [[external validity]]. How relevant for policy and system-wide change are causal inference studies? It depends on how much we already know about the system, and that knowledge might have to come from observational data.
  
	* E.g., suppose a policy intervention shows that busing Black children to Whiter and wealthier schools improves education outcomes. Further suppose, it is a rigorous study and the causal effect is well-estimated. The experiment can tell us nothing about what will happen if this is adopted system-wide as a policy. Sampson poses this provocatively to prove a point (see [[white flight]]).
	  
	* Similar to the idea of [[aggregation bias]] -> homology or processes across different levels cannot be assumed.
	  
	* What worked in the past gives us some indication of what might work in the future, but we need theory and substantive knowledge to know. 