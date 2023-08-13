---
type: [Article]
author: [Thomas A. Loughran, Ray Paternoster, Aaron Chalfin, Theodore Wilson]
journal: [Criminology]
date: 2016
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Thomas A. Loughran, Ray Paternoster, Aaron Chalfin, Theodore Wilson
* **Title**: Can Rational Choice Be Considered a General Theory of Crime? Evidence from Individual-Level Panel Data
* **Date of publication**: 2016
* **Journal**: Criminology
* **Volume**: 54
* **Issue**: 1
* **Pages**: 86-112
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9125.12097](https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9125.12097)
* **Tags**: #comps_exam, #deterrence_rational_choice, #theory_advancement
* **PDF Attachments**:
  * [loughranCanRationalChoice2016.pdf](zotero://open-pdf/library/items/9TNFMY4Q)

## Abstract

In the last few decades, rational choice theory has emerged as a bedrock theory in the fields of economics, sociology, psychology, and political science. Although rational choice theory has been available to criminologists for many years now, the field has not embraced it as other disciplines have. Moreover, rational choice scholars have fueled this skepticism of the theory's generality by modeling offender decision making that is one-sided—large on the costs of crime (sanction threats), short on the benefits of crime. In this article, we directly assess the generality of rational choice theory by examining a fully specified model in a population that is often presumed to be less rational—adolescents from lower socioeconomic families who commit both instrumental (property) and expressive crimes (violence/drugs). By using a panel of N = 1,354 individuals, we find that offending behavior is consistent with rational responses to changes in the perceived costs and benefits of crime even after eliminating fixed unobserved heterogeneity and other time-varying confounders, and these results are robust across different subgroups. The findings support our argument that rational choice theory is a general theory of crime.

## My notes

Expected utility = \[p * (utility - severity of sanctions if caught)] + \[(1 - p) * utility], where p = probability of detection, Y = utility, and f = severity of sanctions if caught.
* Crime will rise as the utility afforded to crimes rises.
* Crime will fall as the probability of detection increases and severity of sanctions increases.

### Prior research

* Negative relationship between crime and increases in police manpower which some argue result from increases in the probability of detection and thus represents evidence in favor of [[Deterrence theory|deterrence theory]].
  
* Argues previous research has found individuals respond on the basis of their own individual-level risk perceptions.

### Gaps in the literature

* Failed to demonstrate empirically that increase in p yield a greater reduction in offending than comparably measured increases in f.

* Failed to account for individual differences in risk preferences (some individuals prefer more or less risky options net of expected value) -> perhaps explain the importance of certainty over severity -> also explains why association of perceptions and offending (without considering risk preferences) are weakly correlated.
  
* Most studies have failed to account for simultaneity between severity and certainty.
  
* Most studies have not taken into account the full costs of crimes. They only account for fines and imprisonment but not the costs of informal sanctions like reputational harm.
  
* Most studies have not studied at all the benefits of crime. Specifically, the net benefit of crime (over and above the opportunity cost of time spent doing crime that could have been spent doing something else).
	* Some evidence suggestive of the fact that better legal opportunities is associated with less crime.
	* Need more holistic understandings of the benefit of crime aside from the monetary aspect -> fun, social benefits.

### Data & Methods

* Use individual panel-level data from a sample of juvenile and young adult serious offenders.
	* Observe individual-specific measures on multiple dimensions concerning the costs and rewards of crime as well as subjective beliefs concerning the probability of being caught.
	* Detailed self-reports of offending variety and frequency.
		* Test for heterogeneity in responsiveness to costs, risks, and rewards by type of offending behavior.
	* Panel data allows for the controlling of time invariant factors.
	* Test differential rational choice (e.g., economically disadvantaged offenders may be more or less responsive to changes in risks, costs, and benefits) on the basis of gender, race, and criminal propensity.
* Plan is to show how the rational choice model applies across a variety of domains even in populations that are thought to least rational (i.e., juveniles).

Data comes from the [[Pathways to Desistance]] study.

* **Self-reported offending** -> variety and frequency scores.
* **Perceived risk** -> At each observation period, individuals were asked how likely it is they would be caught for a variety of different crimes. Ranges from 0 to 10.
* **Perceived Personal Rewards** -> How much of a thrill is it to commit certain crimes? Ranges from 0 to 10.
* **Perceived Social Costs** -> If one were caught breaking the law, would... Lose respect of friends and family? Get suspended from school? 1 to 5.
* **Perceived Social Rewards** -> "If I beat someone up, people my age will respect me more..." ranges from 1 to 5.
* **Legal and Illegal Earnings** -> Asked how much money individuals earned from legal and illegal activities.

**Model**
* **Dependent variable** -> number of crimes of type J committed by an individual in a given time period.
* **Independent variables** -> perceived probability of apprehension, perceived severity, social rewards of crime, personal rewards of crime, time-varying control variables (age, proportion of time incapacitated, witness a family member's arrest, victim of a crime, part of a gang, pregnant or involved with someone who was pregnant).
* [[fixed effects]] for individual and time interacted with site (only 2 sites) using [[Poisson regression]]. [[Clustered standard errors]] on the individual. [[Standardized coefficients]].
	* Do not use [[negative binomial regression]]. Why? Even though there is evidence of [[overdispersion]].
	* Fixed effects estimates are not estimated consistently in nonlinear panel data. [[Incidental parameter bias]].
	* Parameter estimates will differ depending on whether one uses an unconditional or conditional [[maximum likelihood estimator]].
	* The MLE in Poisson regression is equivalent to a [[multinomial]] logistic regression which has identical parameter estimates for unconditional and conditional likelihood functions.
	* Second, robustness tests which estimate conditional fixed effects negative binomial models yield similar estimates to unconditional fixed effects Poisson regression models.

### Results

* **Table 1** -> <mark> Calculate within-respondent share of variation or how much each variable varies within (as opposed to between) individuals. </mark> #highlight 
* **Table 2**
	* Increases in certainty of apprehension decreases the expected count of crime and increases the legal share of earnings (estimated using [[OLS]]).
	* Severity has no relationship.
	* Increases in social rewards and personal rewards are associated with decreases in the expected count of crime and decreases in the legal share of earnings.
	* Omnibus tests suggest that the models have some predictive power suggesting offenders are somewhat responsive to risks, costs, and rewards.
	* Conduct a bunch of pairwise linear restriction statistical tests:
		* Offenders are more responsive to certainty than they are to severity.
* **Tables 3, 4, and 5**
	* Table 3 re-estimates the model for a variety of subgroups. Results are robust.
* **Table 6**
	* Different model specifications -> results are robust.