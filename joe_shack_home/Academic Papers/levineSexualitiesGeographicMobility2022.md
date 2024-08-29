---
type:
  - Article
author:
  - Andrew Levine
journal:
  - Demography
year: 2022
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Andrew Levine
* **Title**: Sexualities and Geographic Mobility Between Childhood and Adulthood in the United States
* **Date of publication**: 2022-08-01
* **Journal**: Demography
* **Volume**: 59
* **Issue**: 4
* **Pages**: 1541-1569
* **URL**: [https://doi.org/10.1215/00703370-10085223](https://doi.org/10.1215/00703370-10085223)
* **Tags**: #journal_club, #migration, #sexual_minorities
* **PDF Attachments**:
  * [Levine_2022_Sexualities and Geographic Mobility Between Childhood and Adulthood in the.pdf](zotero://open-pdf/library/items/N9XVCJSM)

## Abstract

Though research suggests that sexual minorities (e.g., nonheterosexual individuals) are more geographically mobile in the transition to adulthood than their heterosexual counterparts, quantitative estimates are rare and previously used data sources have significant limitations. Using data from the National Longitudinal Study of Adolescent to Adult Health (N = 11,705) that directly measure sexualities across dimensions (i.e., identity, behavior, and attraction), I examine variation in geographic mobility between childhood (ages 11–17) and adulthood (ages 26–34) across various sexualities (e.g., gay/lesbian and bisexual). Three findings emerge. First, mobility varies across sexualities. Individuals with gay/lesbian identity, same-sex behavior, and same-sex attraction are more geographically mobile than individuals with heterosexual identity, different-sex behavior, and different-sex attraction, respectively. By contrast, individuals with bisexual identity, both-sex behavior, and both-sex attraction tend to be statistically indistinct from individuals with heterosexual identity, different-sex behavior, and different-sex attraction, respectively. Second, mobility differences are largest and most prevalent when sexualities are operationalized according to identity. Third, evidence suggests that the effects of gay/lesbian identity, same-sex behavior, and same-sex attraction on mobility are larger for men than for women. In providing the first quantitative estimates of geographic mobility differences across broader sexual minority and heterosexual populations, this study expands inquiry related to sexualities and mobility.

## My notes

### What is the research question?

* Are sexual minorities more geographically mobile between childhood and adulthood?
	* Avoid rejection and stigmatization.
	* Evade surveillance from family.
	* Increase their chances of finding a partner.
	* Weaker ties to place of origin due to being less socially integrated and worse relationships with parents.
	* More willing to move to be with those who share their sexual orientation and life experiences. [[Homophily]].
	* More willing to travel to achieve an education. Why would they want an education?
		* Minimize stigmatization and maximize social acceptance. By doing well in school, one can boost their chances of leaving their hometown. They may also believe college environments to be more accepting.
	  
* What individual, household, parent, and geographic characteristics best explain these differences?
  
* How do mobility gaps vary across dimensions of sexuality? E.g., are mobility differences between heterosexuals and gay/lesbian individuals the same as those between heterosexuals and bisexuals?

* Very little previous quantitative work trying to answer this question. Census data does not directly measure sexual identity (can only be inferred if individuals are living together of the same-sex). People have also not properly captured the wide variety of ways in which sexuality can be measured.
### How do you propose to answer it?

* Use data from the [[National Longitudinal Study of Adolescent to Adult Health]] (Add Health).
  
* Sexual orientation is measured in 3 ways:
	* Identity (how does one label one's self).
	* Behavior
	* Attraction
* These dimensions do not always align.
  
*  **Dependent variable** -> Did the individual move between Wave 1 (ages 11-17) and Wave 4 (ages 26-34)? Uses these constructs instead of intra-neighborhood mobility or number of moves because mobility differences for sexual minorities, theoretically, would argue for moves over a long distance.
	* Distance from childhood address.
	* Inter-county mobility.
	* Interstate mobility.
	  
* **Independent variable** -> Sexual identity, sexual behavior, and sexual attraction.
	* Also interact gender with sexual orientation and all other variables. The authors claim this is equivalent to estimating gender-specific models but is more computationally efficient. #highlight #question 

* **Confounding variables**: Measured during Wave 1 (unless otherwise noted although I do not note it here in my notes).
	* Childhood county unemployment rate
	* Childhood county median household income
	* Household income
	* Number of children
	* English primary language
	* Parental age
	* Parental gender
	* Parental educational attainment
	* Parental immigrant status
	* Parental employment status
	* Parental occupation
	* Parental college expectations
	* Individual age
	* Individual gender (no options for transgender)
	* Individual race/ethnicity
	* Individual residential duration
	* Individual neighborhood satisfaction
	* Individual living with parent

* **Mediators**: Measured during Wave 1 (unless otherwise noted although I do not note it here in my notes).
	* Social integration -> social acceptance, family understanding, closeness to parent, and desire to move.
	* Educational attainment -> GPA, college expectations, educational attainment.

* Estimate a series of [[OLS]] and [[Logistic regression]] models.
  
* Supplemental analyses include childhood county size, childhood county political behavior (proportion who voted Republican in 1992 Presidential election), parents' knowledge of individual's sexual identity.
	* Individuals are more mobile if they're from a more Republican county and are less mobile if they're from a bigger county. No statistically significant results emerge when including if a parent knows the individual's sexual orientation.
### What do you find?

* Individuals with gay/lesbian identity live farther away from their communities of origin and are more likely to move counties than their heterosexual counterparts.
  
* Geographic mobility differences between individuals with bisexual and heterosexual identities tend to be small and statistically insignificant.
  
* Depending on how one measures sexuality, the differences in mobility vary. Mobility gaps are largest when sexuality is conceived of as sexual identity rather than sexual behavior or same-sex attraction.
	* The author argues this makes sense theoretically. Sexual identity (how one views one's self) has the strongest effect on one's life course.
	* Open question -> sexual identity is constituted through place (i.e., you emulate those around you and may then construct your identity based on this or follow their lead and also become geographically mobile) or through migration (i.e., the distance allows for the establishment of one's own unique identity).

* The effects of gay/lesbian identity on mobility are larger for men vs. women.
	* Sexual minority status tends to confer greater stigma on men vs. women. Men may be more willing to move further to escape such stigmatization.
	  
* **Table 2** -> Descriptively it would appear as if sexual minorities are more likely to live further away from their childhood address.

* **Table 3** -> Marginal predictions from models demonstrate that the results are pretty durable across various measures of sexual orientation and geographic mobility.
  
	* Gay/lesbian individuals more likely to move farther and out of their parent's county (holds across really all measures of sexual orientation). Bisexual individuals not so much. Results are statistically insignificant for interstate mobility.
	  
	* One also sees that differences are largest when sexual orientation is measured by sexual identity.
	  
* Common explanations of geographic mobility (e.g., local labor market conditions, residential satisfaction, socioeconomic characteristics, life course milestones) fail to fully explain variation across sexual orientations.
	* Remaining gaps (outside the scope of this study) might be explained by stigmatization. This would need to be measured.
	* Proportion of sexual minorities living in a given county would also be useful to know.
	* Reasons for mobility differences among sexual minorities are unclear (bisexual vs. gay/lesbian). Seem to have the least social acceptance and greatest desire to move in childhood.
		* Not enough resources to move? Accounting for adulthood resources does not change the findings.
		* The category is too ill-defined and noisy. It is a very fluid identity.