---
type: [Article]
author: [Charles E. Loeffler]
journal: [Criminology]
date: 2013
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Charles E. Loeffler
* **Title**: Does Imprisonment Alter the Life Course? Evidence on Crime and Employment from a Natural Experiment
* **Date of publication**: 2013
* **Journal**: Criminology
* **Volume**: 51
* **Issue**: 1
* **Pages**: 137-166
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9125.12000](https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9125.12000)
* **Tags**: #comps_exam, #criminology, #theory_advancement, #life_course
* **PDF Attachments**:
  * [loefflerDoesImprisonmentAlter2013.pdf](zotero://open-pdf/library/items/BI38PXMI)

## Abstract

Ex-prisoners consistently manifest high rates of criminal recidivism and unemployment. Existing explanations for these poor outcomes emphasize the stigmatizing effects of imprisonment on prisoners seeking post-release employment as well as the deleterious effects of imprisonment on prisoners’ attitudes and capabilities. However, these explanations must be distinguished from selection effects in the criminal sentencing process which also could explain some or all of these poor outcomes. To distinguish between criminogenic and selection explanations for ex-prisoners’ post-release experience, I analyze data from a natural experiment in which criminal cases were assigned randomly to judges with sizable sentencing disparities. Using these exogenous sentencing disparities, I produce unbiased estimates of the causal effects of imprisonment on the life course. The results of this analysis suggest that selection effects could be sufficiently large to account for prisoners’ poor postrelease outcomes because judges with large sentencing disparities in their use of imprisonment had similarly high caseload unemployment and criminal recidivism rates.

## My notes

### Introduction and research question

"However, despite this high level of research interest, no clear consensus has emerged on the magnitude of imprisonment's effects on the life course." #quote #highlight

Not enough studies with measures of both employment and recidivism.

Very hard to construct policy relevant counterfactual comparison groups for the imprisoned.

Use a natural experiment in which the cases were randomly assigned to judges with different sentencing propensities -> free from issues of [[selection bias]] and also able to examine effects on recidivism and employment.

### Theories of imprisonment effects

* Imprisonment itself delays an individual's development and leaves them ill equipped to re-enter conventional society.
  
* Imprisonment stigmatizes ex-prisoners and limits their ability to participate productively in society.
  
* Social selection accounts for most, if not all, of the diminished life-course outcomes of ex-prisoners. Imprisoned are more likely to be unemployed and rearrested as a result of preexisting attributes and life experiences which imprisonment does little to improve or worsen. Imprisonment collects individuals who share significant disadvantage, temporarily houses them together, and then releases back into society relatively the same off (prisons being more or less extensions of an individual's neighborhood).
  
	* Most individuals experiencing imprisonment for the first time have already experienced multiple criminal justice system interactions. High rates of recidivism and low rates of employment may reflect the cumulative disadvantage already experienced by the now imprisoned. Imprisonment may not add much to this already sizable disadvantage.

### Data and methods

* Chicago court system. Once a case is sent to the Court, case assignment is entered into a computer program which purportedly assigns cases randomly to available judges.
  
* Look at a sample of felony cases (N = 20,297) from 2000 to 2003.
  
* **Dependent variable**:
	* Recidivism -> Time to rearrest for a new felony crime.
	* Employment -> Presence or absence of nonzero, positive earnings in the 20th quarter (5th year) after initial indictment.
	  
* **Independent variables**:
	* Demographic.
	* Criminal history.
	* Employed in the year prior to indictment.
	* **Imprisonment** -> any court-ordered sentence to imprisonment following a felony conviction (as opposed to being assigned to probation).
		* Pretrial detention was not included in this measure.
		  
* Judge assignment is an [[instrumental variable|Instrumental variable]].
	* It only affects defendant outcomes through the mechanism of the sentencing decision.
	* Disparities in sentencing between judges seems to arise from differences in their judgment on fundamentally similar cases vs. having a different caseload composition.

### Results

* Figures 2a and 2b visually and descriptively indicate that imprisonment and recidivism/employment do not appear to be correlated.

* Use [[OLS]] or [[linear probability models]]. [[probit]] regression models were used as robustness checks.
  
* Then they do instrumental variable 2 stage least squares regression and compare to their naive estimates from OLS.
  
* **Table 2**:
	* OLS estimates indicates a positive relationship between being imprisoned and recidivism.
	* Instrumental variable regression finds no significant correlation, though.

* **Table 3**
	* Similar results from as Table 3 except now the outcome is employment.

* **Supplemental results**
	* What if we re-estimate the equations only among first-time prisoners? Results are largely the same.

* Important to remember the counterfactual here is a similarly situated defendant who was randomly assigned to not get imprisonment. So for those individuals on the margin or already in a position where they could be incarcerated, incarceration does not seem to add much to any preexisting disadvantage in their life.
	* Previous observational studies have used different counterfactuals, namely comparing ex-prisoners to individuals with none or minimal prior criminal justice involvement. These estimates are useful for understanding the cumulative effects of criminal justice involvement, but it is not useful for understanding how those individuals most at risk for imprisonment would fare if they were alternatively punished (i.e., not imprisoned).
	  
* Why is this important to accurately estimate these effects and distinguish between the competing theories?
	* Theory 1 -> life-course imprisonment theories suggest there needs to be a substantial reinvention of correctional policy away from prison usage.
	* Theory 2 -> stigmatization theories suggest the harmful effects of imprisonment would be diminished by limiting people's access to their criminal history as well as by not excluding ex-prisoners from fully reintegrating back into conventional society.
	* Theory 3 -> Selection theories argue that early in the life-course interventions are more important to disrupt the formation of cumulative and chronic disadvantage.

* Limitations:
	* Stronger instruments and larger samples.
	* Exogenous variation was limited to lesser felonies and relatively short spells of imprisonment.
	* Almost everyone experienced pretrial incarceration which complicates the findings -> likely inducing adverse consequences for everyone.