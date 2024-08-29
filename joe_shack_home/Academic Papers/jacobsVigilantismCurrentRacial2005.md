---
type:
  - Article
author:
  - David Jacobs
  - Jason T. Carmichael
  - Stephanie L. Kent
journal:
  - American Sociological Review
year: 2005
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: David Jacobs, Jason T. Carmichael, Stephanie L. Kent
* **Title**: Vigilantism, Current Racial Threat, and Death Sentences
* **Date of publication**: 2005
* **Journal**: American Sociological Review
* **Volume**: 70
* **Issue**: 4
* **Pages**: 656-677
* **URL**: [https://www.jstor.org/stable/4145381](https://www.jstor.org/stable/4145381)
* **Tags**: #crim_597_sentencing, #death_penalty, #history_of_place, #racial_threat #lynching
* **PDF Attachments**:
  * [jacobsVigilantismCurrentRacial2005.pdf](zotero://open-pdf/library/items/9QQFJ5MB)

## Abstract

Capital punishment is the most severe punishment, yet little is known about the social conditions that lead to death sentences. Racial threat explanations imply that this sanction will be imposed more often in jurisdictions with larger minority populations, but some scholars suggest that a tradition of vigilante violence leads to increased death sentences. This study tests the combined explanatory power of both accounts by assessing statistical interactions between past lynchings and the recent percentage of African Americans after political conditions and other plausible effects are held constant. Findings from count models based on different samples, data, and estimators suggest that racial threat and lynchings combine to produce increased death sentences, but the presence of liberal political values explains the absence of death sentences. These findings both confirm and refine the political version of conflict theory because they suggest that the effects of current racial threat and past vigilantism largely directed against newly freed slaves jointly contribute to current lethal but legal reactions to racial threat.

## My notes

### Introduction

Is there a connection between lynchings and areas that want to impose the death penalty? Studies which try to hold all other variables constant during sentencing find a race effect sometimes. The evidence is mixed. Perhaps they’re ignoring the racial history of the USA.

Some claim the death penalty is meant as a replacement for the vigilantism and lynchings of the past. On the face of it, seems plausible. States that once had highest lynching rates now use the death sentence the most. Comes from conflict theory literature, the law is meant to control underclass populations. In the past, Whites viewed lynchings as the primary way of controlling Black Americans.

Does vigilantism in the past combine with current racial threats to white dominance attributable to larger black populations to operate together to produce disparities in death sentencing? As well as increasing the rates of death sentences. Death sentences should be especially likely in states w/ the largest minority populations that also had a history of frequent vigilante violence. These states see the state sanctioned use of lethal force as replacements for lynchings.

### Hypotheses

H1 -> Number of death sentences should be greater in states with a history of multiple lynchings because this tradition should still produce greater pressures on court officials and juries to impose the death penalty.

H2 -> From the racial threat and racial conflict literature, the number of death sentences will be greater in states with more Black Americans/Latinxs. The relationship may not be linear as Black Americans reach a certain threshold and achieve acceptance or power.

H3 -> The relationship between the % of Blacks and death sentences should be positive, but where the black population has reached a threshold, this relationship should become negative.

H4 -> Interaction effects. Death sentences should be most common in states that have the larger proportions of Black Americans combined with a history of repeated lynchings (similarly in the absence of a large enough Black population, a prior history of lynching may not be enough OR a large Black American population may not be enough to trigger racial threats in areas without a history of lynchings). Possible both Blacks and Whites are executed more in these areas.

- Where lynching rates were exceptionally high, expect far larger Black American proportions will be necessary before the number of death sentences begins to decline.

![](https://lh3.googleusercontent.com/dd5bIVEw2Q1jVL2RAQBqAzVcSvmUBQKVv6sqtNAKLVd7Lwz-2mlkLRgZj08-LoS1SFaXSPVJYQF97BwvlebmQSyofyQtT2aVHwhEDaxRRfxhw_KakrgCR-57YJP9jLn5T-hcewImUgxtNELYVAoR)
### Alternative Explanations

- More death sentences where conservative values dominate.
- More death sentences in states with fundamentalist church traditions.
- Death sentences should be more frequent in states where judges are elected.
- Death sentences should be more frequent in states with a Republican governor.
- Marxist view that unemployment and incarceration should be linked -> mixed evidence -> nevertheless suspect higher unemployment will lead to higher rates of death sentencing -> threat to social order.
- Jurisdictions with highest violent crime rates should be more likely to use the death sentence. Property crime rates may be important too.

### Data

- Except for lynchings, use explanatory variables from 1970, 1980, and 1990 to explain death sentence counts in 1971-1972, 1981-1982, and 1991-1992 -> N = 144 state years. Use different counts of lynching data (one from NAACP and another from Tolnay and Beck which was hand counted for 10 states -> use more years on this data).

- Use a [[zero-inflated]] [[negative binomial regression]]. Model those factors which produce zero scores and the other equation models factors that produce one or more death sentences. Zero inflated useful here to account for states where it was illegal -> retain states without death penalty and avoiding selection bias (by excluding those states and potentially biasing results).

- Dependent Variable: Use a dummy variable if the percentage of Black Americans in a states is greater than 6.4%. Get this from the literature apparently, turning it into a threshold. Compute lynching ratres from NAACP and then from Tolnay and Beck.

- Independent Variables: Use ideology scores, % of residents who are members of fundamentalist churches, UCR violent and property crime rates, dummy variable if judges are elected in partisan elections, unemployment, population and its square. Dummy variables for place and time.

### Results

![](https://lh3.googleusercontent.com/7seeq7_kNBGJQtmpoBuIJ_PC0k62CFCoXzKft87MjE6fNTn2jW2lUOGhxVdKIiezBdEMKoxK7fvy5K37knKMmbrv7EVGfW_9uy0UmxXm92qX-jDY5pQjrPr7MJQ3FOJ3rry1dtFRDfKqoHM7mNzq)

Above table shows there is definitely descriptive support for their findings.

Table 3 -> Models 1 and 2 all Death Sentences -> Regression results. **Interaction between Black American presence and prior lynchings is associated with state propensity to use the death sentence** -> also it’s nonlinear as expected and the threshold before it starts declining is higher in areas with histories of more intense lynching. Higher violent crime rates and higher fundamentalist church memberships are also positively associated with death sentences.

Table 3 -> Models 3 and 4, Black Americans -> Black American presence and lynching interaction even stronger. Unemployment becomes significant but religious fundamentalism goes away. Predicting zero counts… find zero counts are very unlikely in states with Republican governors and conservative views.

Findings replicate across data sets.

**Supplemental Analyses** -> Results hold even after removing the four state-years with the most death sentences. Additional economic indicator variables (inequality, poverty, black-white income gap) have no effects. Using a continuous variable for percentage of blacks leads to the same findings but reduced explanatory power.

### Conclusions

Mixed results for Hispanic threat. More time and analysis needed to see if it approaches Black American findings. Perhaps unlikely because they don’t have the same history. Curious that Republican control of the governor’s office explains the presence of at least one black death sentence but not the overall number. Liberal states associated with absence of black death sentences.

Court officials and juror cannot escape their social environment. Invoke [[savelsbergKnowledgeDominationCriminal1994]] that public opinion holds more sway here due to the populist nature of our democracy. Mass values are more influential here -> Europe has more in between layers and more un-elected bureaucrats -> These results might not hold elsewhere.

Need to take into account history.