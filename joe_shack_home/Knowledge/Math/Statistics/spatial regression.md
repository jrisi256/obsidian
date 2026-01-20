---
type: Note
aliases: [Spatial regression]
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #comps_exam #statistics #methodology #spatial_analysis #regression

## Two general approaches for dealing with spatial dependence

### Spatial lag regression

* Models spatial autocorrelation in the dependent variable.
* Misspecifying a model where there is a spatial lag (i.e., a process of diffusion or influence where neighboring areas affect the focal area) will lead to biased coefficient estimates.
* Add a term to the regression equation that is the weighted average of values at neighboring locations. Where $\rho$ is the spatial autoregressive parameter, $W$ is the spatial weights matrix, and $y$ are the observed neighboring values for homicide.
* Although it may be more appropriate to consider $\rho$ as a spatial multiplier rather than diffusion because: A) it is not actually longitudinal data, B) you can expand the equation to see how homicide in a focal neighborhood is now a function of the homicide rate of its neighbors, its neighbors' neighbors, etc. See [[kirkCulturalMechanismsPersistence2011]] and [[morenoffNeighborhoodInequalityCollective2001]].
* $$Y = \rho\\Wy + X\beta\\ + \epsilon\\ $$
### Spatial error regression

* Models spatial dependence in the error term.
* Spatial error arises from the omission of spatially correlated independent variables which also influence the dependent variable. It is similar conceptually to time series autocorrelation. There is spatial dependence in the error term of a spatial unit and the corresponding neighboring units.
	* Neighboring counties are more similar than distant counties meaning the error terms will be correlated which is a violation of [[OLS]] assumptions. These spatially correlated errors are indicative of spatially correlated omitted variables.
* Misspecifying a model where there is spatial error dependence leads to inefficient estimates.
* $$Y = X\beta\\ + \epsilon\\ $$ where $$\epsilon\\ = \lambda\\W\epsilon\\ + u $$
* What the equation is doing is splitting the error into random error (independently and identically distributed) and spatial structural error. The random error is $u$. The spatial error, $\epsilon$, is weighted by the spatial weights matrix $W$. The $\lambda$ is a spatial error coefficient. If it is 0, then there is no spatial correlation between our errors. If is not 0, there is spatial correlation, and our coefficients will be unbiased but inefficient.

### Useful links

* [Great tutorial in R](https://www.emilyburchfield.org/courses/gsa/spatial_regression_lab#fnref2)
