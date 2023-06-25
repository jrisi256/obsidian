---
type: Note
aliases: [Instrumental variable]
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #causal_inference #methodology 

## Assumptions

* **Relevance condition**: Instrument has to induce a change in the endogeneous independent variable of interest and this change has to translate into a sufficiently strong correlation between them.
* **Exogeneity condition**: Changes in the instrumental variable should be uncorrelated with prior trends in the dependent variable. I.e., it should be the case that the values that the instrument takes on are quasi-randomly assigned (conditional on other variables in the model).
* **Exclusion restriction**: The instrument can only affect the dependent variable through the main independent variable.
* You will be estimating the [[Local Average Treatment Effect]] or LATE since the causal estimate is only estimated for the subset of observations for which the instrument induces a change in the independent variable.

## Related papers

* [[sharkeyCommunityCrimeDecline2017]]