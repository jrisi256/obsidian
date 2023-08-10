---
type: [Article]
author: [John R. Sutton]
journal: [American Journal of Sociology]
date: 2000
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: John R. Sutton
* **Title**: Imprisonment and Social Classification in Five Common‐Law Democracies, 1955–1985
* **Date of publication**: 2000
* **Journal**: American Journal of Sociology
* **Volume**: 106
* **Issue**: 2
* **Pages**: 350-386
* **URL**: [https://www.jstor.org/stable/10.1086/316961](https://www.jstor.org/stable/10.1086/316961)
* **Tags**: #determinants_of_mass_incarceration #life_course #marxisms #mass_incarceration #crim_597_sentencing 
* **PDF Attachments**:
  * [suttonImprisonmentSocialClassification2000.pdf](zotero://open-pdf/library/items/7JUA8RXX)

## Abstract

Rates of imprisonment have risen in many Western democracies over the past few decades, most dramatically in the United States. The development of a systematic and general explanation of imprisonment trends has been impeded because of the theoretical and methodological limitations of prior quantitative studies. Most use data from a single country or jurisdiction and focus narrowly on the [[Rusche‐Kirchheimer ]]“labor surplus” hypothesis, with little attention to alternative explanations. This study takes a cross‐national perspective, using longitudinal data from Australia, Canada, New Zealand, the United Kingdom, and the United States to offer an institutional account of imprisonment rates. The labor surplus effect is treated as a special case of a more general process by which individuals are allocated among alternative life‐course paths. This allocation process is likely to be influenced by macrolevel institutional arrangements and contests for political power. Hypotheses are tested using pooled time‐series cross‐section regression techniques. Results support this broadened perspective: prison growth is driven not only by crime rates and unemployment rates, but also by welfare spending and the power of right parties.

## My notes

### Introduction

- Imprisonment rates in the US were gradually declining until the mid-1970s until they increased fourfold over the next two decades. They’ve also been increasing in the UK as well but at a more modest pace. Most other Western democracies have also seen moderate expansion, few have remained constant or declined.

- USA explanations -> baby boom and increased population + structural vulnerability of the USA to moral panics, opportunistic use of crime + welfare as wedge issues, intense focus on crime by the media. However all these things were true in places other than the USA and yet the USA still experienced such a large boom in prison populations.

- Dominant Neo-Marxist approach (Rusche and Kirchheimer) has pursued the argument that prisons in capitalist society are mechanisms for controlling surplus labor. Studies have explored the connection between imprisonment rates and the rise and fall of the business cycle. However studies have yet to identify the causal mechanisms in play.

- Gramsci and Foucault -> causal link is ideological hegemony. Discursive chains which coordinates ideas and practices. Economic interests remain the causal priority though.

- Durkheim and Weber -> Culture and politics. Prisons offer up symbols of what is deviant and what isn’t and they offer up ongoing negotiations of normative boundaries and political authority.

- Durkheim & Bourdieu -> Institutions provide schemas that individuals use to sort events into categories providing meaning and value and proper relations. People are sorted this way too. You are put on a path and are constantly being evaluated as to how successful you are relative to that path. An important classification is criminal vs. non-criminal -> but these classifications are dependent upon society’s ability to produce them i.e. their capacity to punish and what institutions or arenas are set-up to handle these classifications (drug users, criminals or sick patients).

- Garland and Elias -> penal practices emerged from a long-term civilizing process in Western society -> pacification of interpersonal conflict, development of the genteel, privatization of sexuality -> civilization is built on repression and prisons are the most obvious expression of that repression. Doesn’t offer much to help us explain variations in punishment trends among Western countries.

### Current study

- [[Life course theory|Life course]] patterns -> individual involvement with legitimate institutions lowers the probability of criminal activity. As opportunities for legitimate attachment increase, rates of crime and incarceration will decrease. It’s stochastic though in the sense that conforming values are emergent and add to the path dependence in a mutually reinforcing fashion -> [[Routine activity]] theory suggests individuals with less free time won’t commit as much crime, organizational level social control agents use classificatory logic (often based on short-hand, devised through rough experience classification schemas) or stereotypes.

	1) Organizations create typical patterns of dispositions and make official assessments of where someone lies.

	2) These classification schemas are developed with regard to resource constraints. A homeless man can be -> drunk, insane, criminal, or just need a place to sleep. Competition among social fields for resources determine the schema -> determine different life-course paths available to people.

### Hypotheses

1) The greater the proportion of young males in the population, the higher the rate of prison growth.
2) The higher the homicide rate, the higher the rate of prison growth.
3) Expansion in military enlistments reduces rate of prison growth.
4) Expansion in young men’s secondary and tertiary school enrollments reduces rate of prison growth.
5) Growth in unemployment rates increases the rate of prison growth (Rusche-Kirchheimer hypothesis which now appears as a special case of the other hypotheses) -> unemployment is not a proxy for criminal motivation or class interests of criminal justice decision makers. Serves as a measure of slack capacity in the labor market.
6) Growth in welfare spending aimed at workers and families with children decreases the rates of prison expansion (new classification schemas being pushed) -> addresses issues of crime and mediate effects of business cycles.
7) Growth in public spending for education decreases rates of prison expansion.
8) Prison populations expand when right-wing parties are in power vs. leftist and centrist parties.

