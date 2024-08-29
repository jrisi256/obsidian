---
type:
  - Article
author:
  - Charles E. Loeffler
  - Daniel S. Nagin
journal:
  - Annual Review of Criminology
year: 2022
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Charles E. Loeffler, Daniel S. Nagin
* **Title**: The Impact of Incarceration on Recidivism
* **Date of publication**: 2022
* **Journal**: Annual Review of Criminology
* **Volume**: 5
* **Issue**: 1
* **Pages**: 133-152
* **URL**: [https://doi.org/10.1146/annurev-criminol-030920-112506](https://doi.org/10.1146/annurev-criminol-030920-112506)
* **Tags**: #comps_exam, #crime_policy, #incarceration
* **PDF Attachments**:
  * [loefflerImpactIncarcerationRecidivism2022.pdf](zotero://open-pdf/library/items/EE9AH9WQ)

## Abstract

The US prison population stands at 1.43 million persons, with an additional 740,000 persons in local jails. Nearly all will eventually return to society. This review examines the available evidence on how the experience of incarceration is likely to impact the probability that formerly incarcerated individuals will reoffend. Our focus is on two types of studies, those based on the random assignments of cases to judges, called judge instrumental-variable studies, and those based on discontinuities in sentence severity in sentencing grids, called regression discontinuity studies. Both types of studies are designed to account for selection bias in nonexperimental estimates of the impact of incarceration on reoffending. Most such studies find that the experience of postconviction imprisonment has little impact on the probability of recidivism. A smaller number of studies do, however, find significant effects, both positive and negative. The negative, recidivism-reducing effects are mostly in settings in which rehabilitative programming is emphasized and the positive, criminogenic effects are found in settings in which such programming is not emphasized. The findings of studies of pretrial incarceration are more consistent—most find a deleterious effect on postrelease reoffending. We also conclude that additional work is needed to better understand the heterogeneous effects of incarceration as well as the mechanisms through which incarceration effects, when observed, are generated. For policy, our conclusion of the generally deleterious effect of pretrial detention adds to a larger body of evidence pointing to the social value of limiting its use.

## My notes

### Background

* Trying to assess the causal effect of incarceration. But as compared to what?
  
* Alternatives are either: **A)** a non-incarceration sanction like probation for individuals convicted of a crime, or **B)** for individuals held in jail pretrial vs. those who are not held in jail pretrial.
  
* The focus of this review is on: #random_judges or [[judge instrumental variables]] and [[regression discontinuity]] designs. These designs are better able to control for selection vs. other techniques like matching.

### Results from comparing incarceration to non-incarceration

* All USA-based studies of adults report null or criminogenic findings concerning the effects of incarceration on recidivism, and none found any beneficial effects.
  
	* One study, though, found that incarceration has no effect on reconviction for new offenses, they did find incarceration increased the likelihood of technical violations and thus increased future incarceration rates for the previously incarcerated. #paper_idea -> cycles of [[cumulative disadvantage]].
  
* Most research has found [[instrumental variable]] estimates to be comparable to [[OLS]] estimates suggesting that biases arising from [[selection bias]] or [[omitted variable bias]] were not as pronounced as previously thought.
  
	* "Our conclusion concerning omitted variable bias suggests that future research does not need to use IV or RD designs or other approaches such as partial identification (Manski 1995) to account for unmeasured case features to be valid. It would be preferable, of course, if a research setting could be identified where methods designed to account for unmeasured case features could be used, but our review suggests that this is not a necessity for producing credible estimates of the causal effect of incarceration. Estimates based on designs, assuming controls for observables are sufficient to avert material biases due to selection, must, however, include a rich set of such controls." #quote Pretty powerful quote.
  
* One under-examined assumption of instrumental variables unique to judges is the monotonicity assumption which assumes that judges differ in the level of their use of imprisonment and the level difference is proportionally the same across crime type (e.g., judge A is twice as likely to impose a prison sentence as judge B across all crime types). A have attempted to correct for this, and they have not found any differences in results.
  
	* There are also concerns about the exclusion restriction in the sense that different judges will have different propensities to sentence different non-incarceration sentences.

### Comparing pretrial incarceration to non-pretrial incarceration

* Results are pretty uniformly bad concerning the policy efficacy of pretrial incarceration. Pretrial incarceration is shown to cause higher recidivism rates.
	* Disruption from temporary detention and the absence of programming + reentry services leads to pretrial detention being particularly bad.
  
* Some caution should be shown towards these results because the post-conviction literature relies upon random case assignment while the pretrial literature relies upon randomness in judge scheduling which does not guarantee balance in expectation. Balance can only be demonstrated for measured case and individual characteristics.

### Regression discontinuity papers

In this literature, researchers often attempt to exploit discontinuities which emerge from sentencing guideline grids which rely upon offense severity and criminal history.

Only 5 studies have been done.

* Two of the five studies found null or criminogenic results. One study found for positive results, but preventative/deterrent/incapacitative effects may dissipate after 3 years.
  
* One found positive results for juveniles. -> The authors note the incarceration facility was largely seen as rehabilitative.
  
* One positive result was found for federal prisons.

Authors argue this evidence largely concurs with what is found in the instrumental variable literature, but I think it is a bit more mixed.
### High-level results

* Post-conviction imprisonment has no effect on re-offending or exacerbates it. #highlight Less use of incarceration should not increase crime, on the margin (meaning for those people who probation is a consideration).
  
	* In one case, the effects were seen to be rehabilitative. However, that study was conducted in Norway, and it served as a point of comparison between the USA and Norway and how Norway's prison system is actually rehabilitative. Additionally, incarceration is hardly used in Norway.
	  
* Pretrial incarceration results in higher rates of convictions and higher rates of recidivism. This practice should be stopped -> #highlight strong suggestion by the authors!

### Future Research

* We need more [[treatment heterogeneity]] studies that focus on how different prison experiences and different prisons produce different likelihoods of recidivism.
	* See Norway vs. USA.