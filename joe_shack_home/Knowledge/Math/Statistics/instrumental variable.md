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

	* This can be a problem if an instrument is a *weak instrument* or it does not cause enough exogenous variation in the independent variable of interest -> will produce very large standard errors which, in some cases, might be worse than no instrumental variable. See [[bushwayInstrumentalVariablesCriminology2010]]. The analogy is you ran an experiment in which very few people complied with the treatment.
	  
	* This can be tested statistically and is usually demonstrated in the first-stage of the regression. 
	
* **Exogeneity condition**: Changes in the instrumental variable should be uncorrelated with prior trends in the dependent variable. I.e., it should be the case that the values that the instrument takes on are quasi-randomly assigned (conditional on other variables in the model).
  
	* In terms of random judges, this means defendants should be randomly assigned to judges.
	  
	* As mentioned, the assignment may be conditional i.e., conditional on these variables, the assignment to treatment is plausibly random.
	  
	* This has to be defended on substantive and theoretical grounds. 
	  
	* Other times, one way want to include other variables to make one's estimates more precise. In regression modeling, when *relevant* variables are included, the residual error is decreased and the effects of variables can then be more precisely estimated (because there is less unexplained variation).
	  
		* As a thought experiment, imagine you had a variable which perfectly explained/predicted an outcome variable. There would be no residual error and the estimated effect of the variable would be perfectly estimated with no imprecision.
		  
		* Now imagine a variable which poorly predicted an outcome. There would be a lot of unexplained variation, and the model would likely be unable to *precisely* estimate the effect of the variable. By adding more *relevant* (and *uncorrelated*) variables to reduce the unexplained variation, you would also be adding to the precision of the estimates of your coefficients. So if you added a 2nd variable which in conjunction with your poorly performing 1st variable, perfectly predicted the outcome, you would now have perfect precision in the estimates of your coefficients. 
	
* **Exclusion restriction**: The instrument can only affect the dependent variable through the main independent variable.  This, generally speaking, cannot be proven using quantitative data -> puts a premium on substantive and theoretical knowledge.
  
	* Judges only affect the defendants likelihood of recidivating through the punishment decision (incarcerate or not).
	  
	* Lots of controversy around the [[kirkResidentialChangeTurning2012]] paper if its exclusion restriction holds. 

* [[Stable unit treatment value]]
  
	* The treatment assignment of one individual does not affect the outcomes of another individual.
	  
	* The treatment is sufficiently well-defined i.e., in expectation treatment effects should be constant across sample members. If not, the treatment may not be well defined enough.
	  
		* If a judge sentences someone to prison, that should not affect whether or not somebody else recidivates or not.
		  
		* If a judge sentences someone to prison, the type of prison or which prison someone gets sent to should not, in expectation, affect outcomes.
	
* **Monotonicity Assumption**:
	* Slightly different meanings depending on the available treatments. In the simple example, imagine you have a dichotomous treatment procedure (treated or not treated) and a dichotomous exposure (received treatment, did not receive treatment). This creates the usual matrix of **compliers**, **deniers**, **always takers**, and **never takers**.
	  
		* Always takers and never takers do not have their exposure changed by the instrument (or by anything really).
		  
		* The monotonicity assumption (in this situation) boils down to the idea that there are no defiers in your population, and you are only estimating the causal effect among compliers or those who treatment status would be changed (in the predicted direction) by the instrument.
		
		* It can become more complicated the more complicated your treatment procedure becomes. See [[loefflerImpactIncarcerationRecidivism2022]] which has a different operationalization of the monotonicity assumption for [[judge instrumental variables]].

* You will be estimating the [[Local Average Treatment Effect]] or LATE since the causal estimate is only estimated for the subset of observations for which the instrument induces a change in the independent variable.

* Typically estimated using [[two stage least-squares regression]] or 2SLS regression. 
	* First, a regression model is estimated where the endogenous variable is the dependent variable, and the IV is the independent variable.
	* This estimated amount of exogenous variation is then used to estimate the causal effect of the endogenous variable (original independent variable of interest which is potentially subject to confounding bias) on the original dependent variable of interest in the second equation.

## Related papers

* [[sharkeyCommunityCrimeDecline2017]]
* [[loefflerDoesImprisonmentAlter2013]]
* [[greenUsingRandomJudge2010]]
* [[sampsonPoisonedDevelopmentAssessing2018]]