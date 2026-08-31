---
title: Predicting Police Misconduct
author:
  - Greg Stoddard
  - Dylan J. Fitzpatrick
  - Jens Ludwig
year: 2024
journal: National Bureau of Economic Research - Working Paper Series
type: Article
study type: Quantitative
sample size:
  - "113768"
sampling frame:
sample location:
  - Chicago
  - New York City
study method:
  - "[[cross-fitting]]"
  - "[[histogram-based gradient boosting classifier]]"
  - "[[random forest]]"
  - "[[regularized binary logistic regression]]"
  - "[[fast and lightweight automated machine learning]]"
  - "[[ROC-AUC]]"
  - "[[Recall]]"
  - "[[marginal value of public funds]]"
study start: "2010"
study end: "2018"
dependent variable(s):
  - Police officer misconduct
main independent variable(s):
hypotheses supported?:
---
[Zotero entry](zotero://select/items/@stoddardPredictingPoliceMisconduct2024)
**Tags**: #machine_learning #police_misconduct #postdoc_signaling_edovo 
## Abstract
Whether police misconduct can be prevented depends partly on whether it can be predicted. We show police misconduct is partially predictable and that estimated misconduct risk is not simply an artifact of measurement error or a proxy for officer activity. We also show many officers at risk of on-duty misconduct have elevated off-duty risk too, suggesting a potential link between accountability and officer wellness. We show that targeting preventive interventions even with a simple prediction model – number of past complaints, which is not as predictive as machine learning but lower-cost to deploy – has marginal value of public funds of infinity.
## Data and Methods
* Chicago data comes from the Chicago Police Department as part of a data sharing agreement, and it cannot be shared publicly. New York City police department data is publicly available, though, and results largely replicated on the NYC data.
* Created counts of: complaints, penalties associated with complaints, uses of force, days worked and days absent, overtime hours worked, arrests, stops, warrants served, awards received, unit assignment history, and history of roles over the past 1 year, 2 years, and 5 years. They also conduct an exercise where they increasingly make the features more *complex* by introducing types of uses of force, count of reasons for absence, etc.
* The outcome is if an officer was involved in misconduct (based on the data of the incident) up to 2 years after the observation period. E.g., if the observation year is 2012, all covariates would reflect data from 2010 - 2012, and the outcome would reflect if the officer was involved in misconduct from 2013 - 2014.
	* Results are robust even if one changes the window to 1 or 4 years.
* There are 2 dimensions in which misconduct is measured. First, is it on-duty misconduct (harm caused while carrying out a policing function like excessive force or wrongful arrest) vs. off-duty harm (e.g., domestic violence, substance abuse)? Second, does one consider only sustained complaints or all complaints? This creates 4 possible outcomes in total. **This is a bit of a weird way to approach this. If I understand the results correctly, you are having the model make predictions for something it was not trained for.**
	* For off-duty misconduct, the model built to predict all complaints is strictly better as it predicts all off-duty and only sustained off-duty complains the best.
	* For on-duty misconduct, it is less clear. Models trained on sustained on-duty complains predict sustained on-duty complaints better and the same for all on-duty complaints.
* They use cross-fitting in lieu of a [[test/train split]] due to sample size issues. From what I understand, they basically use 3 folds and repeat the procedure 10 times. Out-of-sample predictions are generated from the model which was estimated without using that data point. They use gradient boosting (performed the best). **I am not really familiar with this technique so I am not certain how it compares to test/train. It certainly seems interesting, but I worry about data leakage**.
* They use FLAML for hyperparameter tuning. It searches through the hyperparameter space using weighted random samples and chooses new hyperparameter sets based on an estimate of accuracy gain per computation time. It is basically designed to find a good set of hyperparameters efficiently. Robustness tests indicate more involved tuning methods produce similar results.
## Section 3 --> Is Risk Predictable?
* Both on and off-duty misconduct is reasonably predictable. The models are likely picking up a true signal rather than measurement error. Predictive performance is evaluated using ROC-AUC.
* Predictable risk is concentrated in a very small group of officers. Officers between the 0th and 80th risk percentiles only differ by 5 or 2 percentage points (off-duty vs. on-duty) in % with actual misconduct. Officers between the 80th percentile and 100th range from 5% to 30% of 2% to 12%.
* However, the riskiest officers are only responsible for a moderate amount of the total amount of misconduct. Using recall, if one predicts misconduct for the riskiest 5%, then recall is only 22%. The riskiest 10% captures about 36% (on-duty). **Why don't they provide a precision-recall curve?**
* What about measurement error? What if officers with a lot of, e.g., clout, are able to ensure complaints against them are not sustained? Starting in 2017, a DOJ investigation forced changes in policing practices in Chicago. As a result, the number of sustained complaints increased even as the number of complaints and uses of force declined. The authors argue *true on-duty misconduct*, in this period, is more likely to be lead to a sustained complaint.
	* Estimate two models trained on data before and after the intervention. The early model does miss a group of high-risk officers which are identified by the later model. Measurement error causes the model to under-estimate risk for a group which otherwise would have been flagged as high risk. However, the early model is still picking up on high risk officers. Measurement error is not fatal. **I would have liked a better explanation and visualization of the predictive results, here. What threshold do they use for flagging someone, for example?**
	* The result does not seem explainable by [[data drift]] either because both the early and late model are pretty comparable in predictive performance in regards to **off-duty misconduct** suggesting the data-generating process did not change appreciably. 
	* They do a weird robustness check where they randomly flip the outcome (y = 1, sustained misconduct) to 0 so base rates are similar across time periods and find results do not change (suggesting the model is not simply benefiting from having more cases to learn from). **I am not convinced this is a great robustness check as it is likely not random which misconduct cases would not have been sustained absent the policy change.**
## Section 4 --> What predicts risk?
* First, even very simple model features do a reasonable job of prediction. For on-duty misconduct, recall (while flagging the riskiest 5%) is nearly indistinguishable regardless of which set of predictors were used (simple, intermediate, complex). For off-duty misconduct, it is only a few percentage points different.
* Including the number of prior non-sustained complaints greatly improves model performance (although this raises ethical issues).
* For identifying the riskiest officers, simple heuristics such as having a past record of complaints can be very useful (i.e., no need to make it very complicated nor does having singular large or serious sustained complaints prove more predictive).
## Section 5 --> How can the model be implemented?
* It is costly to build an ML model and put into production and have it guide decisions. What if a simpler model could be used which has slightly worse accuracy but is also much cheaper? By simply flagging the top 5% of officers with the most complaints in the past 2 years, this baseline model does worse than ML but not terribly given how simple it is. This may be particularly helpful for small departments who may not be able to afford building a ML model (and who may not have enough data to build a quality model).
	* Robustness checks which use a sub-sample of Chicago data leads to much worse performance confirming this result. Another option might be to build a model for multiple departments using pooled data (although one would need to verify the model performs equally well across departments).
* Are the models simply predicting which police officers are *the most active*? I.e., every officer has similar levels of risk of misconduct so it is only the most active officers who garner a penalty. This may discourage officers from engaging in the productive aspects of their jobs. To test this, they estimate a model where the risk score is the outcome and the independent variables are: officer unit, officer role, policing activity (test a variety of model specifications involving different definitions of beneficial police activity). They extract the residuals from this model and use them... **somehow. I don't completely understand this section. I am not sure how they use the residualized risk scores to flag individuals**. Additionally, supplementary results suggest police activity and unit assignment only explain a moderate amount of the variation in misconduct behavior suggesting being active does not mean one also has more misconduct (and vice versa). I.e., there appears to be officers who constantly engage in misconduct regardless of their circumstances.
* Is there bias in predicting based on race? For on-duty misconduct, the models seem well-calibrated across race. For off-duty misconduct, Black officers appear to be flagged more often although this is likely due to the higher rate of off-duty misconduct among Black officers (statistical discrimination). Why this is the case and is it real? Hard to say.
## Section 6 --> What do we do with officers flagged as being at-risk?
* Supervisor meets with officers to get them to reflect on past decision making.
* Behavioral science interventions designed to *slow down* officer decision making seem to help.
* Many officers who were at high risk for on-duty misconduct were also at high risk of off-duty misconduct (although not necessarily vice versa). Thus, interventions designed at improving officer wellness (e.g., therapy to help deal with PTSD) may be useful.
* It also suggests targeted and different interventions may be necessary depending on if you are at risk for on-duty, off-duty, or both on-duty and off-duty misconduct.
## Section 7 --> Policy evaluations incorporating costs and benefits
* It is not quite a cost-benefit analysis. Basically, the numerator is the willingness to pay among impacted or affected populations. The denominator is the costs in public funds to implement the policy minus the savings in future expenditures of public funds.
* Using the very simple heuristic model from section 5, the value is basically infinite because the cost of implementing such a model is so incredibly low. The MVPF for a machine learning model is harder to estimate because of uncertainties around the cost to implement, differential efficacy based on the jurisdiction, and how much more predictive it is than the simple heuristic (their very rough estimates indicate it would take about 5 years for this approach to pay for itself and basically have infinite value). **They only calculate the upfront cost of building and deploying the model and not maintaining it. They calculate savings as savings from prevented lawsuits and misconduct investigations.**
	* This approach compares ML and the heuristic to the random assignment of interventions.
	* What if you compare these approaches to another heuristic which targets interventions to those officers with the highest number of **sustained complaints**? Well, it appreciably increases the amount of time it would take for these approaches to become *profitable*, but these approaches would be still worth pursuing on long enough time horizons (e.g., 3 years for the heuristic).
* **This section, to be honest, appears very assumption-driven. The costs to create these tools is based on the authors' prior experience. It is assumed these tools could reduce complaints by 20%**.