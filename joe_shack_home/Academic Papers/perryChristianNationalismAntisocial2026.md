---
title: Christian Nationalism, the Antisocial Gospel? Attitudes on Charity and Justice in the Kingdom of God
author:
  - Samuel L. Perry
  - Blake Victor Kent
  - Phineas J. Bonner
  - Joshua B. Grubbs
year: 2026
journal: Journal for the Scientific Study of Religion
type: Article
study type: Quantitative
sample size:
  - "704"
sampling frame:
  - "[[Public Discourse and Ethics Survey]]"
  - "[[YouGov]]"
sample location:
  - USA
study method:
  - Survey
  - "[[Ordinary Least Squares Regression]]"
  - "[[Multinomial logistic regression]]"
  - "[[Cronbach's Alpha]]"
study start: 2019/08
study end: 2021/02
dependent variable(s):
  - Best way to bring about the Kingdom of God
main independent variable(s):
  - Christian Nationalism
hypotheses supported?: Yes
---
[Zotero entry](zotero://select/items/@perryChristianNationalismAntisocial2026)
**Tags**: #paper_belief_demons_trump_support #christian_nationalism #views_on_kingdom_of_god
## Abstract

The Kingdom of God is a key motif in the teachings of Jesus. Many Christians, including those subscribing to Christian nationalism, believe they have a responsibility to “build” the Kingdom here on Earth. But what would this entail? Using original survey data, we ask Christians whether various actions—acts of charity or justice, personal devotion, attending church, evangelism, or promoting theocratic political arrangements—make God's Kingdom more present. We initially find that Christian nationalism is positively associated with affirming all proposed actions in absolute terms. Yet when we force respondents to choose which option best reflects their view about making God's Kingdom present, Christian nationalism corresponds to deprioritizing acts of charity or justice, while prioritizing electing Christians to power, changing laws to reflect biblical principles, and engaging in evangelism. Our findings are an initial step toward understanding the dynamics at play in American Christians' conceptions of the Kingdom of God.

**Research Question**: According to American Christians, which set of actions would best bring about the Kingdom of God?
## Dependent Variables

1. How much do you agree that the following actions are ways of making the Kingdom of God more present on Earth? (1 = strongly disagree, 5 = strongly agree)
	1. Performing acts of charity or justice.
	2. Following God individually.
	3. Participating in a church or religious community.
	4. Sharing the message of God with others.
	5. Changing laws to reflect Biblical principles.
	6. Electing Christians to positions of influence.
2. Using these same measures, participants were asked to select which one(s) were most closely associated with their view of how to make the Kingdom of God more present on Earth.
## Independent Variables

* They used a modified version of the [[Christian Nationalism Scale]]. See page 4 for their references.
	* The federal government should declare the United States as a Christian nation.
	* The federal government should advocate Christian values.
	* The federal government should enforce strict separation of church and state.
	* The federal government should allow the display of religious symbols in public spaces.
	* The success of the United States is part of God’s plan.
	* The federal government should allow prayer in public schools.
	* **Extra item**: I consider founding documents like the Declaration of Independence and the US Constitution to be divinely inspired.
	* They dropped the strict separation of church and state (provide a reference) since it lowered reliability. After dropping this variable from the construct, they achieved a Cronbach's Alpha of 0.93. A footnote indicates results do not change even when including it, though.
* **Controls**:
	* Political ideology: (1 = very liberal, 5 = very conservative).
	* Political partisanship: (1 = strong Democrat, 3 = independent/other, 5 = strong Republican).
	* Religious commitment: (1 = never attend worship, 6 = more than once a week).
	* Religious identity: (Born-again or Evangelical Protestant - reference; non-evangelical Protestant; Roman Catholic; other Christian including Latter-Day Saints and Orthodox Christians).
	* Age: Continuous.
	* Education attainment: (1 = less than high school, 6 = postgraduate degree).
	* Race: (White - reference; Black, Hispanic, Other).
	* Sex: (Female - reference; Male)
	* Household income: (less than $30,000 - reference; $30,000 - $49,999; $50,000 - $79,999; $80,000 or more, did not report).
	* Region: (Northeast - reference; Midwest; South; West).
## Methods

* Use OLS to estimate (for each of the 6 items) the association between Christian Nationalism and support for each action as a means of achieving the Kingdom of God.
* Then, they use multinomial logistic regression to estimate how much more likely being more Christian Nationalistic is to make you support an action relative to performing acts of charity or justice (using the forced choice question model). **Joe Note**: This seems more like they estimated a series of binary logistic regressions. I think they only present results when performing acts of charity is the reference category.
* Use [[Variable standardization]].
* It appears as if the survey is longitudinal (they use Wave 1 for controls and Wave 7 for outcomes), but they mention in their limitations section that it is not? **Joe note**: Missed opportunity to assess how changing Christian Nationalism beliefs, within person, affected change in beliefs if indeed the survey was longitudinal.
* YouGov methodology: Using a random sample from the [[American Community Survey]], they matched respondents in their panel who most resembled participants in the ACS based on several sociodemographic characteristics. Sampling weights are then employed to ensure the survey sample is nationally representative across age, sex, race, education, and census region.
* **Joe note**: Why aren't survey weights used? I understand you don't necessarily have to use them in the modeling. It would be nice to have a little discussion at least.
* Wave 1 = 2,519 which, by Wave 7, has shrunk to 1,257 due to attrition. They then filter to only include Christians thus shrinking the sample further to 704.
## Results

* Correlational results between Christian Nationalism and the 6 outcome variables indicate:
	* Very weak correlation between Christian nationalism and performing acts of charity/justice.
	* Moderate correlation between Christian nationalism and: following God individually, Church participation, and sharing God's message.
	* Strong correlation between Christian nationalism and: changing laws to follow Biblical principles and electing Christians to power.
* OLS results indicate the more Christian Nationalistic someone is, the more likely they are to endorse all 6 items. However, coefficient sizes are weakest for charity/justice and following God individually. Church participation/sharing God's message have modest sizes. Biblical laws and Christian politicians had the largest coefficients. All results were high statistically significant.
* Figure 2 presents a descriptive look at the second operationalization of the dependent variable. They find the most Christian Nationalistic individuals were very unlikely to support acts of charity vs. justice which is the largest difference between them and the least Christian National individuals. Following God individually and participating in Church were roughly equivalent. Sharing God's message was moderately more important for Christian nationals. Biblical laws and electing Christian were more important, but even the most Christian national influences had a relatively low % of endorsing these items.
* Figure 3 presents the results of the multinomial model. The more Christian Nationalistic someone is, the more likely they are to endorse biblical laws and electing Christians relative to charity and justice. God's message had the largest coefficient size. **Joe note**: Confused because the 95% [[confidence intervals]] suggest the results are barely statistically significant while the tables suggest the results are highly statistically significant.
* **Important limitation**: They did not have the statistical power to determine if Christian Nationalism had a different relationship to the outcome variable when interacted by race.
* **Joe note**: I might quibble with the way they frame their results. The headline findings are that Christian Nationals do not view acts of charity and justice as a means of achieving the Kingdom of God whereas spreading the message of God is. Enacting Biblical laws and electing Christian politicians have relatively little support even among the most Christian Nationalistic people. However, if one does support those things, it's incredibly likely you are a Christian National.