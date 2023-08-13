---
type: [Article]
author: [Brian D. Johnson]
journal: [Criminology]
date: 2006
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Brian D. Johnson
* **Title**: The Multilevel Context of Criminal Sentencing: Integrating Judge- and County-Level Influences*
* **Date of publication**: 2006
* **Journal**: Criminology
* **Volume**: 44
* **Issue**: 2
* **Pages**: 259-298
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1745-9125.2006.00049.x](https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1745-9125.2006.00049.x)
* **Tags**: #comps_exam, #crim_597_sentencing, #sentencing_courts
* **PDF Attachments**:
  * [johnsonMultilevelContextCriminal2006.pdf](zotero://open-pdf/library/items/8F7AUBA2)

## Abstract

This study extends recent inquiries of contextual effects in sentencing by jointly examining the influence of judge and courtroom social contexts. It combines two recent years of individual sentencing data from the Pennsylvania Commission on Sentencing (PCS) with data on judicial background characteristics and county court social contexts. Three-level hierarchical models are estimated to investigate the influence of judge and county contexts on individual variations in sentencing. Results indicate that nontrivial sentencing variations are associated with both individual judge characteristics and county court contexts. Judicial background factors also condition the influence of individual offender characteristics in important ways. These and other findings are discussed in relation to contemporary theoretical perspectives on courtroom decision making that highlight the importance of both judge and court contexts in sentencing. The study concludes with suggestions for future research on contextual disparities in criminal sentencing.

## My notes

### Introduction

Jointly examines the influence of judge and courtroom social contexts. [[Multilevel modeling]] with three levels are used to investigate the influence of judge and county contexts on individual variations in sentencing. Sentencing variations are found to be associated with judge characteristics and county court contexts. Judicial background factors also condition the influence of individual offender characteristics in important ways.

Concerned from a social welfare perspective about disparity and concerned from a methodological level of [[omitted variable bias]] and [[model misspecification]]. Include more controls and properly consider the role of judges and their courtroom environments.

### Research Questions

1. To what extent does sentencing severity very significantly across both judges and county courts?
2. To what extent do the effects of individual-level sentencing factors also vary across judges and courts?
3. Minority judges will sentence more leniently than white judges.
4. Female judges will sentence more leniently than male judges.
5. Judges with heavier caseloads will sentence more leniently.
6. Judges with heavier violent caseloads will sentence more leniently (higher thresholds for what counts as serious crimes).
7. Small courts will sentence more severely than large courts.
8. Higher guidelines departure rates will result in more lenient sentencing outcomes (similar numbers of cases receive downward and upward departures). Lower guidelines compliance suggests a more flexible courtroom normative environment suggesting more leniency.
9. Available jail capacity will increase the likelihood of incarceration.
10. Minority judges will sentence minority offenders more leniently.
11. Male judges will sentence female offenders more leniently.
12. The effect of a violent crime will be greater for judges sentencing less violent crimes.

### Data and Method

PA Sentencing data, judicial background data, county-level courtroom data (both courtroom community characteristics and surrounding community-level social environment). 1999 - 2000. 80,000 cases, 303 judges, 67 counties/courtrooms. 

Uses 2-stage estimation with multilevel models. Judge-level factors may exert different influences on the decision to incarcerate vs. sentence length.

**Dependent variable** -> Incarcerated or not, sentencing length.

**Independent variables** -> Legal characteristics of the case, demographic characteristics of the defendant, also include the hazard rate (probability of being incarcerated) as an additional predictor of sentence length (results remain substantively the same with or without it), judge level characteristics (race, gender, caseload composition, caseload pressure, age, tenure, legal experience, marital and military status), court size, guideline departure rate, local jail capacity, percentage Hispanic, percentage unemployed, percentage Republican.

Why use multilevel models? Cases sentenced by the same judges in the same districts are likely to have certain similarities. This means residual errors are likely to be correlated within judges and within county-level courts violating fundamental error assumptions of [[OLS]] resulting in wrongly estimated standard errors.

“Misestimated standard errors occur within multilevel data when we fail to take into account the dependence among individual responses within the same organization…” #quote -> risks artificial inflation of statistical power (assuming results are more precise than they really are) by misspecifying the degrees of freedom truly available.

Multilevel models incorporate a unique random effect for each organizational unit. Allows for the modeling of heterogeneity of regression coefficients across units (e.g. the effect of being a minority offender might vary across judges) -> allows slopes and intercepts to vary across units.

### Results

- **Table 2**

	- 5% of variation in likelihood of incarceration is attributed to differences between judges.
	- 5% of the variation can also be accounted for by differences between counties.
	- For sentence length it’s 6% and 7% respectively.
    
- **Table 3** -> Individual-level effects are as anticipated with legal variables dominating the models but extralegal variables having some influence and indicating some disparity.
    
- **Table 4** -> Likelihood and length of incarceration vary across judges and courts even when accounting for individual-level sentencing factors. Likelihood of incarceration and sentence length is a factor of the judge hearing your case and the courthouse in which it’s being heard. The effects of virtually all explanatory factors vary significantly across judges and courts. Suggest judges weigh the importance of individual offense and offender characteristics differently and the influence varies across county courthouses.
    
	- Presumptive guideline recommendations vary in their influence on odds of incarceration suggesting they do not produce uniformity as intended.
    
	- Trial penalty also varies across judges and courthouses.
    
- **Table 5** -> After accounting for individual case and offender characteristics.
  
	- Minority judges were somewhat less punitive.
	- The effect of gender was minimal.
	- Older judges less likely to incarcerate and give shorter sentences.
	- Prior military experience exerted a positive influence on the odds of incarceration.
	- Tenure of the judge was only marginally associated with increased sentence severity.
	- Overall, caseload pressure exerted insignificant effects on likelihood and length of incarceration.
	- Caseload composition demonstrated small but significant effects. More property crimes ->. marginally more likely to incarcerate. Heavy violent and drug caseloads -> longer sentences. Small effects but have large cumulative effects.
	- Larger courts tended to be less punitive and smaller courts more punitive. However no statistically significant effects for large courts on incarceration. Footnote 13 -> more research needed.
	- Higher departure rates -> less likely to incarcerate.
	- More jail capacity -> more likely to incarcerate.
	- Communities with larger Hispanic populations were characterized by slightly longer sentences.
    
- **Table 6** -> Interactions.
    
	- No evidence for the gender of the judge interacting with the gender of the defendant or any overall meaningful effect for the gender of the judge.
    
	- Minority judges were less likely to incarcerate black and Hispanic offenders. Still a disparity but greatly reduced. Surprisingly minority judges sentenced black offenders to slightly longer terms of incarceration.
    
	- Effect of a violent conviction was significantly conditioned by the violent caseload of the sentencing judge for both outcomes. Judges who sentenced a higher proportion of violent crimes were less likely to incarcerate violent offenders and shorter sentences.
    
	- Combined influence of age, race, and gender is important on the sentencing habits of the judge. They become even more pronounced when courtroom contexts are considered.

![](https://lh5.googleusercontent.com/LNJ70s5B-SN-WsGjPHd8PsmVztGXlMuWi8f3v2l8ysPQJ9M6Wgn29XQyDiVLkamDaSx0TZ7eMfUFgcKI4iBMhLK7J3Cv9eo9FwEmQ96PvDGXJn-dyuGaCLLuoZMEWROsQoPvfhGpl3SJMkEDUAKN)