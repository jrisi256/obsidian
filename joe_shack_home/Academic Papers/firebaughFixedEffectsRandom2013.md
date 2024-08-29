---
type:
  - Chapter
author:
  - Glenn Firebaugh
  - Cody Warner
  - Michael Massoglia
year: 2013
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Glenn Firebaugh, Cody Warner, Michael Massoglia
* **Title**: Fixed Effects, Random Effects, and Hybrid Models for Causal Analysis
* **Date of publication**: 2013
* **Journal**: * **Volume**: * **Issue**: * **Pages**: 113-132
* **URL**: [https://doi.org/10.1007/978-94-007-6094-3_7](https://doi.org/10.1007/978-94-007-6094-3_7)
* **Tags**: #comps_exam, #multilevel_modeling
* **PDF Attachments**:
  * [firebaughFixedEffectsRandom2013.pdf](zotero://open-pdf/library/items/TWXAPTWF)

## Abstract

Longitudinal data are becoming increasingly common in social science research. In this chapter, we discuss methods for exploiting the features of longitudinal data to study causal effects. The methods we discuss are broadly termed fixed effects and random effects models. We begin by discussing some of the advantages of fixed effects models over traditional regression approaches and then present a basic notation for the fixed effects model. This notation serves also as a baseline for introducing the random effects model, a common alternative to the fixed effects approach. After comparing fixed effects and random effects models – paying particular attention to their underlying assumptions – we describe hybrid models that combine attractive features of each. To provide a deeper understanding of these models, and to help researchers determine the most appropriate approach to use when analyzing longitudinal data, we provide three empirical examples. We also briefly discuss several extensions of fixed/random effects models. We conclude by suggesting additional literature that readers may find helpful.

## My notes

### Benefits of [[fixed effects]] modeling

* Fixed effects modeling can eliminate the effects of confounding variables without measuring them or even knowing what they are exactly.

### Fixed effects model notation

* $Y_{i} = \alpha + \beta X_{i} + \beta^* X^*_i + \epsilon_i$
* The $X_i$ vector represents measured variables while $X^*_i$ represents all unmeasured variables.
* The general strategy is try to shrink $X^*_i$ by as much as possible by including as many relevant variables as possible.
* Fixed effects (when used with longitudinal data) can help alleviate the effect of unmeasured, unchanging (over time) variables.
* $Y_{it} = \alpha_t + \beta X_{it} + \beta^* X^*_{i} + \beta^{**} X^{**}_{it} + \epsilon_{it}$ -> we modified our equation to include a subscript for time. Notice how we model different intercepts for each point in time as well.
	* Notice how we subdivided our unmeasured variables into those variables which change over time ($X^{**}_{it}$) and those unmeasured variables which do not change over time ($X^*_i$) known as time invariant causes.
* $Y_{it} = \alpha_t + \beta X_{it} + u_{i} + \epsilon_{it}$ -> If we assume all unmeasured causes do not change over time, then our unobserved time-varying variable set is empty. We replace our unobserved time-invariant variables with $u_i$ which is a constant for each individual. This model becomes the canonical two-way fixed effects model (allows for time-specific and unit-specific effects).

#### Limitations

* Fixed-effects modeling essentially has individuals serve as their own control. Coefficients are interpreted as within-unit changes.
* Fixed-effects models remove the effects of all time-invariant causes (unmeasured **and** measured), the standard fixed effects model is unable to estimate the effects of time-invariant measured causes.
* By focusing only on within-unit variance, the statistical power of fixed effects models is greatly reduced.

### [[Random effects]] model

* $Y_{it} = \alpha_t + u_{i} + \beta X_{it} + \epsilon_{it}$ -> start with the canonical fixed effects model.
  
* Random effects models treat $u_i$ as a random variable. Fixed effects models treat $u_i$ as a fixed constant and omits all between-person variance. Random effects models treat $u_i$ as the composite effect of unmeasured traits which vary across individuals -> $u_i$ is a random variable drawn from $u$ with fixed variance which can be estimated from the data.
	* Usually assumes $u$ has zero mean, constant variance, and is independent of $X$ and $\epsilon_{it}$.
	* Random effects assumes each individual represents a random pull from some distribution with some mean value plus a random error.
	* Random effects estimation does not discard variation across individual units -> more efficient estimates and can measure the effects of variables which do not vary over time.

#### Limitations

* Random effects models assume time-invariant individual differences are drawn from a random variable $u$. The effects of time-invariant causes are not removed, and the model assumes unmeasured causes in $u_i$ are uncorrelated with measured causes. If there is a correlation, the results are likely subject to [[omitted variable bias]].

### Hybrid Model

* Fixed effects models can be estimated by centering each unit around its mean (random effects models can be estimated in a similar manner).
  
* Centered random effects models eliminate the effects of unmeasured time-invariant causes.
  
* We include within and between person variation in the time-varying predictors as separate predictors. The within component are group-centered means and the between-person variation is captured as grand-centered means.
  
* The regression coefficients for the within-person components will be identical to the coefficients in the standard fixed effects model. At the same time, the model can estimate the effects of time invariant variables as well.
  
	* Additionally, by permitting random intercepts for each person, the hybrid model gives estimates of between-person effects. The between-person coefficients can be compared with the within-person coefficients to test whether the person specific effects ($u_i$) are independent of time-varying variables. If they are, the assumptions of random effects model hold.
	  
* Some people instead employ a [[Hausman Test]] which compares an estimator known to be consistent when unobserved person-specific differences are time-invariant (fixed effects estimator) with an estimator that is efficient under the null hypothesis that those unobserved differences across persons are uncorrelated with the predictor variables (random effects estimator). the Hausman Test compares results from the fixed and random effects models to determine if there is sufficient evidence to reject the null hypothesis that the unobserved person-specific differences are uncorrelated to the other variables in the model.

### Categorical Dependent Variables

* The options for subject-specific fixed effects are limited when the dependent variable is categorical. One possibility is [[conditional logistic regression]] -> in effect limiting the sample to those individuals who change on the response variable over the period of observation. This leads to two sources of information loss though (and loss of precision) -> only consider within-unit change and exclude units which do not vary in the dependent variable.

### Count dependent variables

Fixed effects and hybrid models are available for panel data using [[Poisson regression]] and [[negative binomial regression]]. 