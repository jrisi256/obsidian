---
type:
  - Chapter
author:
  - Richard A. Berk
year: 2010
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Richard Berk
* **Title**: Recent Perspectives on the Regression Discontinuity Design
* **Date of publication**: 2010
* **Pages**: 563-579
* **URL**: [Link to PDF](zotero://open-pdf/library/items/XH32N93V)
* **Tags**: #causal_inference, #comps_exam, #regression_discontinuity

## Abstract

The regression discontinuity design was originally proposed in 1960 as a powerful alternative to randomized experiments. It has been little used since. Over the past decade, however, the design has been increasingly and successfully employed by economists in a variety of studies. In this paper, the fundamentals of the regression-discontinuity are discussed. Recent advances are emphasized.

## My notes

* Focus on the observed responses on either side of the threshold and very close to the threshold. Compare the average value of the outcome variable for observations just to the right and just to the left of the cutoff should provide reasonable estimates of the [[average treatment effect]].
  
	* Why? The trends will hopefully be linear and parallel to each other (suggesting they are useful counterfactuals for each other). The degree to which they are not is the degree to which your estimate will be potentially biased.
	  
	* By narrowing the window or bandwidth of observations, you can more credibly estimate an ATE because the trends should be linear and parallel to each other. However, this has the disadvantage of making your sample smaller and thus your estimates less precise, and it also limits generalizability -> [[bias-variance tradeoff]].
	  
		* One criterion that's popular is to use a window size which minimizes the [[mean squared error]] of the model predictions.
		  
		* You can also minimize [[AIC]] or [[BIC]]. [[Cross-validation]] tools are very helpful here.
	
	* You can do a simple difference in means or you can use a [[kernel function]] to systematically weight observations less the further away they are from the threshold. Different functions can be used to weight observations (linear, Gaussian, etc.).

	* One can also estimate a linear regression on each side of the treatment where the only independent variable is distance from the threshold. The average treatment effect at the threshold (distance from threshold = 0) is the intercept from the one equation subtracted from the intercept of the other equation. Again, one can use a kernel weighting scheme.
	  
		* One can also assume the response functions are not linear and use a [[polynomial regression]] approach in which case the amount of smoothing (which functional form to use) replaces the size of the window as the key matter of tuning. I.e., $Y_{i} = \beta_{0} + \beta_{1}W_{i} + f(X_{i} - T)$ where:
		  
			* $Y_{i}$ is the observed outcome for participant i.
			* $W_{i}$ is the treatment status of participant i.
			* $f$ is the functional form of the relationship between independent variable $X_{i}$ and Y.
			* $T$ is threshold.
			  
		* In such cases, W may not need to be specific and the appropriate window will be found. The risk, of course, comes from over-fitting.
### Extensions

* Having a multi-dimensional threshold (e.g., two-variable threshold would indicate that the assignment procedure is based off a line).
  
* If you have issues with compliance, you can utilize other estimators to account for compliance.

### Rules of thumb

* Descriptively observe your data for trends.
* Apply the difference in means estimator with different window sizes.
* Apply a smoothing procedure to estimate the functional form of the relationship. You can use cross-validation (and [[train/test]]) to ensure you do not overfit.
* You can use the [[Bonferroni correction]] to correct your statistical estimates.