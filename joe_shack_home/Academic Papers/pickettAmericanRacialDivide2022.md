---
type: [Article]
author: [Justin T. Pickett, Amanda Graham, Francis T. Cullen]
journal: [Criminology]
date: 2022
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Justin T. Pickett, Amanda Graham, Francis T. Cullen
* **Title**: The American racial divide in fear of the police
* **Date of publication**: 2022
* **Journal**: Criminology
* **Volume**: 60
* **Issue**: 2
* **Pages**: 291-320
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9125.12298](https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9125.12298)
* **Tags**: #comps_exam, #policing, #racial_inequality, #survey
* **PDF Attachments**:
  * [pickettAmericanRacialDivide2022.pdf](zotero://open-pdf/library/items/BJMU946Y)

## Abstract

The mission of policing is “to protect and serve,” but recent events suggest that many Americans, and especially Black Americans, do not feel protected from the police. Understanding police-related fear is important because it may impact civilians’ health, daily lives, and policy attitudes. To examine the prevalence, sources, and consequences of both personal and altruistic fear of the police, we surveyed a nationwide sample (N = 1,150), which included comparable numbers of Black (N = 517) and White (N = 492) respondents. Most White respondents felt safe, but most Black respondents lived in fear of the police killing them and hurting their family members. Approximately half of Black respondents preferred to be robbed or burglarized than to have unprovoked contact with officers. The racial divide in fear was mediated by past experiences with police mistreatment. In turn, fear mediated the effects of race and past mistreatment on support for defunding the police and intentions to have “the talk” with family youths about the need to distrust and avoid officers. The deep American racial divide in police-related fear represents a racially disparate health crisis and a primary obstacle to law enforcement's capacity to serve all communities equitably.

## My notes

### Background

4 sources of police-related fear:

1. **Vulnerability** -> Those who are most exposed to danger and most unable to protect themselves will be most fearful. Black Americans, given their history with the police and higher rates of contact, will be most afraid.
   
2. **Prior victimization**.
   
3. **Media cultivation** -> exposure to new coverage (which may or may not reflect the reality of the situation) makes viewers more fearful.
   
4. **Neighborhood context** -> What do individuals encounter on a regular basis in their neighborhood? Neighborhood disorder and police presence (signs of dangers) may increase fear of the police while things like [[Collective efficacy|collective efficacy]] would decrease fear.

### Data and Methods

* Sample administered (through [[YouGov]]) in early 2021 to a nationally representative sample (basd on race, gender, age, and education) (N = 1,150) with an equal number of Black (N = 517) and White (N = 492) respondents.
  
* Asked about:
	* Personal fear of the police.
	* *Altruistic* fear of the police (i.e., fear they'll do something bad to your friends and family).
	* Personal fear of crime.
	* Prior police mistreatment.
	* News exposure (number of days you watched the news or read news on the Internet). #disagree -> people are bad at estimating their media consumption.
	* Included neighborhood measures of disorder, collective efficacy, and *perceived* percent black.
	* **Consequences of fear**
		* Intentions to engage in defensive socialization -> *the talk*.
		* Support for defunding the police.
	* **Controls**
		* Urbanicity, region, individual-level demographic, economic, political, and religious factors.
		  
* Ran an experiment asking participants if they would rather be the victim of a serious felony (randomly assigned: robbery or burglary) or experience one of three types of unprovoked police contact (randomly assigned: questioned, searched, arrested).
  
* Estimated unweighted [[OLS]] models with [[robust standard errors]] to account for [[heteroskedasticity]].

### High-level results

* Most White respondents felt safe around the police while most Black Americans were afraid of the police. White respondents were more afraid of crime than police while the opposite was true for Black respondents.
	* Black respondents were more afraid of the police even when disaggregating by socioeconomic status and sex.
	* Low SES Black respondents were slightly more afraid than high SES Black respondents. Low SES White respondents were *slightly, slightly* more afraid than High SES White respondents.
	* Female Black respondents were slightly more afraid than Male Black respondents. Female White respondents were more afraid for the safety of others vs. White Male respondents.
  
* About half of Black respondents (and 35% of White respondents) preferred to be robbed than to have an unprovoked search by the police.
	* 60% of Black respondents (and 50% of White respondents) would rather be the victim of a robbery than be arrested unprovoked.
	* 45% of Black respondents (and 20% of White respondents) would rather be robbed than have an unprovoked question by the police.
  
* Fear of the police was mediated by past experiences of police mistreatment. Black respondents reported experiencing far more police mistreatment than White respondents.
	* News consumption was not statistically significantly associated with fear of the police.
	* Neighborhood police visibility is positively related to fear of the police. Other neighborhood variables like collective efficacy and disorder are either strangely negative or null.
	* Interestingly, being involved with police work decreased one's fear of the police.
  
* Fear of the police mediated the effects of race/past mistreatment on support for defunding the police and wanting to talk about youths about the dangers of the police.
	* Support for defunding the police and having the talk increase as fear of the police increases.
		* Despite the differences in fear of policing -> only a small percentage of respondents reported wanting to disband the police (15% of Black respondents and 8% of White respondents).
		* 51% of Black respondents supported defunding while only 29% of White respondents supported defunding.
	* The race effects for defunding the police disappear once fear of the police is included (racial effects still exist for the talk although the racial effect is attenuated).