---
type: [Article]
author: [Skyler J. Cranmer, Bruce A. Desmarais]
journal: [Political Analysis]
date: 2017/04
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Skyler J. Cranmer, Bruce A. Desmarais
* **Title**: What Can We Learn from Predictive Modeling?
* **Date of publication**: 2017/04
* **Journal**: Political Analysis
* **Volume**: 25
* **Issue**: 2
* **Pages**: 145-166
* **URL**: [https://www.cambridge.org/core/journals/political-analysis/article/abs/what-can-we-learn-from-predictive-modeling/DA6161B358A86146B2DB3E5025461554](https://www.cambridge.org/core/journals/political-analysis/article/abs/what-can-we-learn-from-predictive-modeling/DA6161B358A86146B2DB3E5025461554)
* **Tags**: #comps_exam, #plsc_597_machine-learning, #prediction_theory
* **PDF Attachments**:
  * [cranmerWhatCanWe2017.pdf](zotero://open-pdf/library/items/CIFL85Y8)

## Abstract

The large majority of inferences drawn in empirical political research follow from model-based associations (e.g., regression). Here, we articulate the benefits of predictive modeling as a complement to this approach. Predictive models aim to specify a probabilistic model that provides a good fit to testing data that were not used to estimate the model’s parameters. Our goals are threefold. First, we review the central benefits of this under-utilized approach from a perspective uncommon in the existing literature: we focus on how predictive modeling can be used to complement and augment standard associational analyses. Second, we advance the state of the literature by laying out a simple set of benchmark predictive criteria. Third, we illustrate our approach through a detailed application to the prediction of interstate conflict.

## My notes

### Inferential Modeling

The statistical model is constructed as an operationalization of a theoretical model. The coefficients are the objects of interest which is to say the statistical model itself is the object of interest. We use the data to learn about the statistical model -> minimize bias to produce most accurate coefficients.

### Predictive Modeling

The objects of interest are the variables rather than the parameters. We use the available data to produce the best possible predictions of the outcome variable. It doesn’t matter if the model used is a close operationalization of a causal theory because the only metric of importance is predictive performance -> minimize bias and variance to optimize empirical precision.

Prediction is useful! [[Cross-validation]] (randomly test on held out partitions and report out mean error), [[train/test]], [[machine learning]] to learn a model not from a theory-informed perspective but from a data-informed perspective. It can uncover patterns which may not have been obvious or may be unintuitive.

- Predictive modeling and machine learning allow for the observation of nature in a systematic and principled way.
    
- Predictive models can help refine measures (finding new measures or finding the best way to operationalize a measure) and help refine explanatory statistical models (how parsimonious can the model be made, identify [[model misspecification]] because they’ll be poor predictors even when over-fitted ones).
    
- Predictive modeling can help test the quality of an explanatory model against more robust null models or a competing theoretical model.
    
- Predictive modeling can tell us how well an explanatory theory is capturing the phenomenon of interest, and it can establish an upper bound on what can be further learned -> much work remains to be done or the outcome exhibits a high amount of noise and not much natural signal (largely complete explanatory model but high degrees of imprecision in our ability to measure the relevant variables produce high stochasticity) -> imprecision in our ability or just inability/impossibility to measure and/or capture all relevant variables.

### Establishing a Predictive Baseline

Benchmark models can reflect the best-accepted model in the literature. It can also reflect a baseline, null model which is specified without using theory.

- Baseline model should be portable and not require any domain specific knowledge so therefore it should derive its inputs only from (previous values of) the outcome variable.
    
- All predictions must be out-of-sample lest you run the risk of over-fitting. Many ways to partition data ([[k-fold cross validation]] is the most common as well as train/test). This also means cumulatively growing the sample of test data and replicating past studies to ensure continued robust prediction results out of sample.
    
- You must choose appropriate evaluation criteria.

### Demonstrating the Argument Through an Empirical Example

Consider three classes of models:

1) Those based only on structure endogenous to the outcome measure (benchmark criteria).
2) Those based only on exogenous covariates (capturing large majority of explanatory models observed in the literature).
3) Those that combine 1 and 2.

Use 4 different classification algorithms:

1) Logistic regression.
2) Elastic net regularization (adds terms to the regression equation which punishes those variables that do not contribute enough to the fit of the model).
3) Boosting (iteratively learns from a bunch of weak classifiers with greater weight placed on those data points which are poorly fit in prior iterations).
4) Neural networks.

Use AUC-PR ([[Area Under the Precision Recall Curve]]) since the outcome variable is rare. [[ROC]] is not as good at evaluating the predictive performance or rare events.

### Results

* Elastic net regularization seems to routinely do the best. However the confidence intervals overlap for all models so their performance levels aren’t statistically distinguishable from one another.
  
* Surprisingly, elastic net regularization only using benchmark variables performed the best -> predictive performance decreases when exogenous variables are added. Suggests the vast majority of the literature has missed the dominant predictive attributes of the conflict process AND suggests overfitting occurs when including endogenous and exogenous variables.
  
* Best performing model can only predict 7% of those conflicts which ultimately occur. Suggests that our theories capture the causal process quite well but the process is chaotic, OR we are missing something from our current understanding of conflict processes.

### Conclusions

Identified new relationships (like researchers should be accounting for longer memories) and also the predictive power of the algorithm changed over time (did best during the mid-1980’s and late 1990’s/early 2000’s) -> learned Cold War dynamics and then had to relearn new dynamics post-Cold War. Able to identify those variables that are important as well using the net regularization. The best performing predictive features are those with dependence effects not exogenous covariates.