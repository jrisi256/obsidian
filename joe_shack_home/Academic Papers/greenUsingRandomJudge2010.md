---
type: [Article]
author: [Donald P. Green, Daniel Winik]
journal: [Criminology]
date: 2010
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Donald P. Green, Daniel Winik
* **Title**: Using Random Judge Assignments to Estimate the Effects of Incarceration and Probation on Recidivism Among Drug Offenders*
* **Date of publication**: 2010
* **Journal**: Criminology
* **Volume**: 48
* **Issue**: 2
* **Pages**: 357-387
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1745-9125.2010.00189.x](https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1745-9125.2010.00189.x)
* **Tags**: #comps_exam, #recidivism #random_judges 
* **PDF Attachments**:
  * [greenUsingRandomJudge2010.pdf](zotero://open-pdf/library/items/MWKA8S58)

## Abstract

Most prior studies of recidivism have used observational data to estimate the causal effect of imprisonment or probation on the probability that a convicted individual is rearrested after release. Few studies have taken advantage of the fact that, in some jurisdictions, defendants are assigned randomly to judges who vary in sentencing tendencies. This study investigates whether defendants who are assigned randomly to more punitive judges have different recidivism probabilities than defendants who are assigned to relatively lenient judges. We track 1,003 defendants charged with drug-related offenses who were assigned randomly to nine judicial calendars between June 1, 2002 and May 9, 2003. Judges on these calendars meted out sentences that varied substantially in terms of prison and probation time. We tracked defendants using court records across a 4-year period after the disposition of their cases to determine whether they subsequently were rearrested. Our results indicate that randomly assigned variations in prison and probation time have no detectable effect on rates of rearrest. The findings suggest that, at least among those facing drug-related charges, incarceration and supervision seem not to deter subsequent criminal behavior.

## My notes

### Research Question

Are defendants who are incarcerated (as designated by being assigned to a more punitive judge) versus those who are let off on probation (as designated by being assigned to a more lenient judge) recidivate more, less, or the same amount?

### Data and Methods

* Focused on felony drug offenders (and no non-drug related offenses) who appeared before the DC Superior Court between June 2002 and May 2003. N = 1,003.
	* Charges mostly related to distribution.

* Recidivism (1/0) -> Arrests which occurred after the disposition date in Maryland within 4 years after disposition for any charge.
  
	* Why not start the clock at release? Because the authors wanted to preserve symmetry between defendants. In expectation, defendants are identical except for the punishment received. Starting the clock at release would confound the effects of age (you are older when you are released) with incarceration (and also discount the [[Incapacitation effect]]).
	  
		* Of course, this also makes it harder to distinguish between [[Specific deterrence]] and incapacitation. The authors argue, though, many defendants who were incarcerated still had a large chunk of time which they could recidivate under.
		
* Other independent variables:
	* Need them to verify random assignment of judges conditional on observed variables.
	* They can help improve precision by reducing unexplained variation.
	* Age (age squared) (calculated as year of arrest minus year of birth), race (Black or not), gender, criminal history (series of dummy variables), current offense.
	* These variables do not have causal interpretations.

* Statistical model: Use judge assignment as an [[instrumental variable]] which affects a defendant's likelihood of recidivating only through the punishment decision.
### Results

#### Are cases randomly assigned?

Using [[multinomial]] regression modeling, the authors found no statistically significant relationship between case characteristics and date of assignment.

#### Is there sufficient variation in judge's sentences?

The authors argue that calendar assignment (when different judges are working) were significant predictors of sentence length as well as likelihood of getting sentenced to probation. It seems like the results remained significant even when including case characteristics.

#### Is the exclusion restriction satisfied?

Cannot be proven with data but seems so, logically.

#### Is the [[Stable unit treatment value]] assumption satisfied?

Cannot be proven with data but also seems satisfied. At least, it seems satisfied that one's treatment status does not affect any one else's likelihood of recidivating.

* #question -> This could be true. However, if defendants know each other, and one of them gets locked up, it is conceivable that this could affect the other non-locked up defendant's probability of recidivating. Authors do not really address this.

#### Effects

In no model specification does incarceration (or probation) have statistically significant causal effects on the likelihood of recidivating.

Both causal estimates, though, are positive with the causal estimates for probation being much lower.

Results are interpreted as each extra month of (incarceration or probation) increases the expected odds of recidivating by... X amount.

Estimates suggest that the average sentence length of those sentenced (16.5 months) causes a 14 percentage point increase in the likelihood of recidivism.

The average probation sentence among those who receive one (23.7 months) causes a 7.1 percentage point increase in the likelihood of recidivism.

The median defendant who experiences incarceration and probation is expected to recidivate at approximately the same rate as a defendant released without any punishment or supervision.

#### [[OLS]] estimates

OLS regression models report a statistically significant negative effect for incarceration. Probation has non-significant effects.

OLS could be biased in that longer sentences are being given out to defendants least likely to recidivate.

Instrumental variable could be biased. The random judge assignment could be a [[weak instrument]]. Weak in the sense they explain very little variance in the independent variables of interest. They have some evidence to suggest they have a weak instrument so they restrict their instrument by including only the most punitive judges and obtain similar results.

They also tried different definitions of recidivism. Results replicated.

Subset the sample by those who were being incarcerated for the first time. Results replicated.

#### Distinguishing deterrence from incapacitation

Use a [[statistical simulation]]. They simulate how defendants would have behaved if they were not incarcerated. Start with the release date of each defendant. They estimate the hazard rate of recidivism as a function of time and their other independent variables using [[hazard models]]. They then extend their predictions to a 4-year window.

They then replace these estimates of recidivism with the real rates of recidivism to calculate the specific deterrent effect of prison or the effect of prison on recidivism net of incapacitation. They find marginally significant positive results. Thus after controlling for incapacitation, it appears plausible that incarceration actually has criminogenic effects.

### Conclusions

* Incarceration has little net effect on the likelihood of recidivism (does not deter).
* Probation also has little net effect on the likelihood of recidivism.
* These effects might conceal countervailing forces.
	* In the case of prison, incapacitation vs. labeling.
	* In the case of probation, deterrence vs. increasing supervision:
		* Leads to a higher probability of getting caught even if it does not change the underlying probability of committing another deviant act.
		* Leads to a higher probability of breaking the law because there are now more rules to follow.
		* It might actually be criminogenic -> defiance. See [[shermanDefianceDeterrenceIrrelevance1993]].
