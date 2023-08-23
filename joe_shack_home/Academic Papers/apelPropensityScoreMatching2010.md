---
type: [Chapter]
author: [Robert J. Apel, Gary Sweeten]
date: 2010
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Robert J. Apel, Gary Sweeten
* **Title**: Propensity Score Matching in Criminology and Criminal Justice
* **Date of publication**: 2010
* **Journal**: * **Volume**: * **Issue**: * **Pages**: 543-562
* **URL**: [https://doi.org/10.1007/978-0-387-77650-7_26](https://doi.org/10.1007/978-0-387-77650-7_26)
* **Tags**: #causal_inference, #comps_exam, #propensity_scores

## Abstract

The propensity score methodology has become quite common in applied research in the last 10 years, and criminology is no exception to this growing trend. It offers a potentially powerful way to estimate the treatment effect of some intervention on behavior when the receipt of treatment arises in a nonrandom way – this is the selection problem. It does so by creating synthetic “experimental” and “control” groups that are equivalent on a large number of potential confounding variables. In this chapter, we first introduce the counterfactual framework on which the propensity score method is based and define the average treatment effect. We then outline technical issues that must be addressed when the propensity score method is used in practice, including estimation of the propensity score, demonstration of covariate balance, and estimation of the treatment effect of interest. To provide a step-by-step example of the method, we appeal to the relationship between employment and substance use in adolescence. Following a brief review of research in criminology and related disciplines that employ the propensity score methodology, we offer a number of guidelines for use of the technique.

## My notes

* [[propensity score matching]] is used to help deal with [[selection bias]] or [[confounders]]. It tries to achieve *conditional ignorability* or conditional independence of the treatment status from the potential outcomes.
  
	* Propensity score matching is a more specific type of matching techniques in general which try to match individuals who are similar in important and relevant ways (important and relevant defined in relation to the independent variable or treatment and dependent variable of interest) **except** that one individual received the treatment while the other did not. It can be argued the only relevant difference between the two individuals is the treatment.
		* [[coarsened exact matching]] can become intractable as the list of measured characteristics grows larger.
		  
* One of the underlying problems propensity score matching is trying to solve is that of [[balance]] or ensuring treated individuals are statistically equivalent, in expectation, to untreated individuals on all relevant background factors. To the extent that balance is achieved, the treatment is said to be [[exogenous]] or ignorable -> treatment assignment is independent of potential outcomes.
	* Selection is when treatment is not ignorable or it is subject to [[endogeneity]].
	  
* Propensity score is defined as the conditional probability of assignment to treatment given a vector of observed variables. The conditional distribution of the variables is the same for treated and untreated individuals.

	1. Estimate the propensity score -> open question as to which variables should be chosen (theoretically chosen or kitchen sink approaches). Authors argue that whatever approach you use, you must convincingly argue all nonrandom sources of selection into treatment are fully captured by the model (regardless of if you include it in your model or not). You can use any modeling approach you wish really.
	   
		1. Then you must demonstrate [[common support]] or that there is overlap in the distribution of propensity scores between untreated and treated individuals. It is only in those parts of the distribution where treated and untreated overlap that a comparison can happen.
			1. Useful analysis because it reveals those situations in which individuals receive and do not receive treatment.
			   
		2. Make use of something called a [[caliper]] or a bandwidth (subject to discretion) which is how far away a potential match can be on the propensity score metric and still be useful as a counterfactual.
	   
	2. Conditional independence assumption must be evaluated by demonstrating balance on potential confounders. Can assess balance in a variety of ways:
	   
		1. Stratify the sample into equally-sized bins based on propensity score and use something like a [[t-test in the difference of means]] to demonstrate equivalence or not on certain key independent variables.
		   
		2. Can estimate the [[standardized bias]] (which is the difference in means divided by the sum of the variances squared (related to [[Cohen's d measure of effect size]])) before and after matching.
	   
	3. The treatment effect of interest ([[ATE]], [[treatment effect on the treated|ATT]], or [[ATU]]) is estimated.
	   
		1. Can estimate using a regression model where you include the treatment status as an independent variable, and its estimated coefficient is the ATE. You include the propensity score variable as a control.
		   
		2. Can use stratification. You divide the sample into equally-sized bins based on propensity score, and then you find the weighted average of the ATE in each bin, and then you calculate the grand weighted average overall.
		   
		3. Can use matching. You match individuals on the basis of propensity score (one individual was treated while the other was not) and calculate the average treatment effect this way. You may also match one treated individual to many untreated individuals wherein untreated individuals are weighted (higher weight given to better matches where very poorly matched individuals are given 0).
		   
			1. Simplest form of matching is [[nearest neighbor matching]].The untreated case with the closest propensity score is matched to a treated case known as one-to-one matching. You can also do many-to-one matching in which a treated individual is matched to many untreated individuals with weights evenly divided among all untreated individuals. There is a whole cottage industry it seems of how to achieve proper matches.
			   
			2. You can also use [[kernel matching]]. You decide upon a kernel function and a bandwidth (Gaussian, uniform, etc.). All matches within the bandwidth are then given a weight on the basis of the distribution used -> unlike with nearest neighbor matching where the number of matches is set beforehand and matches are thrown away so to speak, kernel matching uses all available matches in the bandwidth. 

Their empirical example demonstrates that the causal effect of employment on substance use among youth is not statistically significantly different from 0. The correlation between employment and substance use is spurious. There is some third factor (or set of factors) inducing youth to work and use drugs.
* This is different from what is estimated using regression-based approaches because they fail to conduct a proper apples-to-apples comparison.