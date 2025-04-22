---
title: Examining the relationship between U.S. incarceration rates and population health at the county level
author:
  - Robert R. Weidner, Jennifer Schultz
year: 2019
journal:
  - SSM - Population Health
type:
  - Article
---
[Zotero entry](zotero://select/items/@weidnerExaminingRelationshipUS2019)
**Tags**: #effects_of_incarceration #incarceration #incarceration_health #instrumental_variable #community_effects 
## Abstract

A collateral consequence of mass incarceration in the United States is its negative effects on population health. Using data from 2015, this study examines the relationship between incarceration rates and population health for a national sample of U.S. counties. To obtain unbiased estimates of the effect of incarceration on health, we use multivariate models which account for the endogeneity of incarceration rates when determining their effect on population health by employing an instrumental variable approach where the robust instrumental (exogenous) variable per capita corrections expenditures is used to predict incarceration rate. We then estimate population health outcomes as a function of predicted incarceration rate alongside factors such as public health spending, indicators of health behavior and control variables in models explaining county-level population health. Consistent with findings from prior research on individuals, families and at the state level, results of our analyses indicate that higher levels of incarceration are associated with higher levels of both morbidity (percentage reporting fair or poor health) and mortality (life expectancy). Implications of these findings for health and criminal justice policy, as well as research, are considered.

### Mechanisms

#### Incarcerated individuals

* Prisoners tend to have much higher rates of chronic and infectious diseases than the general public.
* Degradation of skills and lack of ability to develop marketable skills --> inability to develop social capital and find work --> long periods of unemployment and relationship instability --> unlikely to have health insurance due to inability to find consistent employment.
* Stigmatized which causes mental and physical strain.
* Inability to find consistent, stable housing. Homelessness is much higher among former prisoners vs. the general public.

#### Effects on families

* Adds to instability in the life of the children --> causing educational problems. Can also worsen health of the children.
* Left behind women caregivers have less financial resources to leverage in the care of their child causing physical strain and increased risk of contracting chronic diseases like hypertension and diabetes.

#### Effects on communities

* Returning prisoners bring with them the trauma of incarceration as well lessened potential to find work harming the overall economic health of the community.
* Greatly increases the risks of STI transmission --> skews the male/female ratio causing riskier sex practices to emerge.

### Methods

* Use an [[instrumental variable]], correctional expenditures.
* First-stage, estimate incarceration rates as a function of correctional expenditures.
	* If spending increases on corrections, and this causes other funding to decrease as a result, does this not violate the exclusion restriction? Authors argue, based on prior research, spending on incarceration does not crowd out health spending.
	* There is some evidence to suggest corrections spending does crowd out welfare spending. Authors argue that most welfare money comes from the federal government, and thus any crowding out effects are likely small.
	* Correlational analysis reveals a weak and non-significant relationship between corrections spending and health and a weak (albeit positive and significant) relationship between corrections spending and welfare.
	  
* **Independent variable**: Sum (?) of the average daily jail county population and the prison admission rate from [[Vera Incarceration Trends]] from 2015.
* **Instrumental variable**: County-level per capita spending on corrections which comes from the [[Census of Governments]]. It is log-transformed. It is from 2012 (thus 3-year lag from incarceration data).
* **Dependent variable**:
	* Data comes from [[County Health Rankings and Roadmap tool]] which draws the data from [[Behavioral Risk Factor Surveillance System]] and the [[National Vital Statistics System]].
	* Premature death (years of potential life lost before age 75).
	* % in fair or poor health.
* **Controls** (slight different across the two models): 
	* Model 1 --> [[UCR]] index crime rate, urban/rural, % Black, % unemployed, median household income, % of children in single-parent households, number of social associations. Data comes from [[County Health Rankings and Roadmap tool]] which is sourced from the [[ACS]]. Data come from a variety of years (2006 - 2012).
	* Model 2 --> Categorical variable for state, natural logarithm of per capita spending on public health, urban/rural, % adults who smoke, % adults who are obese, % uninsured, % of diabetes patients who have their glucose regularly monitored, poverty index (unemployed, children in poverty, children in single-parent households, % Black).
		* Data comes from [[County Health Rankings and Roadmap tool]] who source their data from a variety of sources including: [[Behavioral Risk Factor Surveillance System]], [[SAHIE]], [[Centers for Medicare and Medicaid Services]].
* **Modelling**: [[two stage least-squares regression]] using [[OLS]].

### Results

* Higher rates of incarceration seem to cause worse health outcomes.