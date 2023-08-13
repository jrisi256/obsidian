---
type: Note
aliases: [Regression discontinuity]
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #causal_inference #methodology 

## Notes

### Related to the effects of incarceration

See [[loefflerImpactIncarcerationRecidivism2022]]

Assumptions:

* Assignment variable is ideally continuous and cannot be dichotomous.
  
* The discontinuity should be deterministic in the sense that people cannot game the system to get just above or below the cutoff.
  
* It will ideally be non-fuzzy in the sense that everyone above the cutoff gets the treatment (or the control) and everyone below the cutoff gets the control (or the treatment).
  
* If these conditions are met, cases just above and below the threshold should be balanced in expectation except for the treatment.

**Example** -> In a sentencing grid, an individual with three or more prior offenses receives a mandatory sentence of incarceration while individuals with two or less offenses receive non-incarceration sentences.

Allows for the estimation of a [[Local Average Treatment Effect]] -> only generalizes to those individuals just above and below the cutoff.