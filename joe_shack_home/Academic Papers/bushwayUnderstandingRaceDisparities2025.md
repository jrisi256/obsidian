---
title: Understanding Race Disparities in Criminal Court Outcomes
author:
  - Shawn Bushway
  - Andrew Jordan
  - Derek Neal
  - Steven Raphael
year: 2025
journal: The Russell Sage Foundation Journal of the Social Sciences
type: Article
study type: Review
sample size:
sampling frame:
  - "[[State Court Processing Statistics]]"
  - "[[National Corrections Reporting Program]]"
sample location:
study method:
  - "[[quantile regression]]"
  - "[[Ordinary Least Squares Regression]]"
  - "[[Outcome tests|Outcome test]]"
  - "[[Fairness tests|Fairness test]]"
  - "[[steady-state simulation]]"
study start: "2019"
study end: "2019"
dependent variable(s):
  - Pretrial Detention Size
  - Probation Size
  - Parole Size
  - Prison Size
main independent variable(s):
hypotheses supported?:
---
[Zotero entry](zotero://select/items/@bushwayUnderstandingRaceDisparities2025)
**Tags**: #public_policy #racial_disparity_courts #review #simulation 
## Abstract
We construct a framework that defines optimal outcomes in criminal courts, and we use this framework to interpret and organize the existing literature on racial disparities in pretrial detention, sentencing, and community corrections outcomes. Existing research indicates that some actors within courts and within the agencies that implement the sentences that courts impose make decisions that are contaminated by racial animus or racially biased assessments of the recidivism risks posed by some offenders. However, the most important sources of racial disparities in case outcomes are numerous practices, regulations, and laws that are too punitive—that is, their social costs are likely greater than any derived social benefits. Since minorities, especially Blacks, face arrest at much higher rates than Whites, they bear large disparate impacts from such policies.

## Notes

### Introduction
* Racial bias is being defined in the context of court proceedings.
* The outcome of a criminal case is racially biased if the outcome is not socially optimal (costs outweigh the benefits), and it contributes to racial disparities in case outcomes. Concerns around *proportionality* or *fairness* will not be considered.
* Precisely calculating exact costs and benefits and hard. The authors' main point existing practices in the USA generate punishment costs far in excess of any crime-prevention benefits. Additionally, minority groups (particularly Black individuals) bear much of these costs (because they are disproportionately involved in the criminal legal system).
* **3 types of racially biased outcomes**
	* First, assume a comparable group of defendants who face the same charge and same socially optimal sentence. If average outcomes are different for different racial groups, this is evidence of racial bias. It means one group is receiving sentences that are too harsh or too lenient.
	* Second, the law may not permit socially optimal decisions. Two groups of defendants (with the same socially optimal sentence) may not be permitted to be given the same sentence. If a racial group is over-represented in cases which require harsher than optimal punishment (or more lenient than optimal), this is **structural racism**.
	* Third, assume the law broadly requires outcomes for all defendants which are too lenient or too severe (relative to socially optimal outcomes). If racial minorities are more likely to appear in court, just generally speaking, this produces a form of racial bias which is also **structural racism**; even though the courts themselves are producing outcomes independent of defendant race.
	* **Joe note**: Under this definition, if Black defendants, on average, had *harsher* socially optimal sentences, this would not be racial bias?
* Math:
	* $j$ indexes cases while $i$ indexes a specific defendant.
	* $D$ is the outcome or decision of a specific case (e.g., verdict, sentence, supervision conditions).
	* $X^*$ is the set of case and defendant characteristics which determines the target outcome.
	* $X^{law}$ is the set of case and defendant characteristics the law requires/encourages to be considered when deciding the outcome.
	* $\widetilde{X}$ is the set of case and defendant characteristics observed by the researcher.
	* $R$ is the categorical variable denoting the race of defendant $i$ in case $j$.
	* $F(D|X^*)$ is the distribution of outcomes produced by a court conditional on relevant case and defendant characteristics.
* The authors note in their framework racial bias may exist (structural racism) even when defendants facing comparable charge receive similar sentences (regardless of race). However, many researchers are concerned with this problem which is defined as $E(D|X^*) = E(D|X^*, R)$. I.e., knowing an individual's race should not change outcomes.
	* **Assumption 1**: Courtroom actors see all elements of $X^*$ and $X^{law}$.
	* **Assumption 2:** $\widetilde{X} \in X^* \cup X^{law}$.  Researchers see a subset of information. In reality, researchers really test: $E(D|\widetilde{X}) = E(D|\widetilde{X}, R)$. Why might this relationship not hold?
		* **1)** Racial animus on the part of courtroom actors.
		* **2)**$\widetilde{X}$ may not be a good approximation of $X^*$ --> Judge uses defendant's residence as an aggravating factor (correlated with race, form of statistical discrimination), but the researcher does not have access to this data.
			* If the judge uses this information correctly, it will create racial differences in outcomes for defendants, but it will be socially optimal. If they are not using the information correctly, it will also create racial disparities that are socially harmful.
