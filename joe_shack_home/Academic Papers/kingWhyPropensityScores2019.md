---
type:
  - Article
author:
  - Gary King
  - Richard Nielsen
journal:
  - Political Analysis
year: 2019
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Gary King, Richard Nielsen
* **Title**: Why Propensity Scores Should Not Be Used for Matching
* **Date of publication**: 2019
* **Journal**: Political Analysis
* **Volume**: 27
* **Issue**: 4
* **Pages**: 435-454
* **URL**: * **Tags**: #causal_inference, #comps_exam, #propensity_scores
* **PDF Attachments**:
  * [kingWhyPropensityScores2019.pdf](zotero://open-pdf/library/items/SAF68JSN)

## Abstract

We show that [[propensity score matching]] (PSM), an enormously popular method of preprocessing data for causal inference, often accomplishes the opposite of its intended goal—thus increasing imbalance, inefficiency, model dependence, and bias. The weakness of PSM comes from its attempts to approximate a completely randomized experiment, rather than, as with other matching methods, a more efficient fully blocked randomized experiment. PSM is thus uniquely blind to the often large portion of imbalance that can be eliminated by approximating full blocking with other matching methods. Moreover, in data balanced enough to approximate complete randomization, either to begin with or after pruning some observations, PSM approximates random matching which, we show, increases imbalance even relative to the original data. Although these results suggest researchers replace PSM with one of the other available matching methods, propensity scores have other productive uses.

## My notes

* [See this video for Gary King's explanation of the paper](https://www.youtube.com/watch?v=rBv39pK1iEs).
  
* [See here for a rejoinder to this paper](https://www.journals.uchicago.edu/doi/full/10.1086/711393).
  
	* The critique basically boils down to the fact that the critique of PSM is more theoretical and that the careful application and comparison of matching techniques with an awareness of the assumptions being made is the best approach.
	  
	* I do not know how I feel about this, though. The arguments are compelling from this paper.
	  
* [[arceneauxCautionaryNoteUse2010]] -> The problems with matching, in general, and how important it is for one to understand their data and the degree to which omitted variables can endanger one's results. This paper in particular stresses the need for calculating how sensitive one's matched results are i.e., how much does omitted variable bias threaten one's results? Even after controlling for everything, how much can unexplained variation account for the treatment effect?
  
	* In the paper, they assume the treatment had no effect, and instead all the observed effect attributed to the treatment comes from omitted variables, and thus how large does the effect of the unexplained variables have to be to account for the treatment effect observed.
	  
	* One can also conduct placebo tests i.e., how well does the treatment affect outcomes before the treatment was administered? If you find the treatment predicts pre-treatment outcomes relatively well, you probably have an [[omitted variable bias]] problem.
### High-level overview

* Propensity scores as commonly used increase imbalance, inefficiency, model dependence, and statistical bias. The more balanced the data becomes through pruning observations, the more likely PSM will degrade inference.
  
	* The more one's data is already balanced, the more likely it is that PSM will harm your inferences.
	* The more imbalanced one's data is, the more likely it is PSM can help, but if your data is very imbalanced, your ability to estimate a causal effect is likely suspect to begin with.
  
* PSM is still useful for regression adjustment, inverse weighting, and stratification, but they are not useful for matching.
  
* Other matching techniques like [[coarsened exact matching]] are still useful. 

### Model dependence in causal inference

* Identifying the appropriate model for estimating the causal effect is quite hard. What variables should I include? What modeling techniques should I use?
  
	* Model dependence is when small changes in the model specification lead to big changes in the substantive results.

	* "... the point of research is to discover the data generation process rather than to plausibly invent one. When our knowledge of the data generation process is limited, it makes little sense to use a model as if it were known." #quote Researchers are demonstrating *plausible model specifications* even when they can vary by quite a bit in their matching estimator estimates! Which model specification is correct, though?
	
* Good matching procedures can reduce model dependence. The goal of any matching procedure is to find a subset of the data which best approximates exact matching (prune those cases which do not have a match so to speak). Deviations from exact matches are categorized by the degree of [[balance|imbalance]]. One popular way of measuring imbalance is the average distance of each treated unit to its closest counterpart in the control unit.

	* Lower levels of imbalance bounds model dependence in estimating the [[ATE]].
	* Essentially, matching finds a treated individual and then another individual to serve as a plausible counterfactual.
	* Good matching is like finding a fully blocked experiment whereas PSM is like finding a completely randomized experiment which can be problematic as described below.
		* If non-PSM matching techniques can recover the experiment of their choice, they should almost always be better than PSM.

### Problem with propensity scores

The authors claim the problem is analogous to the problem of [[completely randomized experiments]] vs. [[fully blocked randomized experiments]].

* [See here for a very simple illustration demonstrating the difference between the two](https://quantifyinghealth.com/randomized-block-design-vs-completely-randomized-design/).
* In short, the difference is that fully blocked experiments can better control for systematic error or unlucky dice rolls in a completely randomized experiment (e.g., too many men in the treatment).

Matching techniques like CEM are like fully blocked experiments whereas PSM is more like a completely randomized experiment and has a much higher potential for imbalance to occur. What does this mean in plain English?

If you take two individuals with identical propensity score values (but different treatment statuses), they will not have identical covariates. In expectation, the distribution should be the same between treatment and control groups, though. So PSM attempts to reconstruct a completely randomized experiment where covariates are balanced on average whereas other matching approaches mimic a blocked experiment which give more precise treatment effect estimates and are less sensitive to model specification (because they attempt to find matches who actually match and do not just match in expectation).

### PSM Paradox

When you have a very balanced dataset (e.g., every observation has the same propensity score), you essentially have to prune at random which observations to compare. As the authors point out, this is one of the fundamental problems of PSM. The degree to which your dataset is already balanced, that is the degree to which PSM will not be useful.

* Furthermore, in expectation, the units will be same but you will not enjoy the full benefits as you would if the units were exact matches.
  
* This random pruning also only serves to increase imbalance -> but this occurs when PSM best approximates a random experiment (when all observations have similar propensity scores):
	* E.g., imagine you had a perfectly balanced dataset on sex between male and female. Purposeful pruning through some exact matching procedure (equivalent to a blocked design) will preserve the balance while randomly throwing out cases (equivalent to PSM or a fully randomized experiment) will increase imbalance.