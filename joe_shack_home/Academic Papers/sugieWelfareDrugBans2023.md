---
type: [Article]
author: [Naomi F. Sugie, Carol Newark]
journal: [American Journal of Sociology]
date: 2023-07
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Naomi F. Sugie, Carol Newark
* **Title**: Welfare Drug Bans and Criminal Legal Cycling
* **Date of publication**: 2023-07
* **Journal**: American Journal of Sociology
* **Volume**: 129
* **Issue**: 1
* **Pages**: 41-75
* **URL**: [https://www.journals.uchicago.edu/doi/abs/10.1086/725424](https://www.journals.uchicago.edu/doi/abs/10.1086/725424)
* **Tags**: #journal_club #recidivism #welfare #welfare_drug_ban
* **PDF Attachments**:
  * [Sugie_Newark_2023_Welfare Drug Bans and Criminal Legal Cycling.pdf](zotero://open-pdf/library/items/W6Q8FX7L)

## Abstract

Punitive policies of welfare and criminal legal systems reflect a shared orientation governing social marginality. The welfare drug bans, which prohibit people convicted of drug-related felonies from receiving cash assistance and food stamps, are a key example of increasing synergies between the two systems. In this article, we examine whether the bans increase recidivism by leveraging a methodologically rigorous approach using administrative data from California to compare rearrest rates among people convicted before and after the bans. We find that the cash assistance ban has no measurable impact on recidivism, but the food stamps ban hastens time to arrest, particularly in counties with more accessible policies and more generous benefits. We also find differences in the bans” effects by gender and race/ethnicity, with consequences concentrated among non-Hispanic White and Black men. The findings underscore the importance of inclusive welfare systems for protecting against repeat contact with the criminal legal system.

## My notes

* Welfare drug ban -> Lifetime prohibition on cash assistance and food stamps for anyone convicted of a drug-related felony. Inter-coupling of social welfare and criminal justice systems. Achieve social control through more punitive policies. Criminalizing poverty.
  
* Many argue that by kicking people out of social welfare programs (particularly during a very unstable period in a person's life such as post-release), it more likely they'll recidivate. 

### What is the research question?

* Do welfare bans influence the likelihood of rearrest? Are there different effects on recidivism for different welfare programs? E.g., cash assistance vs. food stamps.
  
	* The effects are not straightforward. The authors argue that recipients have to balance the benefits of receiving benefits with the costs of navigating the punitive welfare system. Thus, if someone is no longer eligible for a welfare program, it may not always lead back into recidivism since, on net, it is not that big of a loss.
	  
	* As they will later argue, I am sure, if one lives in an area with a more robust welfare system, having that welfare taken away from you is more detrimental and is thus more likely to lead you back into recidivism 

### How do you propose to answer it?

* California implemented welfare drug bans for cash assistance and food stamps at different times and this study leverages these different dates to see if there is any difference between the two programs.
  
* Administrative data from the California Department of Justice which includes most criminal legal system records for individuals convicted for drug-related felonies.
  
	* The first sample ([[TANF]] sample or cash assistance) is all individuals convicted three months before and after January 1, 1998 (cutoff date of the ban).
	  
	* The second sample ([[food stamps]] sample) is all individuals convicted three months before and after August 22, 1996.
	  
	* In sensitivity analyses, they use different dates. Different government documents refer to different starting dates for the program.
	  
* **Dependent variable** -> any arrest following the focal conviction. Any arrest before January 1, 2004 (California made changes to the law). Sensitivity analyses extend the analysis to March 2013 (full data).
  
* **Control variables** -> County-level welfare generosity: 1) ratio of TANF recipients to population in poverty, 2) Ratio of food stamp recipients to population in poverty, 3) average TANF expenditures per recipient in the county, 4) average food stamp benefit per recipient in the county. Data comes from the [[Stanford California Welfare Laboratory]] or the [[Stanford Center on Poverty and Inequality]].
	* Interact the ban with these variables to see if the results differ by local county welfare context.
	* Unfortunately, they only have the county of conviction and not county of release.

* Also look at age, gender, race/ethnicity, length of custody and supervision, number of prior arrests, number of prior drug arrests, and age of first arrest.
	* Estimate a regression model for different subgroups based on gender and race/ethnicity.
  
* Assume that people who were convicted just before and just after the ban are similar, and it is as good as random when people were arrested in relation to the ban hence the relatively small 3-month window.
	* **Table 1** -> No observable differences between the two groups (pre-ban and post-ban).
	* Estimate [[intend-to-treat]] or ITT effects. This is not a test of how welfare affects recidivism. It is a test of how being subject to a ban on welfare affects recidivism. To the degree you believe that individuals do not receive welfare after being banned, that is the degree to which this measure the direct effects of not being able to access welfare.
	  
* Use [[survival analysis]] specifically [[Cox proportional hazard models]] to estimate the relationship between bans and time to arrest.
  
* Sensitivity analysis -> They estimate their models using [[Weibull distibution]]. Use arrest date rather than conviction date as the cutoff. They conduct placebo tests using fake cut-off dates (to see if effects could be the result of some larger more general trend at that time).
	* Do find some localized temporal trends around the TANF ban date which complicates their findings for that program. Food stamps, though, seem free of temporal trends.
### What do you find?

* Food stamp bans lead to higher recidivism especially in counties with more inclusive welfare policies. See **Table 3**.
  
* Different results by gender and race/ethnicity. Results are worst for White and Black men (food stamps). Why? Hypothesizing only, but it seems as if women are more closely connected to family post-release, and they're more likely to be caring for others (can access the benefits of their dependents and pool resources).
	* Find some suggestive results for Black women that being banned from welfare actually led to lower re-arrest rates. The authors interpret this to mean that, for Black women, welfare is a net negative for Black women (subject to the harshest policies in terms of navigating their receipt of it).

![[sugieWelfareDrugBans2023_fig2.png]] 
Time to rearrest -> those subject to the food stamps ban have a shorter time to rearrest.
#figure 