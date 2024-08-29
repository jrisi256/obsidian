---
type:
  - Article
author:
  - Daniel S. Nagin
  - Robert J. Sampson
journal:
  - Annual Review of Criminology
year: 2019
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Daniel S. Nagin, Robert J. Sampson
* **Title**: The Real Gold Standard: Measuring Counterfactual Worlds That Matter Most to Social Science and Policy
* **Date of publication**: 2019
* **Journal**: Annual Review of Criminology
* **Volume**: 2
* **Issue**: 1
* **Pages**: 123-145
* **URL**: [https://doi.org/10.1146/annurev-criminol-011518-024838](https://doi.org/10.1146/annurev-criminol-011518-024838)
* **Tags**: #causal_inference, #comps_exam
* **PDF Attachments**:
  * [naginRealGoldStandard2019.pdf](zotero://open-pdf/library/items/YDKNZKDW)

## Abstract

The randomized experiment has achieved the status of the gold standard for estimating causal effects in criminology and the other social sciences. Although causal identification is indeed important and observational data present numerous challenges to causal inference, we argue that conflating causality with the method used to identify it leads to a cognitive narrowing that diverts attention from what ultimately matters most—the difference between counterfactual worlds that emerge as a consequence of their being subjected to different treatment regimes applied to all eligible population members over a sustained period of time. To address this system-level and long-term challenge, we develop an analytic framework for integrating causality and policy inference that accepts the mandate of causal rigor but is conceptually rather than methodologically driven. We then apply our framework to two substantive areas that have generated high-visibility experimental research and that have considerable policy influence: (a) hot-spots policing and (b) the use of housing vouchers to reduce concentrated disadvantage and thereby crime. After reviewing the research in these two areas in light of our framework, we propose a research path forward and conclude with implications for the interplay of theory, data, and causal understanding in criminology and other social sciences.

## My notes

* The authors of this paper focus on two types of experiments:
  
	* Giving low-income and disadvantaged individuals housing vouchers.
	* Hot-spots policing (certain addresses experience an influx of police officers while others do not).
	  
* Estimating the causal impact of some treatment is not the same thing as asking **what would have happened had I done X**. Causal inference studies can help set expectations for what one might have observed had they acted differently. However, as Judea Pearl points out, counterfactual reasoning is the highest form of causal thinking and interventions are a rung below.
  
* Thus, it is two separate questions with two separate answers (and different methodologies and variables which would need to be considered):
  
	* What is the effect of increasing the police presence in certain hot spots compared to not
	* What if I had increased police presence at all hot spots?
	  
* The first question can be answered using the causal inference studies we all know well. The second question, though, depends on many other factors which causal inference studies cannot answer:
  
	* How would interference (or the diffusion of benefits/crime) scale? Would it become more likely or less likely if police targeted all hot spots? Would it the beneficial kind of interference suggesting our inferences are too conservative or the negative kind suggesting our inferences are too optimistic?
	  
	* Assuming policing resources were held constant, police would need to be pulled from other areas to police the hot spots. What would happen to crime in those areas?
	  
	* What would the long-term effects be (on crime)?
	  
* Similar problems crop up in the study of housing vouchers (see [[Moving to Opportunity]]):
  
	*  The counterfactual question (the policy question) here would be what if we offered housing vouchers to everyone?

	* The problem of interference again ([[Stable unit treatment value]]). Even in the original experiment, treatment subjects knew other people in the treatment suggesting there may have been a coordination in terms of where to move. It is unclear how the coordination would affect estimates of the outcomes (e.g., would it lead to more or less crime among the children?).
	  
		* Related point -> What if everyone moves to the same places recreating the cluster of neighborhood disadvantage originally observed?
		
	* How would people already living in the neighborhood react (e.g., out-migration of more advantaged residents? more restrictive zoning laws?)? How would the nature of the neighborhood change over time in ways relevant to the outcome? (e.g., how would it affect [[Collective efficacy|collective efficacy]]?).

I.e., policy makers are done a disservice by us telling them that our causal estimates represent realistic estimates of what would happen if we made changes system-wide. Policy makers might still adopt it on the basis that it looks promising which is fine. But how can research address these problems of jurisdiction-wide change, longer-term impacts, and system change?

Observational data, modeling ([[agent-based models]], statistical models based on estimating system-wide level impacts), substantive theory, quasi-experimental work will all be necessary.