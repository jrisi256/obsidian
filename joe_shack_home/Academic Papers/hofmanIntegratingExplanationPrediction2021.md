---
type: [Article]
author: [Jake M. Hofman, Duncan J. Watts, Susan Athey, Filiz Garip, Thomas L. Griffiths, Jon Kleinberg, Helen Margetts, Sendhil Mullainathan, Matthew J. Salganik, Simine Vazire, Alessandro Vespignani, Tal Yarkoni]
journal: [Nature]
date: 2021-07
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Jake M. Hofman, Duncan J. Watts, Susan Athey, Filiz Garip, Thomas L. Griffiths, Jon Kleinberg, Helen Margetts, Sendhil Mullainathan, Matthew J. Salganik, Simine Vazire, Alessandro Vespignani, Tal Yarkoni
* **Title**: Integrating explanation and prediction in computational social science
* **Date of publication**: 2021-07
* **Journal**: Nature
* **Volume**: 595
* **Issue**: 7866
* **Pages**: 181-188
* **URL**: [https://www.nature.com/articles/s41586-021-03659-0](https://www.nature.com/articles/s41586-021-03659-0)
* **Tags**: #comps_exam, #computational_social_science
* **PDF Attachments**:
  * [hofmanIntegratingExplanationPrediction2021.pdf](zotero://open-pdf/library/items/T8ZBZFEE)

## Abstract

Computational social science is more than just large repositories of digital data and the computational methods needed to construct and analyse them. It also represents a convergence of different fields with different ways of thinking about and doing science. The goal of this Perspective is to provide some clarity around how these approaches differ from one another and to propose how they might be productively integrated. Towards this end we make two contributions. The first is a schema for thinking about research activities along two dimensions—the extent to which work is explanatory, focusing on identifying and estimating causal effects, and the degree of consideration given to testing predictions of outcomes—and how these two priorities can complement, rather than compete with, one another. Our second contribution is to advocate that computational social scientists devote more attention to combining prediction and explanation, which we call integrative modelling, and to outline some practical suggestions for realizing this goal.

## My notes

### Problem

* Social scientists favor interpretatively satisfying explanations of individual and collective human behavior often invoking causal mechanisms derived from substantive theory.
  
	* Favor methods which identify causal relationships and create unbiased estimates of interesting parameters.
	  
	* Estimate models entirely in-sample.
	  
	* Model specification should be theory-driven.
	  
	* Replication failures, generalization failures, low predictive utility, and lack of solutions to real-world problems. 
  
* Computer scientists have favored accurate predictive models regardless of their relationships to causal mechanisms or interpretability.
  
	* Favor methods like machine learning models which minimize predictive error on unseen data.
	  
	* Complex models are acceptable as long as they achieve substantively better predictive outcomes.
	  
	* Also fail to generalize, uninterpretable, and biased.

### Prediction vs. Explanation

* [[Null hypothesis significance testing]] are exceptionally weak tests of theory since it is, in effect, arguing data are not inconsistent with my theory, but it offers no confirmatory proof of one's theory being true.
  
* On the other hand, purely predictive exercises risk confusing prediction with explanation. Simply being able to predict outcomes well does not mean one has a good substantive understanding of the phenomenon (e.g., 2-week lagged CDC flu case counts predict future flue case counts very well). Assessing predictive accuracy is thus very dependent upon the baseline. 

### Integrative modeling

![[hofmanIntegratingExplanationPrediction2021_table1.png]]

1) Descriptive work -> surveys, topical modeling, community detection
2) Basically all social science -> observational regression-techniques, quasi-experimental, experimental methods
3) Supervised machine learning, out-of-sample
4) A combination of quadrants 2 and 3. Words of caution, forcing one's explanations to make predictions can reveal they explain less than one would like. There may be fundamental limits to predictive accuracy which results from system complexity and randomness. The least studied quadrant and deserves more attention.
   
	1) Predict/model the outcomes of an experiment.
		1) Alternate between predictive and explanatory modeling.
		   
	2) How well does a causal estimate in one domain transfer to another?
	   
	3) Machine learning techniques can improve [[matching]] and [[instrumental variable]] estimation. More efficiently design experiments. Benchmark the completeness of explanatory models.
	   
	4) Structural causal models have been shown to improve the generalizability of predictive models.

### Recommendations

* Add some sort of badge system for identifying what quadrant research falls under as well as the level of granularity of results.
  
* [[Pre-registration]].
	* Separate the building of models from the the act of testing models.
  
* Common task framework.
	* [[Goodhardt's Law]] -> When a measure becomes a target, it ceases to become a good measure.

### Interpretability

Separate issue:

* A model can be shown to have very robust predictions in a wide variety of contexts while not being interpretable and subject to human understanding (and still being useful) (e.g., quantum mechanics).
  
* A theory can have a great deal of intuitive appeal or even make sense of a great deal of phenomena, but it may not be predictive or demonstrably causal.
  
* Interpretability should be valued on its own grounds and not by how much it contributes to causal explanations or prediction.