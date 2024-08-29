---
type:
  - Article
author:
  - Emily K. Weisburst
journal:
  - Journal of Policy Analysis and Management
year: 2019
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Emily K. Weisburst
* **Title**: Patrolling Public Schools: The Impact of Funding for School Police on Student Discipline and Long-term Education Outcomes
* **Date of publication**: 2019
* **Journal**: Journal of Policy Analysis and Management
* **Volume**: 38
* **Issue**: 2
* **Pages**: 338-365
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1002/pam.22116](https://onlinelibrary.wiley.com/doi/abs/10.1002/pam.22116)
* **Tags**: #comps_exam, #crime_policy, #policing, #racial_inequality, #school_resource_officers
* **PDF Attachments**:
  * [weisburstPatrollingPublicSchools2019.pdf](zotero://open-pdf/library/items/PTT7RPHD)

## Abstract

As police officers have become increasingly common in U.S. public schools, their role in school discipline has often expanded. While there is growing public debate about the consequences of police presence in schools, there is scant evidence of the impact of police on student discipline and academic outcomes. This paper provides the first quasi-experimental estimate of funding for school police on student outcomes, leveraging variation in federal Community Oriented Policing Services (COPS) grants. Exploiting detailed data on over 2.5 million students in Texas, I find that federal grants for police in schools increase middle school discipline rates by 6 percent. The rise in discipline is driven by sanctions for low-level offenses or school code of conduct violations. Further, I find that Black students experience the largest increases in discipline. I also find that exposure to a three-year federal grant for school police is associated with a 2.5 percent decrease in high school graduation rates and a 4 percent decrease in college enrollment rates.

## My notes

### Introduction

**Research Question** -> What is the impact of the police on student discipline outcomes and future academic success?

**Arguments for more police in schools** -> School resource officers (SROs) can serve as educators, counselors, and positive role models while improving school safety. Students cannot learn in an unsafe environment.

**Arguments against more police in schools** -> SROs create a heavy-handed disciplinary culture which undermines learning and further disadvantages poor and minority students. Leads to stigmatization and decreased attachment to school -> can affect human capital development and eligibility for resources.

**High-level results** -> Using data from 2.5 million public school students in Texas. Federal funding for school police:

* Increases disciplinary rates by 6% for middle school students (no effects for high school students).
  
* Decreases high school graduation rates by 2.5% and college enrollment rates by 4%.
  
* All student racial groups experience significant increases in disciplinary actions, the effects are largest for Black students.
  
* Declines in college enrollment are concentrated among low-income students.

### Data and Methods

Challenges in estimating the effect of SROs:
  
* Data availability.
* [[confounders]] -> SROs are more likely to be assigned to disadvantaged schools.
* [[simultaneity bias]] -> even using longitudinal data is not perfect if the hiring of SROs is in response to changes to student behavior and school discipline.

Uses the [[Federal COPS Grant]] to introduce exogenous variation from 1999 to 2008.
* Schools are not rewarded the grant randomly.
* However, the author uses within-school variation. They compare schools in years where they received federal funding to years where they did not. The model also controls for school district decisions to apply for funding.

Model:

* School disciplinary action and long-term education outcomes -> at the student-year level.
  
	* **Individual-level variables** (student race, grade-level, limited English proficiency, Special education, gifted/talented, economically disadvantaged).
	  
	* Year [[fixed effects]].
	  
	* Grade-level fixed effects.
	  
	* School-district fixed effects. 
	  
	* Key independent variables are **Accepted** for a grant and **Applied** for a grant. Also controls for the application and acceptance of other grants in the COPS system.
	  
	* One big limitation is that the author does not have data on the number of officers.
		* **Table 3** -> School districts devote more resources to security when covered by the grant. Other evidence in the appendix also demonstrates more officers being hired as SROs.

	* The author notes this is similar conceptually to a [[difference in differences]] model.

### Results

**Table 4** -> See the effects for disciplinary outcomes.
* **Table 5** -> Increase in discipline is driven by low-level offenses or school conduct code violations rather than for serious offenses.

**Table 6** -> Lower high school graduation rates and lower college enrollment (driven by lower 2-year college enrollment).

**Table 7** -> All racial groups experienced more discipline, but it was the highest for Black students.
* **Table 8** -> Declines in high school graduation and college admission do not appear to be statistically significantly different across racial groups.

Lots of robustness checks.

* Conditional on grant application decisions, the timing of the grant acceptance should not be a function of changes in student outcomes. They find that the timing of the grant acceptance is unrelated to pre-treatment changes in student disciplinary actions.
  
* [[Placebo tests]] -> Artificially vary the timing of the treatment by randomly assigning **accept** treatments to districts which applied for a grant in a given year.
  
* School districts which apply for grants may be very different from school districts which do not apply. School district fixed effects account for time-constant differences but not time varying differences. They do a variety of checks for this (e.g., estimate the effect only for schools that ever applied), but the big one is interacting year fixed effects with grant history status (never applied, always accepted, only rejected, and accepted and rejected).
  
* Include controls for region of Texas and school enrollment size.
  
* Interact year fixed effects and district fixed effects with student race, income, and gender to account for differential trends in school discipline by race, income, and gender.
  
* One mechanism which could explain the high school and college findings is that students who are most likely to be disciplined drop out of school when funding for police officers increases. Re-estimates the model only including students who do not drop out.
  
* Effects are robust when including grade by year fixed effects and grade by school district fixed effects. 