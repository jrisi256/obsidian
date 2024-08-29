---
type:
  - Article
author:
  - Shawn D. Bushway
  - Allison D. Redlich
  - Robert J. Norris
journal:
  - Criminology
year: 2014
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Shawn D. Bushway, Allison D. Redlich, Robert J. Norris
* **Title**: An Explicit Test of Plea Bargaining in the “Shadow of the Trial”
* **Date of publication**: 2014
* **Journal**: Criminology
* **Volume**: 52
* **Issue**: 4
* **Pages**: 723-754
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9125.12054](https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9125.12054)
* **Tags**: #comps_exam, #crim_597_sentencing, #crim501, #prosecutors, #sentencing_courts
* **PDF Attachments**:
  * [bushwayExplicitTestPlea2014.pdf](zotero://open-pdf/library/items/Y2SFZGU5)

## Abstract

Bargaining in the “[[shadow of the trial]],” which hinges on the expectations of trial outcomes, is the primary theory used by non-criminologists to explain variation in the plea discount given to defendants who plead guilty. This study develops a formal mathematical representation of the theory and then presents an empirical test of the theory using an innovative online survey with responses to a hypothetical case from 1,585 prosecutors, defense attorneys, and judges. The key outcomes are the probability that the defendant will be convicted at trial, the sentence for the defendant if convicted, and the best plea that the respondent would accept or offer. Variation in the outcomes is created through experimental variation in the information presented to the respondents. Structural regression models are estimated to fit the formal theoretical models, and the instrumental variables method is used to correct for measurement error in the estimate for probability of conviction. The data support the basic shadow model, with minor modifications, for only prosecutors and defense attorneys. Controlling for the characteristics of the individual actors and their jurisdictions adds explanatory value to the model, although these control variables did not affect the key coefficients from the shadow model.

## My notes

**Research Question**: Is the shadow of the trial perspective a reasonable model for understanding how plea bargains are constructed?

**What is the shadow of the trial perspective?** 3 variables

- Probability of conviction at trial (e.g. 0.7)
- Sentence length if convicted at a trial (e.g. 10 years)
- Value of a plea bargain (e.g. 7 years)

**Differences in the shadow of the trial perspective vs. traditional criminological perspective**:

- Is the plea value strictly a function of the expected trial sentence and probability of conviction regardless of how the expected trial sentence and probability of conviction are constructed?
    
- How do focal concerns and work group dynamics shape expected trial length and the probability of conviction which in turn affect the plea value (and subsequent plea discount)?
    
- Complementary in some ways but conflicting in others.

**Design**:

- Recruited lawyers and judges from a variety of organizations.
  
- They were presented with a hypothetical case and fact files.
  
- 16 test conditions: Eyewitness (present or absent) * Confession (present or absent) * DNA Match (present or absent) * Criminal History (Long or short).
  
- Asked to estimate: 1) Probability of conviction if the case went to trial, 2) Trial sentence if found guilty, 3) What would be the least severe sentence they’d offer as a plea deal?
  
- [[Structural equation modeling]] is used for estimating the system of equations the authors devised for determining the length of plea deals.

- Measurement Issue of Probability

	- There was clumping in the probability estimates. This could reflect reality, or it could reflect measurement error. This will bias the coefficient estimates.
	  
	- So the authors use an [[instrumental variable]] which can be used to create consistent estimates of the independent variable even with measurement error. A valid instrumental variable would be anything affecting a respondent's predicted probability of conviction (P) but is uncorrelated with the measurement error AND is only correlated with the dependent variable (the plea value) through P.
	  
		- Mechanically what happens is it works in two stages. You first estimate the independent variable through the IV (Z). They use DNA match, confession, and positive ID witness to model probability of conviction since they should not affect the average sentence.
		  
		- In the second stage the dependent variable is regressed using the predicted values of the independent variable. The coefficient in the second stage is identified only by the exogenous variation in the probability of conviction created by the instrumental variables, the result will be less susceptible to measurement bias
  
			- Instrumental variables can lead to a large loss of precision (since only a subset of your sample is likely to be affected by the instrument). Thus if the clumping reflects the actual preferences of respondents and does not reflect measurement error, the estimates from the instrumental variable should be similar if not significant.

**Results**:

- The authors claim the shadow model appears to be a reasonable model of how defense attorneys and prosecutors arrive at plea values.
    
- Judges appear to not subscribe so much to the shadow model. It appears as if they don’t really consider the probability of conviction at trial when considering an appropriate plea value. The authors term this as judges giving a fixed discount.
    
- The results hold when the authors add a series of control variables to their models (e.g. sex of respondent, race of respondent, age of respondent, etc.).

**Discussion Questions**:

1. The authors briefly mention in their paper there is the issue of external validity given their research design (hypothetical cases rather than real cases). In other words, how well would we expect these findings to generalize to other experiments but also to the real world? In particular, how do we think the characteristics of the defendant might change the findings? Note in the hypothetical case, the suspect was described as a white male in their twenties.
    
2. Methodological Question: The R2 values reported in table 5 (IV model) range from 0.59 (for judges) to 0.27 (for prosecutors). Do we think the authors should have focused more on contextualizing these values? Are these large enough values to suggest the probability of conviction and trial sentence length are enough to predict what the plea value will be?
    
3. How important do we think defendants are for this model? Different from question 1 which is asking how the characteristics of the defendant might change the nature of the plea deal - this question is asking do we think defendants will always heed the advice of their defense attorney? How often do they deviate from their advice and what would that say about how well the shadow model might predict their behavior? How could we get at this question, or is there any research which tries to address this question?
    
4. The conclusion of the article states that judges do not appear to act in accordance with the shadow model and rather that their behavior is most consistent with a fixed discount model, adding that judges are not often directly involved except in cases where a plea bargain is not reached and a probability of conviction near .5. What does this tell us about differences between prosecutors/defense attorneys and judges? Can we think of this group as having equal influence on bargaining?
    
5. Within the shadow model there exists the idea of the risk-neutral, risk-seeking, and risk-averse defendant. Do you agree with the author's decision to start with the assumption of the risk-neutral defendant? Do the findings point to this? What important considerations about risk should be included in the shadow model if adopted by criminologists?
    
6. In line with questions 1 and 3, the data is collected from a sample that is more than 70% white and over 90% male. Matched with the finding that male defense attorneys have acceptable plea amounts that are 18 percent lower than their female colleagues, do we think the shadow model is applicable to judges, defense attorneys, and prosecutors in the real world? What characteristics or knowledge of those who bargain might be useful?