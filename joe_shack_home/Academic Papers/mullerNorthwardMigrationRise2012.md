---
type:
  - Article
author:
  - Christopher Muller
journal:
  - American Journal of Sociology
year: 2012
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Christopher Muller
* **Title**: Northward Migration and the Rise of Racial Disparity in American Incarceration, 1880–1950
* **Date of publication**: 2012-09
* **Journal**: American Journal of Sociology
* **Volume**: 118
* **Issue**: 2
* **Pages**: 281-326
* **URL**: [https://www.journals.uchicago.edu/doi/full/10.1086/666384](https://www.journals.uchicago.edu/doi/full/10.1086/666384)
* **Tags**: #crim501, #mass_incarceration, #policing, #racial_threat
* **PDF Attachments**:
  * [mullerNorthwardMigrationRise2012.pdf](zotero://open-pdf/library/items/A7PXHHE5)

## Abstract

Of all facets of American racial inequality studied by social scientists, racial disparity in incarceration has proved one of the most difficult to explain. This article traces a portion of the rise of racial inequality in incarceration in northern and southern states to increasing rates of African-American migration to the North between 1880 and 1950. It employs three analytical strategies. First, it introduces a decomposition to assess the relative contributions of geographic shifts in the population and regional changes in the incarceration rate to the increase in racial disparity. Second, it estimates the effect of the rate of white and nonwhite migration on the change in the white and nonwhite incarceration rates of the North. Finally, it uses macro- and microdata to evaluate the mechanisms proposed to explain this effect.

## My notes

### Introduction

Why are there racial disparities in incarceration? It is not a recent phenomenon which appeared with the start of mass incarceration in the 1970s. We need to look further back to understand the source of these disparities. Furthermore, it’s hard to demonstrate that racial discrimination in the criminal justice system is directly implicated in the racial disparities found in arrests, convictions, and imprisonment. Efforts to prove otherwise are marred by barriers to causal inference and our inability to measure criminal activity directly. We’ve been looking at the wrong times in the wrong places to answer our question.

- Trends in incarceration and trends in racial disparity are separate phenomena each with its own historical path and subject to its own historical influences. To connect the two, we must recognize their independence. High incarceration is new, racial disparity is not.

This article posits that a portion of the inequality in incarceration was caused by increasing Black-American migration to the North between 1880 and 1950.

1. It assesses the relative contributions of changing demographics in different areas (i.e. geographic shifts in population) and regional changes in the incarceration rate on racial disparities in incarceration. The non-White incarceration rate of the North was much higher than that of the South. Racial disparities could have arisen simply because migrants left a region with a comparatively low incarceration rate to one with a comparatively high incarceration rate.

2. It estimates the effects of White vs. non-White migration on changes in the White vs. non-White incarceration rates in the North. Accelerating migration of Black Americans into the North fueled an increase in the incarceration rate of Black Americans. One explanation might be Hubert Blalock’s [[Minority threat hypothesis]] → until minority groups cross some population threshold, they will face increasing discrimination as their share of the population increases. Recent research hasn’t found this to be the case for incarceration. Muller claims that this is because minority threat is moderated by time and place (minority groups will seem more/less threatening in different times and places). Accelerating Black American migration caused most of the newly arrived European immigrants to band together to protect themselves and construct a White race and a Black race (wages and jobs would be threatened from the increased competition, unsolidified racial hierarchy, unstable situation where groups felt their tenuous position was at stake).

	1. Note → A central way European immigrants advanced themselves politically was through securing patronage positions in municipal services like law enforcement. Irish immigrants, in particular, used policing as a means of advancing themselves but also keeping Black immigrants in check through violence and arrests → see increases in petty crime arrest rates. Class did not protect Black residents. Northern-born, better off, Black Americans were known to claim they hadn’t felt the burdens of discrimination before the arrival of southern newcomers.

1. It uses macro and microdata to evaluate the proposed mechanisms.

	1. Macro-data
	   
		1. **Prediction 1**. Increasing rates of northward migration (to 11 Northern states) should have led the North’s non-White, but not its White, incarceration rate to increase between 1880 and 1950. 

		2. **Prediction 2**. The size of this effect should be larger in states whose police force was composed predominantly of foreign Whites (using data from 1880 to 1920).

			1. Each 100 per 100,000 person increase in a northern state’s non-White migration rate increased its incarceration rate by an average of 1.1 people per 100,000 (no real effect on White incarceration rate).

				1. Without increases in the nonwhite migration rate, the trend in the North’s non-White incarceration rate would have remained flat. Echoes findings from decomposition analysis (uses predictions from the model instead of actual values and finds similar results).

			2. The effect size increased as the proportion of police composed of foreign whites grew. No effect for White Americans. Effects don’t become significant until they constitute a majority of the police force.

	2. Microdata → Use a sample of respondents to the 1940 census to compare migrants’ and non-migrants’ conditional probabilities of incarceration.
	   
		1. **Prediction 3**. Increases in the rate of non-White migration to the North raised the probability of incarceration for Black migrants and non-migrants both. **Confirmed**. Probabilities of incarceration were statistically indistinguishable.

		3. **Dependent variable** → Incarcerated or not. Variables include age, age squared, education, marriage, and residence in a metropolitan region (yes/no). Uses [[Logistic regression]].

### Methods: Increasing migration vs. increasing incarceration rates

- If we fix the the weights (i.e. the proportion of the population of a specific race in a specific state in 1880), this tells us what racial disparity would’ve been if the White and non-White populations hadn’t changed, but the incarceration rates did change.

	- Reduces racial disparity from 5:1 (1950) to 4.2:1, a 29% reduction.
    
- Fixing the incarceration rates at 1880 tells us what racial disparity would’ve been if the incarceration rates didn’t change, but the population composition still shifted.

	- Reduces disparity from 5:1 to 3.3:1, a 64% reduction.
	- Holding constant incarceration for just Northern states reduced disparity by 41%.
    
- **Regression** → Unit of analysis are state-decades. Dependent variable is change in incarceration rate. Independent variables are: migration rate, lagged change in homicide rate, change in the percentage of males ages 10 and over gainfully employed, state fixed effects, period fixed effects, and an error term.

	- Introduces new independent variables: proportion of a state’s police force composed of foreign whites and an interaction term with state’s police force and migration.

### Minority Threat → Assumptions

All 3 assumptions are satisfied.

- Incremental shifts in minority populations are detectable by the majority group.
- These shifts will be construed as threatening.
- The majority group will have the means available to them to act on the perceived challenge to their dominance.

	- Adjustments:
	  
		- We should assess rather than assume shifts in the minority population are detectable.
		  
		- Migration rates are a better index of understanding the perceived threat the majority group might feel.
		  
		- The narrower the status gap between majority and minority groups, the likelier it’ll be that the former will see the latter as a threat.
		  
		- State actors are also civilians with social identities. Knowing who administers state actions may help us understand why the state produces divergent outcomes for different segments of the population (at different times in different places).

### Alternative Explanations

- Increases in incarceration stemmed from increases in crime or unemployment.
  
	- Black migrants tended to be among the best educated and moved to the North to take advantage of the economic opportunities. Southern-born Black-Americans were more likely to be employed and earn higher incomes and have a smaller chance of requiring public assistance than northern-born Black-Americans.
    
	- To account for residential instability changing the crime rate (see [[Collective efficacy|collective efficacy]], rise of public housing) and thus changing the incarceration rate → includes controls for the lagged change in the homicide arrest rate. Not perfect but best we can do.
    
	- To account for changes in employment affecting incarceration rates, controls for state employment rates are included.

- Regional differences in penal regimes. In the South, crime was less likely to be punished through formal channels. This would lead to understated racial disparities in the South. Such concerns should be mitigated by the fact that inmates on chain gangs and leased convicts were counted as prisoners. Regardless, analysis is restricted to samples in Northern states to ensure regional differences aren’t responsible for any observed relationship between rate of migration and change in the incarceration rate.

	- However, there are other reasons for limiting it to the North. Comparable homicide arrest data are unavailable. The instrument is only valid in Northern states.

### Conclusion

Why does this historical disparity persist? The sources which explain its continued existence no longer are present(?). Well… maybe not. Black-Americans have harbored historically-validated mistrust of the police. This may lead to biased samples in whom the police encounter (law-abiding Black Americans avoid the police) thus leading to observations of higher fractions of criminally engaged Black Americans.

- Of course, racial gaps in offending and enforcement persist. The history of this relationship needs to be considered. To connect today’s high rates of Black-American incarceration to the centuries-old association of blackness with criminality, we must understand history; this analysis helps elucidate how the association started and how it’s connected with migration.

### Appendix

[[instrumental variable|Instrumental variable]] design using federal restrictions on foreign immigration. Federal policies on foreign immigrants should affect the nonwhite migration rate which in turn affects the nonwhite incarceration rate. This is an exogenous shock on the nonwhite migration rate (so long as the federal policies towards foreign immigrants doesn’t affect the nonwhite incarceration rate directly and only indirectly through its effect on the nonwhite migration rate).

- Exclusion restriction doesn’t seem violated. No connection between immigration policy and composition of Northern police forces.
- Replicates results of [[OLS]].