* **Alternatives**
	* Incomplete information is the source of bias in court outcomes, and it leads to socially harmful decisions. Authors do not necessarily disagree but argue disparities in quality/amount of information by race would also be a form of structural racism (e.g., minority defendants having worse quality defense attorneys, on average).
	* What about implicit bias? The authors don't find this a compelling argument to explain racial differences. Even if it did, their framework could still be used to analyze disparities and deviations from socially optimal outcomes. The policy recommendations might differ, of course.
	* They are specifically not trying to address racial bias in policing.

### Racial bias in various court proceedings
* **Prosecutorial Screening** --> Prosecutors have basically unlimited discretion as to what they want to charge. Not a lot of research but what evidence we do have suggests not a lot of racial bias in this stage.
* **Pretrial custody** --> Some evidence suggests Black defendants are less likely to be released without any conditions. The authors argue the main driver of disparities, though, in pretrial detention are due to the differential ability to pay bail for Black vs. non-Black defendants. Because financial capacity is not really related to flight/safety risk **and** because because bail provides only weak incentives for good behavior, cash bail is socially harmful and structurally racist.
	* **[[Outcome tests]]**: One strand of literature looks at differences in rates of pretrial misconduct by race among those released. Researchers generally find White defendants have a higher likelihood of being rearrested meaning judges hold Black defendants to a higher standard. However, this research is plagued by the [[infra-marginality problem]]. I.e., assume every defendant $i$ has some likelihood of recidivating $p_i$. Assume judges know $p_i$ and use a simple decision rule where an individual is released if $p_i < \overline{p}$. Rates of recidivism may differ by race simply due to different distributions of $p$ by race. Researchers must isolate comparable cases (i.e., someone was released vs. someone was not) to conduct valid outcomes test (to generate plausible counterfactuals) but even this is problematic.
		* **Issue 1**
			* $E(\Delta|r, v) \leq T(z, r, v)$
			* $T(z, r, v) = c(z, r, v) + \lambda(z, r, v) + \beta(z, r, v)$
			* $\Delta$ is the cost incurred to society of releasing the defendant.
			* $r$ is the race, $v$ is a case or defendant characteristic observed by the judge but not by the researcher, $z$ is the judge.
			* $T()$ is the judge's total assessed cost of detainment. $c()$ is the judge's assessed societal cost of detainment; $\lambda()$ is the mistake made by the judge in assessing cost, and $\beta()$ is the judge's own personal factors which influence the decision to detain or not.
			* If $T(z, r, v) = T(z, v)$, then there is no racial bias. However, there can be significant racial differences in average post-release outcomes among comparable defendants even when this condition holds and $v$ is independent of $r$. How can this happen? Suppose past discrimination by police inflates criminal records of Black defendants relative to non-Black defendants who engaged in the same illegal behavior. It's reasonable to assume that among defendants facing the same expected outcome, Black defendants will have lower expected recidivism risk if released.
		* **Issue 2**: Judges do not determine release outcomes (directly). They determine release conditions. These decisions are made very quickly in somewhat high stress situations many times without a lot of information. Therefore, knowing that there are racial differences in violation rates tells us very little about how racial bias impacts decision making. Differences may arise primarily due to institutional practices of bail setting which disadvantages poor defendants who most likely a minority racial group.
	* **[[Fairness tests]]**: Authors do not think these tests work for their study purposes.
		* $$E(S|\widetilde{X}, R = r, Y(1) = 1) = E(S|\widetilde{X}, R = r', Y(1) = 1) \tag{1}$$
		* $$E(D|\widetilde{X}, R = r, Y(1) = 1) = E(D|\widetilde{X}, R = r', Y(1) = 1) \tag{2}$$
		* where $S$ is a risk score (e.g., how risky is it to release this defendant), $D$ is the release decision, and $Y(1) = 1$ is a potential outcome indicating if this defendant is released, they will re-offend.
		* The equations state that among defendants with similar $\widetilde{X}$, who would re-offend upon release, the expected risk score and the release decision should not be different for different racial groups. Even if you can observe plausible counterfactuals for $Y(1)$ for defendants who are not released $D = 0$, this is not a good test.
		* Assume a defendant is given $S$ and $\widetilde{X} = X^{*}$.
		* Assume conditional on $X^{*}$, the probability of misconduct is independent of race.
		* Assume $S(X^{*}) = P(Y(1) = 1 |X^{*}) = P(Y(1) = 1|X^{*}, R)$ meaning the risk score equals the true probability that $Y(1) = 1$ given $X^{*}$ for all racial groups.
		* Assume, the judge releases a defendant if their risk score is below some cutoff $\overline{S}$.
		* As long the distribution of $S$ is different for different racial groups, the outcomes will always violate the fairness criteria state above in equations 1 and 2.
* **Charge decisions and plea bargaining**: Racial differences in time served in prison among comparable defendants driven almost entirely by prosecutors. Racial differences in crimes committed and criminal history drive much of the observed disparity, as well.
	* The growth in mass incarceration was primarily due to how courts dealt with arrested offenders and convicted offenders. I.e., someone arrested and/or convicted in 1960 for crime *x* faced much lower odds of being incarcerated for that offense. Courts started to push harder for incarceration as a punishment. This resulted from the passing of more punitive sentencing laws.
	* **Incarceration and Public Safety**
		* How does incarceration affect the individual? **1)** They are incapacitated. **2)** They are aging and become less likely to recidivate upon release simply due to this fact. **3)** Prisons can make age-specific individuals more or less likely to recidivate post-release through such mechanisms as: rehabilitation and therapy, skills and job training, specific deterrence, *schools for criminals*. Research suggests that incarceration in the USA largely incapacitates and that's about it. Incapacitating individuals does reduce their criminal activity (almost logically).
		* However, how do incarceration rates affect overall levels of crime in society? Individual-level affects cannot account for spillover effects (e.g., general deterrence, criminal replacement, other criminals commit more crime due to increase opportunity). Most research in the USA indicates that mass incarceration had incredibly limited returns in violence and crime prevented. I.e., each extra person you incarcerate leads to fewer and fewer expected crimes prevented.
