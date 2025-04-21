---
title: "A consequence of mass incarceration: County-level association between jail incarceration rates and poor mental health days"
author:
  - Ashley Hickson, Ritika Purbey, Lorraine Dean, Joseph J. Gallo, Roland J. Thorpe, Keshia Pollack Porter, Aruna Chandran
year: 2022
journal:
  - Health & Justice
type:
  - Article
---
[Zotero entry](zotero://select/items/@hicksonConsequenceMassIncarceration2022)
**Tags**: #effects_of_incarceration #community_effects #incarceration_health 
## Abstract

Mass incarceration has mental health consequences on those directly affected; some studies have also shown spillover effects on the physical health of the surrounding population. There is a dearth of research on the spillover mental health consequences of mass incarceration. This study aimed to quantify a consequence of mass incarceration which may adversely affect the population's health and widen health disparities.

### Mechanisms

* The incarceration of a family member can adversely affect the mental and physical health of the individual as well as their family. The authors posit incarceration can also affect other individuals in the community not focally affected by incarceration.

### Data & Methods

* Unit of analysis is counties. I think it is for 2018? 2,823 counties.
* **Independent variable**: Annual average daily jail population from [[Vera Incarceration Trends]].
* **Dependent variable**: Age-adjusted mean number of reported poor mental health days in the past 30 days from the [[County Health Rankings and Roadmap tool]] which compiles data from the [[Behavioral Risk Factor Surveillance System]].
* **Controls**: % Black, % Male (removed due to collinearity), violent crime rate (2014 - 2016) from [[County Health Rankings and Roadmap tool]] which got it from the [[UCR]], and the [[Social Vulnerability Index]] (poverty, unemployment, income, education, single-parent households, age structure, disability, English-speaking ability, housing type).
* [[negative binomial regression]]. Use total population as an offset variable. included a categorical variable for state, I believe.

### Results

* The authors talk about percentage increases (did they take the natural logarithm?) but regardless, increases in the incarceration rate lead to increases in the number of poor mental health days.