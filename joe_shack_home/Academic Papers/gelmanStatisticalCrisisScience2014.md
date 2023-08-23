---
type: [Magazine article]
author: [Andrew Gelman, Eric Loken]
journal: [American Scientist]
date: 2014
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Andrew Gelman, Eric Loken
* **Title**: The Statistical Crisis in Science
* **Date of publication**: 2014
* **Journal**: American Scientist
* **Volume**: 102
* **Issue**: 6
* **Pages**: 460-65
* **URL**: [https://www.americanscientist.org/article/the-statistical-crisis-in-science](https://www.americanscientist.org/article/the-statistical-crisis-in-science)
* **Tags**: #comps_exam #statistical_crisis_science
* **PDF Attachments**:
  * [gelmanStatisticalCrisisScience2017.pdf](zotero://open-pdf/library/items/2QAVK278)

## Abstract

Data-dependent analysis—a “garden of forking paths”— explains why many statistically significant comparisons don't hold up.

## My notes

### Example

* Suppose you have a research question when you are interested in if Republicans or Democrats have better mathematical reasoning skills (and if it differs depending on the context of the mathematical test):
  
	* You obtain a sample and have everyone do a math test.
	  
	* Suppose you achieve statistically significant findings for men and not women -> men are more ideological.
	  
	* Suppose you achieve statistically significant findings for women and not men -> women are more sensitive to the context.
	  
	* The pattern might not be statistically significant for either group, but the coefficients between sexes themselves are statistically significant.
	  
	* The effect is stronger among men who had a female test giver.
	
	* There is a difference between sexes in the healthcare context but not the military context.
	
	* How do the researchers deal with independents?

* Similar example with ESP (results statistically significant only for erotic images which has familiar arguments while other equally valid arguments could have been made for non-erotic images if that result was statistically significant **OR** maybe a learning argument could be made that results improved in the second half vs. the first half).
  
	* If hypotheses are not stated clearly enough, then statistical analyses need not look like post hoc data exploration.

* Typically, this might be a problem of p-hacking, but honest researchers might also come upon the [[multiple comparisons problem]].

### The problem

* Given a particular data set, it would seem entirely reasonable to look at the data and construct rules for data exclusion, coding, and analysis which would yield the least noisy (and most significant results), and it would be a sign moving forward for which results to use and build off of.
  
	* When data analysis is a deterministic function of the observed data, the multiple comparisons problem looms large. 
  
* This problem is particularly acute in small sample sizes, small effect sizes, large potential measurement errors, and high variation (leads to low [[statistical power]]).
  
* E.g., one research paper found that stronger men (arm circumference as a proxy for strength) with high SES are more likely to oppose wealth redistribution policies while stronger men with low SES were more likely to support wealth redistribution.
  
	* There was no significant main result for arm strength, and there was only a significant interaction.
	  
	* It is likely if the authors saw a main result, they would have come up with a theoretically justified explanation for that observation. If there was no main effect and no interactions, they could like for other theoretically justified interactions.
	  
	* No evidence of p-hacking or any malicious intent. It makes sense for scientists to refine their hypotheses in response to data and to look for new effects given the main effects did not pan out.
	  
* When one makes data-dependent analysis decisions, one is at risk of the multiple comparisons problem. The statistically significant p-value cannot be taken at face value even if it is associated with existing theory.

### What do p-values really mean?

* To accept the meaning of the p-value, one has to accept the same analysis would have been performed *even if the data were different*. I.e., would the same data analysis decisions have been made with a different data set?
  
	* If so, even in settings with just one analysis of the data, the issue of multiple comparisons emerges because different decisions might have been made with different data given what cases to include/exclude, how to transform variables, tests for interactions, different codings of variables, etc.
  
* Whatever route one takes through the garden of forking paths is made to seem predetermined, but it is done implicitly. Researchers are not trying multiple tests to see what has the best p-value. They use their scientific common sense to create reasonable hypotheses given the data they have.
  
	* The mistake is in thinking that if the particular path chose yields statistical significance that this is strong evidence in favor of the hypothesis.
	  
	* The multiple comparisons problem can creep up in just one analysis of the data.

### Solutions

* [[Preregistration]].
  
	* This is not always feasible. In fields where it is (where you can collect more data), it makes sense to do data exploration in the first part and then the second part be a complete replication of the data exploration in the first part.
	  
	* Better, more comprehensive data analyses of all the different combinations which could have unfolded.
	  
	* More strict delineation of exploratory vs. confirmatory research.