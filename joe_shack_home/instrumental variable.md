---
type: Note
aliases: [Instrumental variable]
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #causal_inference #methodology 

## Assumptions

* **Relevance condition**: Instrument has to induce a change in the endogenous independent variable of interest and this change has to translate into a sufficiently strong correlation between them.
	* In terms of #random_judges , this means judges have to have sufficiently different sentencing dispositions.
	
* **Exogeneity condition**: Changes in the instrumental variable should be uncorrelated with prior trends in the dependent variable. I.e., it should be the case that the values that the instrument takes on are quasi-randomly assigned (conditional on other variables in the model).
	* In terms of random judges, this means defendants should be randomly assigned to judges.
	
* **Exclusion restriction**: The instrument can only affect the dependent variable through the main independent variable.
	* Judges only affect the defendants likelihood of recidivating through the punishment decision (incarcerate or not).

* [[Stable unit treatment value]]
	* The treatment assignment of one individual does not affect the outcomes of another individual.
	  
	* The treatment is sufficiently well-defined i.e., in expectation treatment effects should be constant across sample members. If not, the treatment may not be well defined enough.
	  
		* If a judge sentences someone to prison, that should not affect whether or not somebody else recidivates or not.
		  
		* If a judge sentences someone to prison, the type of prison or which prison someone gets sent to should not, in expectation, affect outcomes.

* You will be estimating the [[Local Average Treatment Effect]] or LATE since the causal estimate is only estimated for the subset of observations for which the instrument induces a change in the independent variable.

* Typically estimated using [[two stage least-squares regression]] or 2SLS regression. 
	* First, a regression model is estimated where the endogenous variable is the dependent variable, and the IV is the independent variable.
	* This estimated amount of exogenous variation is then used to estimate the causal effect of the endogenous variable (original independent variable of interest which is potentially subject to confounding bias) on the original dependent variable of interest in the second equation.

## Related papers

* [[sharkeyCommunityCrimeDecline2017]]
* [[loefflerDoesImprisonmentAlter2013]]
* [[greenUsingRandomJudge2010]]
* [[sampsonPoisonedDevelopmentAssessing2018]]