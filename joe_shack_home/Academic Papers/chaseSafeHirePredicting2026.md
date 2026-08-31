---
title: "Safe to Hire: Predicting Recidivism Risk for Job Candidates with Criminal Records"
author:
  - Elizabeth C. Chase
  - Shawn Bushway
  - Bethany Saunders-Medina
  - Lane F. Burgette
year: 2026
journal: Statistics and Public Policy
type: Article
study type: Quantitative
sample size:
sampling frame: "[[Criminal Justice Administrative Records System]]"
sample location:
  - Arizona
  - Florida
  - Minnesota
  - Oklahoma
  - North Carolina
  - Texas
  - Wisconsin
study method:
  - "[[Cox proportional hazards model]]"
  - "[[Bayesian Additive Regression Tree]]"
  - "[[Generalized Boosted Model]]"
  - "[[Classification and Regression Tree]]"
  - "[[time-dependent AUC]]"
  - "[[calibration plot]]"
study start: "1992"
study end: "2021"
dependent variable(s):
  - Time to next conviction
main independent variable(s):
hypotheses supported?:
---
[Zotero entry](zotero://select/items/@chaseSafeHirePredicting2026)
**Tags**: #human_vs_algorithm #job_hiring #machine_learning #public_policy #recidivism #postdoc_signaling_edovo 
## Abstract
In the United States, the use of criminal history information in employment decision-making is ubiquitous. However, employers' decision-making about job candidates' criminal records is often nontransparent and inconsistent, with disproportionate negative effects on Black and Hispanic Americans. Here, we consider whether statistical models can produce a more accurate, interpretable, and fair assessment of the recidivism risk of job candidates with criminal records relative to current approaches. We review existing approaches and policy guidance on the use of criminal records in employment decision-making. Then, using data from seven states from the Criminal Justice Administrative Records System (CJARS), spanning 1992–2021, we build a Cox proportional hazards model to predict the risk of recidivism based on a job candidate's criminal record. We assess the predictive performance, fairness, and generalizability of this model. We find that our candidate model outperforms some existing approaches, although challenges remain in the domains of fairness and usability in practice.
## Research Questions
1. How is criminal history information currently used in employment decision-making?
2. Can a better model for decision making be used when assessing recidivism risk for employers?
3. How can forecasting of recidivism risk be improved?
## Research Question 1
* The USA has an open criminal records system allowing anyone (I think) to access someone's criminal history. As a result, the [[Equal Employment Opportunity Commission]] regulates the use of criminal history for employers. They offer recommendations on what to consider (e.g., only convictions and not arrests, time since last conviction, age at last conviction, number of convictions, relevance of the crime to the job, and efforts at rehabilitation). Protected categories like race and sex should not be considered. Applicants are entitled to know why if they are excluded due to criminal history. If the use of criminal history results in disparate impact for a protected category, then there must be a strong case that the criminal history information is directly job-related. Additionally, there must not exist an equally effective but less discriminatory alternative. Disparate impact is assessed using the $\frac{4}{5}$ rule wherein if hiring rates for a protected group are less than 80% for another group, there is disparate impact.
* This has led to a standardization in the use of criminal history. Broadly, the job is offered and then a criminal background check is initiated at which point a black-box screening process (e.g., could be an outside company with its own algorithmic approach, could be individualized decisions made by the employer, HR, or company legal counsel) is employed. If the individual fails the screening, the applicant is informed, and they are given the opportunity to challenge the record and/or provide more information. An individualized assessment is conducted at which point the job offer goes through or is rescinded. **The modeling approach used in this paper would be employed in lieu of the black-box screening process**.
* There are data quality issues in criminal background checks. For one, they include arrests but not information on how arrests led (or not) to a conviction. There is no information on incarceration or rehabilitation. Due to the heterogeneity in criminal legal systems across the USA, the same criminal behavior may have dramatically different representations in the background check. Additionally, HR professionals have trouble parsing the jargon of background checks.
## Data
### Advantages
* Researchers can use incarceration data to obtain more accurate estimates of recidivism risk (since risk is 0 while incarcerated). Not including this information risks biasing estimates downwards (i.e., one's estimates of risk are too low) because an individual who was incarcerated may have committed crime while not incarcerated.
### Limitations
* CJARS does not have data on all 50 states. Therefore, individuals who migrate out of the focal state may have some criminal legal system interactions not captured.
* Incarcerations and convictions are not linked --> Incarcerations are matched to the most recent conviction and any gaps between conviction date and incarceration date are assumed to be spent incarcerated (possibly in county jail).  **I am not quite sure how this works. What happens when you have an incarceration spell which is closer in time to a past conviction?**
* Convictions and criminal episodes are not linked --> To link convictions with criminal episodes, all convictions within a 30-day window get classified as being part of a single episode.
### Sample construction
* The final dataset is at the individual-criminal episode level. Each row has information on: number of resulting convictions, crime types from the episode, time spent incarcerated, prior convictions, prior crime types, prior incarceration time, time spent in free society before next offense, censoring indicator to indicate whether another recidivism event was observed during follow-up or not. Then they kept individual-criminal episodes where the individual was between 15 and 60 (prime working age range).
* The full data cleaning can be found in the Appendix. Some questions I have:
	* What date column did you use for adjudications/convictions?
	* How did you determine if an incarceration sentence was ongoing (thus does not have an exit date)?
	* Interesting that they used a modeling technique to impute missing incarceration exit dates.
* One interesting thing they do is they select a single crime episode per individual. Including all conviction episodes would upweight individuals with extensive criminal histories (and high recidivism rates). **Future work should explore the statistical properties of this approach**.
	* One can randomly sample among records.
	* The authors choose to to have their sample be representative of those with a criminal record looking for work. Records (instead of having an equal chance of being selected) are instead given different weights proportional to the time spent in free society. The idea being that when an individual is not actively involved in crime, they are probably more actively looking for work.
## Data and methods
* Age at offense, age at first conviction, age, age squared, offense involved a felony or misdemeanor conviction, crime type, time spent incarcerated, number of prior felonies, number of prior misdemeanors, number of prior convictions in each crime type, number of prior incarcerations, total amount of time spent incarcerated, interactions between age and prior record.
* See the study methodology properties for models estimated and performance criteria.
* Estimate probabilities of recidivism from 1-year out to M - 1 years out (where M is the number of years under observation).
* The benchmark model was a binary prediction based on whether an individual had a felony conviction, violent offense, or both in the past 10 years.
### Fairness and portability
* They considered fairness across race/ethnicity (White, Black, Hispanic) and sex (male, female).
* They calculated race and sex stratified AUC and calibration plots.
* They also investigated feature bias and label bias.
	* Feature bias is when predictors have different effects on the outcome depending on race and/or sex. E.g., is the effect of having a previous felony different for Black men vs. White men? If there is a difference, it could be due to differences in the measurement or true differences in the impact of the predictor on the outcome. **Is this bias? I am having hard time understanding why this is considered bias?**
	* Label bias is when the outcome means something different for members of different groups. E.g., a Black man's criminal behavior is more likely to result in a conviction than a White man's criminal behavior.
		* To assess feature bias, they fit a Cox proportional hazards model where they include a main effect of race and sex and the interact each predictor with race and sex to see if there are interactions. **Couldn't you just compare coefficient estimates from the stratified models?** Specifically, they are curious as to how predictive performance changes and if particular predictors changed as a result of adding race/sex.
		* To assess label bias, they estimate a model only felony offenses (with the idea being that more serious offenses are less subject to bias).
* They also investigated portability. I.e., does the model perform equally well in different states as well as across time? To assess state portability, they estimate a model using 6 states and assess performance on the held-out state (for each state). To assess temporal portability, they estimate (and test?) models in 5-year groupings based on year of conviction to see if performance changes over time (with cohort in some sense?).
## Results
* Recidivism rates are quite low. Even for the states with the highest recidivism rates, 70% of individuals had not recidivated nearly 10 years after the focal criminal episode. The models reflect this by having relatively low estimates of recidivism. As more time passes without a conviction, the predicted (and actual risk) continues to decline.
* CART, GBM, and Cox all performed very similarly to one another. GBM tended to perform the best while Cox performed the worse. Predictive power declined the further out one went (i.e., the risk of someone recidivating given their last offense was 1 vs. 9 years ago). I.e., the longer one went without being re-convicted, the less useful their prior criminal record was in forecasting future criminal involvement. Importantly, all models vastly outperformed the baseline model.
* They also estimated a **reduced form model** which did not include incarceration information and crime type to more accurately capture a background check. The model performed worse but only marginally so indicating this approach can be useful to employers even without the full information. However, the data was constructed using incarceration data so these results may not be fully applicable.
### Fairness Results
* Stratified models all tended to perform generally equally well (although women had much higher variability likely due to smaller sample sizes). Calibration plots were a little optimistic, surprisingly, for Black men (likely reflecting Black men are re-convicted more quickly than otherwise anticipated). However, all models tended to perform equally well across groups.
* Models which included race and sex had slightly better predictive performance and calibration plots. But nothing major.
* The main effects of race and the interactive effects of race were all statistically significant indicating feature bias (**not sure how?**).
* In regards to label bias, the coefficient estimates were generally the same between all convictions and just felony convictions. Predictive performance is also broadly similar. However, the calibration plot is quite different based on race and sex.
* **Criminal history alone cannot account for differences in recidivism rates by race and sex**. However, the models employed do a much better job at mitigating these problems than the baseline.
### Portability Results
* Results seem to generalize quite well across states and time (although the youngest and oldest cohorts had slightly worse calibration plots and the oldest cohort had worse predictive performance).
## Limitations
* Data problems still exist in background checks (spurious convictions and unclear jargon).
* It is not clear how to translate probabilities into binary yes/no decisions (or relative risk compared to other candidates).
* Bias was not assessed for other racial groups and gender identities.
* We need better baseline models to compare to.
* The modeling approach likely needs to be tailored for predicting recidivism for specific crime types relative to the job.
* The model, if deployed, would need to consistently checked for predictive performance and fairness.
* Appropriately assessing recidivism risk is hard given the list of predictors currently deemed acceptable largely because systemic racism affects everything. Unless you can control for this, the predictors will reflect this bias (i.e., Black individuals have a higher base risk of being convicted).
	* Other approaches to limiting bias seem unsatisfactory (e.g., predictions can only differ so much for individuals from predicted groups) because they hurt overall model performance. Other approaches like ensuring equivalent model calibration might not hurt **overall** model performance so much but would hurt model performance for some groups at the expense of others. It also invites all sorts of legal problems.
	* The best (unsatisfying?) approach is to detach risk assessment from risk-informed decision making. Statisticians can develop optimal risk assessment models and quantify the disparity. Decision makers would then need to agree on how to use these predictions in the light of the disparity.
* Future work should consider alternative modeling schemes to deal with the sampling issue they devised (allowing the use of the whole set of criminal episodes).
* Other modeling techniques could be employed, both more sophisticated and less sophisticated (e.g., logistic binary regression).
* More data can be incorporated on things like rehabilitation.
* It isn't clear that forecasting recidivism risk is a good proxy for job performance.