Likely all these factors interact and aren’t simply additive. Life-course and policy effects likely interact with politics. Right-wing parties are likely to make the argument a tradeoff is needed between higher welfare spending and higher spending on law and order. Another issue is whether the effects are different from the US vs. other countries because the US is such an outlier. Are the effects stronger under right-wing parties in the US?

### Data

* Dependent variable -> No standardized data collection on prisons/jails across countries. Make do with what we got so to speak. We’re looking at imprisonment rates. 

* Independent variables -> Homicide rates, military enlistment, male school enrollment, unemployment rates, welfare spending, education spending, right-wing party dominance.

* Method: 28 years of observation available for 5 countries yielding 140 observations. They use [[pooled time-series cross-sectional]] analysis -> useful when you have few *individuals* (i..e, countries) and are more concerned with the effects of time.
	* Use a 3-year lag for the imprisonment variable.
	* They include dummy variables for the countries so this does not seem to be pooled time-series cross-sectional analysis but a more typical [[fixed effects]] estimation procedure.
	* Standard errors are *panel corrected*, but I do not really know what this mean. I assume this means they use [[Clustered standard errors]] at the country level. #question   
	* Use [[OLS]] and not [[WGLS]].
	* Use some techniques to determine the *deterministic trend* versus the *stochastic trend* -> use some form of difference techniques to determine the trends of the time series.

### Results

1) Percentage of young males not found to be significant.
2) The higher the homicide rate, the higher the rate of prison growth (in all but 1 model).
	1) Some supplementary analysis seems to suggest these two variables are connected. The influence of one seems to be mediated through the other. In any case, the supply side variables are appropriately specified.
3) Male school enrollment not found to be significant.
4) Military enrollment found to be significant and strangely positively associated.
5) Unemployment rates found to be significant and positively associated.
	1) The only life course variable found to be significant.
6) Welfare spending found to be significant and negatively associated.
	1) It is important this variable is specified in the model otherwise the effect of unemployment becomes biased (the unemployment variable would be indirectly capturing how welfare spending tends to go up as unemployment increases -> if only because more people applying for unemployment).
7) Education spending not significant.
8) Right-wing party dominance is significant and positively associated.

Looking at standardized variables to compare effects, prison growth is constrained/predicted most by prior size of prison population and incidence of homicide. All the other variables vary but are pretty close in value.

1) Prison growth is partly an instrumental response to increases in crime, but this is a bit murky because it also grows more quickly where there are young males.
2) Unemployment is important as pointed out by Rusche-Krichheimer, but it isn’t the only factor. It’s part of a rich and complex set of institutional processes.

Interaction Effects -> Expectation were that interaction effects would be in the same direction as main effects and stronger under right-party rule and in the US. Results are more complex.

- For example, right-wing parties seem to blunt the main effect of unemployment (drive it to zero). The interpretation seems to be that right-wing parties raise the rate of prison growth so much so that fluctuations in the business cycle (as measured by unemployment) no longer matter.

- The decelerating effect of welfare spending on prison growth seems to be confined to the USA i.e. welfare spending in the USA (only) seems to reduce prison growth.

- Similar findings in welfare where more spending on education does seem to reduce prison growth (again only in the USA).

- Only in the USA do right-wing parties effectively encourage punitive policies.

- Very strange results though. So some supplemental analyses are called for to make sense of these results.
  
	- We find main effects of right-wing parties and the USA are independent and additive. Lowest baseline rates of prison expansion are in countries other than the USA when right-wing parties are out of power, and the highest rates in the USA when the right-wing party controls power. Unemployment effect disappears when right-wing parties are out of power.

	- Welfare spending is most effective in the USA, but it’s effective elsewhere too.

### Conclusion

We’re trying to answer the question why there are differential growth rates in prisons across countries. Try to fix this problem by nesting the labor market/imprisonment association (Marxism) within a broader system of social classification -> prisons are an institution and not just instruments of social control/class oppression.

Classification patterns are the outcomes of institutional projects which operate at 3 levels:
1) Allocation of persons among life-course paths.
2) Trade-offs among social programs that manage socially marginal populations.
3) Contests for political dominance.
    
* Dominant life-course effect comes from fluctuations in labor markets.
* Strong evidence of policy trade-offs as declines in welfare spending are associated with growth in imprisonment.  
- Politics matter too.
- Strangely(?) military expansion contributes to the expansion of prisons. If it is a real effect, it must operate in diffuse and long-term ways because enlistment and imprisonment trends are not parallels of each other. Perhaps the effect stems from slow demobilization and are echoes from ramp-ups from wars (Korea and Vietnam) -> ideological mutualism in how coercive policies used in domestic and international arenas -> speculation.

#### Key Findings

- Net of supply-side factors (young men and more homicides), prisons grow when conservative parties are in power, when social spending is constrained, when there is an economic downturn, and perhaps under conditions of long-term military mobilization -> Moves away from an instrumental account towards one that emphasizes the politics of a moral order.

- How is the USA different? The effects of welfare spending and education spending and right-wing parties are exaggerated somewhat. It is perhaps the case that the US is much more decentralized and administratively fragmented leading to highly politicized and localized policy debates. Policy deliberations happen in campaigning not in government ministries. Symbolic stakes are higher. Much more responsive to moral panics and the vicissitudes of public opinion.