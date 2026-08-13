---
title: Ruled by the Demons? Exploring the Relationship Between Belief in Demons and Public Attitudes Toward Donald Trump and Joe Biden
author: Fanhao Nie
year: 2024
journal: Social Currents
type: Article
study type: Quantitative
sample size: "1071"
sampling frame: Qualtrics
sample location:
  - USA
study method:
  - Survey
  - "[[Cronbach's Alpha]]"
  - "[[Chained Multiple Imputation]]"
  - "[[Ordinary Least Squares Regression]]"
  - "[[Ordered Logistic Regression]]"
study start: 2023/03
dependent variable(s):
  - Views of Donald Trump and Joe Biden
main independent variable(s):
  - Belief in supernatural evil
hypotheses supported?: Somewhat
---
[Zotero entry](zotero://select/items/@nieRuledDemonsExploring2024)
**Tags**: #belief_in_demons #paper_belief_demons_trump_support #support_trump_biden #spiritual_warfare 
## Abstract
Beliefs in supernatural evils are prevalent among many religions. Prior research has shown that beliefs in supernatural evils were tied to various social and health outcomes. However, much less is known about the political implications of beliefs in supernatural evils. To fill this research void, a national survey of 1,092 adults with oversamples of respondents of Asian or Hispanic heritage was conducted in March 2023. The findings suggest that a stronger belief in demons or evil spirits was associated with more negative views toward President Joe Biden. This demonic effect was robust even after controlling for a variety of religious and sociodemographic variables. Besides being robust, the demonic effect was the strongest among all religiosity measures. In contrast, a main relationship between a stronger belief in demons and greater support for Donald Trump was found. However, this demonic effect was explained by Christian nationalism. Finally, these demonic effects vary based on one's political party identity.
## Results
1. Stronger belief in demons will be associated with favorable views of Trump because they see Trump as the defender of the moral order from demons. -> **Weakly supported**.
2. Stronger belief in demons will be associated with less favorable views of Biden as will be seen as the means through which demons will invade. -> **Supported**.
3. The gap in views of Trump will increase between Republicans and Democrats as the strength of belief in demons increases -> **Weakly supported**.
4. The gap in views of Biden will increase between Republicans and Democrats as the strength of belief in demons increases -> **Moderately supported**.
	1. Both H3 and H4 come from the fact that it is hypothesized that conservative individuals will be more strongly affected by their belief in demons. 
## Theory
1. Belief in demons has been shown to be associated with a variety of outcomes and beliefs (e.g., poorer mental health, stricter parenting, stronger punitive views toward pornography and criminal conduct).
2. A strong belief in demons and evil spirits may lead to a dichotomized worldview, perceiving the world as good versus evil. Such a worldview has been termed the [[spiritual warfare perspective]]. In order to reestablish the unity and purity of the in-group, a community needs to expiate and expunge the collective perceptions of sin, which are represented by demonic forces. The violation of moral order may produce [[moral panic]], which is defined as social processes in which a behavior or group of people is seen as disproportionately harmful or dangerous relative to the actual threat they pose.
3. People who subscribe to the spiritual warfare perspective are more likely to see social situations as morally binary.
4. Political candidates and groups who represent their sociocultural values (often conceptualized as the dominant or traditional values) would be perceived as spiritual warriors defending righteousness while political forces representing groups with opposing views would be viewed as demonic.
## Methods
### Dependent variable
1. **Views toward Donald Trump**. Coded from -2 to +2 with -2 being very unfavorable, 0 being neutral, and +2 being very favorable.
2. **Views toward Joe Biden**. Coded from -2 to +2 with -2 being very unfavorable, 0 being neutral, and +2 being very favorable.
### Independent variables
1. **Belief in supernatural evil**. Coded from -2 to +2 with -2 meaning definitely disbelieve, 0 meaning not sure, and +2 meaning definitely believe.
### Controls
1. **Religiosity scale** (where each variable was [[Variable standardization|standardized]] and summed to form the scale w/ [[Cronbach's Alpha]]. They find a value of 0.87).
	1. **How often do you attend religious services?**: 0 = never, 1 = few times a year, 2 = many times a year, 3 = once a month, 4 = 23 times a month, 5 = once a week, and 6 = more than once a week.
	2. **How often do you pray alone?**: 0 = never, 1 = less than once a month, 2 = one to two times a month, 3 = about once a week, 4 = a few times a week, 5 = about once a day, and 6 = many times a day.
	3. **Religious salience or how important religious faith was in shaping your daily life?**: 0 = not important at all, 1 = not very important, 2 = somewhat important, 3 = very important, and 4 = extremely important.
2. **Religion**
	1. Protestant
	2. Catholic
	3. Atheist
	4. Agnostic
	5. Nothing in Particular
	6. Other (Mormon, Eastern Orthodox, Jewish, Muslim, Buddhist, Hindu, and Something Else).
3. **[[Christian Nationalism Scale]]** which is based on the [[Baylor Religion Survey]]. They use a 6-item scale in this paper for the main results, but they also try a 2-item scale as a robustness check and results are largely the same. Each question had 5 responses ranging from strongly disagree to strongly agree with neither agree nor disagree in the middle. Cronbach's alpha is 0.8.
	1. The federal government should declare the United States as a Christian nation.
	2. The federal government should advocate Christian values.
	3. The federal government should enforce strict separation of church and state (reverse coded). 
	4. The federal government should allow the display of religious symbols in public spaces.
	5. The success of the United States is part of God’s plan.
	6. The federal government should allow prayer in public schools.
4. Sex (male/female). Original category included trans identities but had low sample sizes.
5. Race/ethnicity.
	1. White
	2. Hispanic
	3. Asian
	4. Other (Black, Middle Eastern/Arab, Native American, Other)
6. Age (continuous)
7. Region of residence
	1. South
	2. West
	3. Midwest
	4. Northeast
8. Education
	1. Up to 12th grade but no diploma
	2. High school graduate or GED
	3. Some college but no degree
	4. 2-year college degree
	5. 4-year college degree
	6. A postgraduate degree
9. Income (recoded from an ordinal variable with 12 income categories)
	1. Low income: lower than the 25th percentile rank in income
	2. Lower-middle income: the 25th percentile to lower than the median income
	3. Upper-middle income: the median to lower than the 75th percentile rank in income
	4. High income: the 75th percentile rank in income or higher
	5. Refused to answer.
10. Political identity
	1. Democrat
	2. Republican
	3. Independent
	4. Other
11. Political views (measured on a 7 point scale ranging from very conservative to very liberal).
### Model
* Used [[Chained Multiple Imputation]] but results remained the same.
* Used [[Ordered Logistic Regression]] however the parallel line assumption failed.
* As a result, they used [[Ordinary Least Squares Regression]].
* No survey weights used although I do not understand why.

## Criticisms
1. Some strange results from the models concerning the control variables. E.g., the higher your education, the more likely you are to have favorable views of Trump. The more religious you are, the more likely you are to have positive views of both Trump and Biden. Christian Nationalism had no relationship with views on Biden.