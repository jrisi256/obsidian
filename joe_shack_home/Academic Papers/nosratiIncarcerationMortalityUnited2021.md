---
title: "Incarceration and mortality in the United States"
author: Elias Nosrati, Jacob Kang-Brown, Michael Ash, Martin McKee, Michael Marmot, Lawrence P. King
year: 2021
journal: SSM - Population Health
type: article
---
[Zotero entry](zotero://select/items/@nosratiIncarcerationMortalityUnited2021)
**Tags**:
## Abstract

The ongoing COVID-19 pandemic has spotlighted the role of America's overcrowded prisons as vectors of ill health, but robust analyses of the degree to which high rates of incarceration impact population-level health outcomes remain scarce. In this paper, we use county-level panel data from 2927 counties across 43 states between 1983 and 2014 and a novel instrumental variable technique to study the causal effect of penal expansion on age-standardised cause-specific and all-cause mortality rates. We find that higher rates of incarceration have substantively large effects on deaths from communicable, maternal, neonatal, and nutritional diseases in the short and medium term, whilst deaths from non-communicable disease and from all causes combined are impacted in the short, medium, and long run. These findings are further corroborated by a between-unit analysis using coarsened exact matching and a simulation-based regression approach to predicting geographically anchored mortality differences.

### Mechanisms

* Worse individual health for incarcerated individuals due to increased exposure to infectious diseases and increased vulnerability in the first two weeks of release via stress-related mechanisms.
  
* Family members have lower income, lower parental investment, and unstable social relationships.
  
* Incarceration leads to the removal of prime-age working men from local communities causing the fragmentation of family relationships and the erosion of community social ties. "... the material and symbolic fabric of social life is eroded..." #quote 

## Data

County-level from 1983 to 2014.

* **Dependent variables**
	* Communicable disease mortality rate.
	* Non-communicable disease mortality rate.
	* All-cause mortality rate.
	* I will note that they said they got their data from the Institute for Health Metrics and Evaluation. When I investigated, I could not find the data they were referencing concerning mortality broken down by cause (because they do not do a very good job distinguishing between communicable vs. non-communicable).
* **Independent variables**
	* Prison admissions data from [[Vera Incarceration Trends]].
	* As they detail in [[nosratiEconomicDeclineIncarceration2019]], they drop Alaska, Connecticut, Delaware, Hawaii, Rhode Island, and Vermont because they have joint jail + prisons. They also exclude Virginia because they had consistently changing county boundaries.
	* **Controls**: Median household income, high school graduation rates, % Black, % Hispanic, % non-White other ([[ACS]]) and violent crime rate [[UCR]].

### Methods

* [[fixed effects]] for county and year using [[OLS]] regression.
  
* Use an [[instrumental variable]] where the first stage equation predicts the incarceration rate (based on the instrument) and the second stage equation uses the predicted incarceration to predict the outcome.
  
* The instrument is an interacted variable that is $\overline{T_{i}} \times C_{t}$ where $\overline{T_{i}}$ is the average incarceration rate for county $i$ and $C_{t}$ is the aggregate per capita expenditure on the construction and maintenance of correctional facilities nationally for year $t$ (data comes from [[Bureau of Justice Statistics' Justice Expenditure and Employment series]]). Missing data is imputed using a spline function.
  
* They also use [[coarsened exact matching]].