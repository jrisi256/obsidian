---
type:
  - Article
author:
  - Lawrence M. Berger
  - Sarah K. Bruch
  - Elizabeth I. Johnson
  - Sigrid James
  - David Rubin
journal:
  - Child Development
year: 2009
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Lawrence M. Berger, Sarah K. Bruch, Elizabeth I. Johnson, Sigrid James, David Rubin
* **Title**: Estimating the “Impact” of Out-of-Home Placement on Child Well-Being: Approaching the Problem of Selection Bias
* **Date of publication**: 2009
* **Journal**: Child Development
* **Volume**: 80
* **Issue**: 6
* **Pages**: 1856-1876
* **URL**: [https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2836492/](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2836492/)
* **Tags**: #causal_inference, #comps_exam, #soc513
* **PDF Attachments**:
  * [bergerEstimatingImpactOutofHome2009.pdf](zotero://open-pdf/library/items/IE4FSSRX)

## Abstract

This study used data on 2,453 children age 4 to 17 from the National Survey of Child and Adolescent Well-Being and 5 analytic methods that adjust for selection factors to estimate the impact of out-of-home placement on children's cognitive skills and behavior problems. Methods included ordinary least squares ([[OLS]]) regressions and residualized change, simple change, difference-in-difference, and fixed effects models. Models were estimated using the full sample and a matched sample generated by propensity scoring. Although results from the unmatched OLS and residualized change models suggested that out-of-home placement is associated with increased child behavior problems, estimates from models that more rigorously adjust for selection bias indicated that placement has little effect on children's cognitive skills or behavior problems.

## My notes

### What is the research question?

How can we adjust for selection bias when attempting to estimate the impacts of out-of-home placement?  

### Why is it important?

- CPS is an important social policy program, but its effects are little understood. It’s important to understand whether out-of-home placement mitigates or heightens developmental risks for children.
    
- We cannot run an experiment. So researchers have relied on 4 methods generally: 
	- Control for correlates (omitted variable bias).
	- Employ [[matching]] techniques (ensure appropriate overlap in the covariate distributions, however still subject to omitted variable bias).
	- Estimate change models (mainly longitudinal data or [[difference in differences]] approaches or [[fixed effects]], adjust pretty well for preexisting or unmeasured differences in children who are and aren’t removed from home).
	- Utilize an [[instrumental variable|Instrumental variable]].
	  
- Each has their own costs and benefits. This studies aims to clarify what the costs and benefits are in practice.
### How do you propose to answer it?

- Used 5 analytic methods to adjust for selection factors to estimate the impact of out-of-home placement on children’s cognitive skills and behavior problems: 
	- OLS.
	- Residualized change (includes a baseline measure of the dependent variable which would hopefully capture some of the effects of unobserved variables).
	- Simple change (estimate the difference in follow-up vs. baseline well-being scores).
	- Difference in difference (will be biased to the degree that unobserved factors differentially affects over time in well-being between treatment and control groups).
	- Fixed effects (expresses each variable as a deviation from a child’s mean value on that measure across time, should in theory remove all time-invariant and unobserved variables from the model → however if unobserved variables are time varying or if permanent characteristics have time varying effects, estimates will be biased).
    
- All models were estimated using the full sample and a matched sample using [[propensity score matching]].
    
- Novel dataset with larger amount of variables and more variance in area and children covered, and it has a longitudinal design.
    
- Out-of-home placement → primary predictor variable if a child was removed from home by CPS between his or her baseline and follow-up assessments. Dependent Variables: Cognitive skills and behavior problems. Various control variables.

### What did you find?

- OLS and residualized changes models suggest out-of-home placement is associated with increased child behavior problems. But estimates from models which more rigorously adjust for selection bias indicate placement has little effect on children’s cognitive skills or behavior problems.

- When using propensity score matching, found no significant results as to the effects of out-of-home placement.

- Limitations → Cannot claim causality but can claim suggestive evidence of causality.