* **Community supervision**: The incentive structure for community correctional officers incentivizes preventing recidivism at all costs leading to socially harmful punishment.
	* **Parole boards, parole supervision, and probation supervision**: Not much research on racial disparities. However, the restrictions placed on parolees tends to be too harsh, leads to many people being re-incarcerated who otherwise would not have offended, and disproportionately harms Black individuals (who are disproportionately under community supervision). It is possible there is some differential treatment of individuals (e.g., Black individuals are more likely to be re-incarcerated for a technical violation), but these community supervision programs, the authors argue, mostly reflect structurally racist practices. Technical violations are weak signals of future propensity to re-offend.
### Simulation
* Most research shows court actors do not assign wildly different average treatment outcomes to comparable defendants from different racial groups. No amount of individual-level reforms (e.g., anti-bias training) will move the needle. At best, they would produce small reductions in racial disparities. True change must be achieved through changing law and policy especially laws and policies which shape the discretion of courtroom actors.
* **Policy simulation**: **1)** All nonviolent offenders who are not on probation or parole must be released pretrial (do not condition release on financial capacity). **2)** Eliminate all technical parole revocations. **3)** Reduce prison admission rates by 50% for nonviolent offenders (diminishing returns the more people are incarcerated, trying to get closer to the ideal). These are very **limited reforms**, the authors designed it that way. They also do not touch violent crimes (thus limiting any potential costs to public safety).
	* Essentially, they define 32 states a defendant can exist in (e.g., non-felony defendant on probation, felony defendant released pretrial on parole). They use various data sources to calculate the probability of transitioning between different states. They then calculate how the population sizes would change if their reforms were introduced on pretrial detention population size, probation population size, parole population size, and prison population size (broken down by crime type). They essentially find pretty sizable reductions in pretrial detention population size (~700,000 to ~300,000). Probation and parole offset each other leading to only a slightly lower total community supervision population size. The prison population size declines moderately from ~1,100,000 to ~800,000.