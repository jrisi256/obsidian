---
type: [Chapter]
author: [Shawn D. Bushway, Robert J. Apel]
journal: date: 2010
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Shawn D. Bushway, Robert J. Apel
* **Title**: Instrumental Variables in Criminology and Criminal Justice
* **Date of publication**: 2010
* **Journal**: * **Volume**: * **Issue**: * **Pages**: 595-612
* **URL**: [https://doi.org/10.1007/978-0-387-77650-7_29](https://doi.org/10.1007/978-0-387-77650-7_29)
* **Tags**: #causal_inference, #comps_exam, #instrumental_variable
* **PDF Attachments**:
  * [Bushway and Apel - 2010 - Instrumental Variables in Criminology and Criminal](zotero://open-pdf/library/items/G4EKWLNF)

## Abstract

[[instrumental variable]] estimation is an econometric technique that is commonly employed by economists to overcome the problem of [[endogeneity]] in a causal variable of interest. It is a method that could be of some use to criminologists who also confront [[simultaneity bias]], [[measurement error]], and [[selection bias]]. The method is sometimes referred to as a natural experiment because, like a classical experiment, it resolves these problems by rendering variation in the key independent variable exogenous or uncorrelated with the error term. It does so through the introduction of a variable that is correlated with the causal variable of interest but is otherwise uncorrelated with the outcome other than the one through the causal variable. This exclusion restriction is the key to causal identification and must be defended on substantive and theoretical grounds, not necessarily statistical ones. Following an intuitive description of the method, a short empirical example is provided, along with guidance about common pitfalls and potential problems with the method. Researchers interested in a more technical treatment of the method are pointed to accessible treatments in economics.

## My notes

Instrumental variables are useful for:

1. Estimating the [[Local Average Treatment Effect]] in experiments with noncompliance (as seen in [[angristInstrumentalVariablesMethods2006]]).
   
	1. Researchers often use treatment assignment as an instrumental variable for the treatment itself to estimate the LATE over and above the [[intend-to-treat]] or ITT effect.
   
2. Deals with endogenous independent variables and measurement error.
   
	1. It can create consistent estimates in the presence of [[omitted variable bias]]. Similar to the below, example, we can reason about if our results are being biased by omitted variable bias.
	   
	2. How can it help with measurement error? There is an example of this in [[bushwayExplicitTestPlea2014]]. When error is random (zero mean and uncorrelated with X), measurement error will always attenuate the main effect of X biasing it towards zero.
	   
		1. When we see a bigger X than is actually there (observe 5 when it is actually 3), we will think there has been more a change in X than there actually was, and we will underestimate the change that would occur if X truly did change by that larger amount.
		   
		2. Many times, though, the error will not behave well. It will be systematically different from the true value in which case it is harder to anticipate how it is affecting our estimates.
		   
		3. Take the relationship between crime and housing prices. Typical approaches found a null effect and in low-income neighborhoods they actually found a positive relationship. Crime can under-reported, and it may be most under-reported in low-income areas. The researchers used murder (best reported crime) as an instrument for all violent crime -> the predicted values of violent crime were then used to predict housing prices.
			1. Stated more plainly, the variation in violent crime correlated with murder negatively affects housing prices.
   
3. Instrumental variables can help with issues of simultaneity.
   
	1. E.g., police and crime. We would observe a positive correlation between the two because the two simultaneously determine each other. In reality, police tend to have a negative causal effect on crime. Estimates are likely biased upward (negative coefficient biased towards zero).
	   
		1. We can reason about these things about which direction we anticipate results to be in. E.g., unemployment and crime cause have positive causal effects on each other. Thus, we would expect a positive coefficient biased upwards -> bigger effect size than would be estimated properly -> if a weak relationship were then found, simultaneity would not theoretically be the reason why.

The basic idea of an instrumental variable is to make an independent variable uncorrelated with the error term thus making it exogenous.

* Instrumental variable identify the variation in the endogenous independent variable of interest that is truly exogenous and only uses that variation in estimation -> of course, this leads to less precision because there is now less variation in X.
