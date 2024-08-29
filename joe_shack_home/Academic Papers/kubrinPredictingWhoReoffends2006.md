---
type:
  - Article
author:
  - Charis E. Kubrin
  - Eric A. Stewart
journal:
  - Criminology
year: 2006
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Charis E. Kubrin, Eric A. Stewart
* **Title**: Predicting Who Reoffends: The Neglected Role of Neighborhood Context in Recidivism Studies*
* **Date of publication**: 2006
* **Journal**: Criminology
* **Volume**: 44
* **Issue**: 1
* **Pages**: 165-197
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1745-9125.2006.00046.x](https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1745-9125.2006.00046.x)
* **Tags**: #comps_exam #incarceration #neighborhood_context #recidivism 
* **PDF Attachments**:
  * [kubrinPredictingWhoReoffends2006.pdf](zotero://open-pdf/library/items/GER29HFS)

## Abstract

Prior studies of recidivism have focused almost exclusively on individual-level characteristics of offenders and their offenses to explore the correlates of reoffending. Notably absent from these studies are measures reflecting the neighborhood contexts in which individuals live. The current research addresses this shortcoming. Using data on a sample of ex-offenders in Multnomah County, Oregon (Portland and surrounding area) in conjunction with 2000 census data, we answer two questions. First, which individual-level factors influence rates of recidivism? Second, to what extent does neighborhood socioeconomic status account for variation in the reoffending behavior of ex-prisoners that is not explained by their individual-level characteristics? We find that those who return to disadvantaged neighborhoods recidivate at a greater rate while those who return to resource rich or affluent communities recidivate at a lesser rate, controlling for individual-level factors.

## My notes

#paper_idea -> Important to cite this paper in terms of establishing the importance of neighborhoods.

#disagree -> See [[kirkResidentialChangeTurning2012]] who finds that neighborhood socioeconomic context did not have a statistically significant association with the probability of an ex-prisoner reoffending. They found distance from parish was what was really the key factor.
### Research Questions

* What individual-level factors influence rates of recidivism?
* What neighborhood socioeconomic factors account for variation in recidivism above and beyond individual-level characteristics?

### Background

Being able to successfully reintegrate relies upon a prisoner having access to services and resources to help them find housing, secure employment, receive treatment, and comply with the terms of their supervision. Some neighborhoods will be better equipped to help these ex-prisoners obtain these services while others will not.

The community networks in place in various neighborhoods will also be important for helping to build and maintain social capital which ex-prisoners can tap into to help themselves and integrate themselves into the community.

### Data

* Data is based in Multnomah County (Portland, Oregon and surrounding areas) in the year 2000 from January to June.
  
* Sample was all individuals released from prison during this time period and put under community supervision or put directly into community supervision.
  
* Variety of individual-level variables (age, sex, race, current offense, risk-supervision level, criminal history).
  
* Tracked offenders for up to 1 year post-admission date into community supervision.
  
  Use offender home address to match them with their appropriate census tract.

**Dependent variables** -> Recidivism. Measured as a new arrest.
**Independent variable**:
* The new shiny one of interest is [[Concentrated disadvantage|concentrated disadvantage]] of census tracts -> absolute inequality. The degree to which certain conditions (e.g., poverty and unemployment) coexist.
* They also measure [[index of concentration at the extremes]] -> relative inequality. The degree to which person with various levels of these conditions coexist.

### Methods

Use [[Multilevel modeling|multilevel modeling]] and [[Logistic regression]]-> individuals released into the same neighborhood may be more similar than individuals in another neighborhood and are not completely independent observations. Failure to account for this non-independence would lead to standard errors that were too precise.

Multilevel modeling also allows for the simultaneous investigation of individual and neighborhood-level variables and how much each contributes to explanation of the variance.

Level 2 model uses the intercept from the level 1 model as a dependent variable. Random intercept, fixed slope.

### Results

**Table 2** -> Models 3 and 4. Even after controlling for individual-level characteristics (which are important and remain significant). Concentrated disadvantage and ICE are shown to be statistically significant.
* As disadvantage increases, the likelihood of recidivating increases.
* As ICE increases (indicating more affluence), the likelihood of recidivating decreases.
### High-level results

* Those parolees who return to disadvantaged neighborhoods recidivate at a higher rate than those who return to more affluent communities even when controlling for individual-level characteristics.

### Limitations

Do ex-offenders live in their officially provided address?