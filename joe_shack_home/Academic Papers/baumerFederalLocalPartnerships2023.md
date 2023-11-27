---
type: [Article]
author: [Eric P. Baumer, Min Xie]
journal: [Criminology & Public Policy]
date: 2023
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Eric P. Baumer, Min Xie
* **Title**: Federal–local partnerships on immigration law enforcement: Are the policies effective in reducing violent victimization?
* **Date of publication**: 2023
* **Journal**: Criminology & Public Policy
* **Volume**: 22
* **Issue**: 3
* **Pages**: 417-455
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9133.12619](https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9133.12619)
* **Tags**: #journal_club #immigration #policy_evaluation #victimization
* **PDF Attachments**:
  * [baumerFederalLocalPartnerships2023.pdf](zotero://open-pdf/library/items/G6X7GHF4)

## Abstract

Our understanding of how immigration enforcement impacts crime has been informed exclusively by data from police crime statistics. This study complements existing research by using longitudinal multilevel data from the National Crime Victimization Survey for 2005–2014 to simultaneously assess the impact of the three predominant immigration policies that have been implemented in local communities. The results indicate that the activation of Secure Communities and 287(g) task force agreements significantly increased violent victimization risk among Latinos, whereas they showed no evident impact on victimization risk among non-Latino Whites and Blacks. The activation of 287(g) jail enforcement agreements and anti-detainer policies had no significant impact on violent victimization risk during the period. Contrary to their stated purpose of enhancing public safety, our results show that the Secure Communities program and 287(g) task force agreements did not reduce crime, but instead eroded security in U.S. communities by increasing the likelihood that Latinos experienced violent victimization. These results support the Federal government's ending of 287(g) task force agreements and its more recent move to end the Secure Communities program. Additionally, the results of our study add to the evidence challenging claims that anti-detainer policies pose a threat to violence risk.

## My notes

### Research Question

* **Background** -> Historically, the federal government in the USA held exclusive jurisdiction over immigrant enforcement. In 2002 after 9/11, the federal government began to request (and demand) help from state and local agencies in terms of helping them enforce immigration laws.
  
	* [[U.S. Immigration and Customs Enforcement]] (ICE) (part of the [[Department of Homeland Security]] (DHS)), created in 2003, has partnered with local official to enforce immigration law notably through [[Section 287(g)]] and the Secure Communities Program. These programs were designed to remove serious criminal aliens from the USA, but they have generated a lot of controversy because the vast majority of individuals affected by these programs are not serious criminals.
	  
	* Many jurisdictions have decided to decline cooperation with federal authorities and have passed [[sanctuary policies]] and anti-detainer policies which limit the role local officials can play in immigration enforcement.
	
* Has Section 287(g), the Secure Communities program, and the contrasting sanctuary policies/anti-detainer policies made the USA safer? Specifically using the [[National Crime Victimization Survey]] -> has the rate of victimization decreased?
* 
	* Has it affected victimization risk differently among Latinos, non-Latino Whites, and non-Latino Blacks?
  
* Challenges in the research:
  
	* Section 287(g), Secure Communities, and sanctuary/anti-detainer policies are often implemented side-by-side and with different intensity. There is an immense amount of heterogeneity within place in terms of how/when these policies get implemented.
	  
		* Section 287(g) (passed in 1996) allows ICE to enter into agreements with local law enforcement agencies and allows those agents to take on the roles of ICE agents and directly enforce federal immigration law. Three models:
		  
			* **Jail Enforcement** -> Check immigration status of those arrested and booked.
			  
			* **Task Force** -> Check immigration status of anyone stopped.
			  
			* Hybrid model.
			  
			* ICE began to phase out this program in 2012 as there was evidence the program was racially biased. However, under the Trump administration, the program was revived. It dropped the **Task Force** model, and it created the **Warrant Service Officer** model allowing local officials to execute ICE warrants.
		  
			* As October 2022, ICE had 287(g) jail enforcement agreements with 64 law enforcement agencies in 19 states and warrant service officer agreements with 76 law enforcement agencies in 11 states.
			  
		* Secure Communities was launched in 2008. When individuals were arrested and booked, their fingerprints were automatically sent to ICE. It was suspended in November 2014 when it raised constitutionality concerns. In January 2017, it was reinstated by President Trump. It was revoked in January 2021 by President Biden.
		  
		* Local jurisdictions often adopt policies to limit local participation with federal enforcement. Often these policies are called anti-detainer policies and do not allow for the detainment of an individual past their release date (as ICE may ask to detain an individual longer to understand their immigrant status). This opens up a locality to extra financial costs (for housing an individual) as well as opening them up to litigation. Some jurisdictions, as a result, limit compliance (or do not allow for compliance) with ICE detainer requests either out of financial concerns of humanitarian concerns or both.

	* [[UCR]] data has been the de facto standard for tracking crime rates. However, this data only captures crimes reported to the police. It is likely that this form of missingness is correlated with community attributes relevant to variation in the activation of immigration policy.
	  
		* UCR also does not allow for an analysis of differential crime exposure by race/ethnicity.

### Background and Importance

* Descriptive analyses have cast doubt on the efficacy of 287(g) and Secure Communities given that most people deported had very no criminal convictions or very minor crimes (immigration or traffic violations).
  
* Theoretically, it might increase crime by disrupting local social and economic life, entangling local crime-fighting resources with immigration enforcement, and damaging community cooperation with law enforcement thus increasing the vulnerability of already vulnerable groups to crime.
### Data & Methods

* Data comes from the NCVS from 2005 to 2014 and publicly available data on when/where various immigration enforcement policies took effect. Individuals home census tracts were able to be identified using restricted access data. Used publicly available data from the [[ACS]], [[Census of Law Enforcement Agencies]], and [[Law Enforcement Agency Roster]].
  
* 354,000 individuals with 1,006,000 interviews.
  
* **Dependent variable** -> Did a respondent experience violent victimization during the 6 months preceding their interview? 1/0.
  
* **Independent variables**
	* Was Secure Communities active in the county during the 6 month reference period?
	* Was a 287(g) agreement active in the county?
	* Was an anti-detainer policy active in the county?
	  
* **Individual controls** -> Age, gender, race, marital status, education, employment status, income, homeownership, and residential tenure.
  
* **Neighborhood controls** -> Census tract. Population density, concentrated disadvantage, racial/ethnic heterogeneity, neighborhood age profile, family disruption (% divorced or separated), and residential instability (% of households which moved into their unit less than 10 years ago, % vacant), percent unemployed, immigration history (traditional or new immigrant destination), policing resources (police force size and expenditures), adjacency to the border, and regional location.
  
* Estimate a [[between-within model]]. Used repeated interviews with the same respondent and group-mean centering to partition policy effects into between-person differences and within-person changes.
  
	* As a robustness check, also use [[fixed effects]] [[difference in differences]] [[Logistic regression]] to estimate models using only within-person variance. Lead-lag effects were statistically indistinguishable from 0 indicating support for the parallel trends assumption.
	  
* Unique among policy papers because the unit of analysis is at the individual level.
### Results

* **Table 2** -> Secure Communities being active was associated with an increased risk of victimization. Null results for Section 287(g) and anti-detainer laws.
  
* **Table 4** -> Secure Communities and Section 287(g) task force agreements increased risk of victimization for Latinos (only). No increase in risk of victimization for Whites or Blacks. Null results for anti-detainer laws.
  
*  **Robustness analysis** -> Use [[propensity score matching]] difference in differences. Match NCVS respondents residing in counties where a given policy was activated to similar NCVS respondents residing in counties where the given policy was not activated.
  
* Anti-detainer programs do not increase crime.
  
* "... 287(g) and Secure Communities... provide no discernible crime-protective benefits while also bringing adverse consequences for Latinos. These findings lend support to the notion these programs fostered a devolution of discretion and net-widening that eroded trust of police in the communities they targeted, putting Latino residents at a higher risk of victimization." -> Other mechanisms could be at play as well.

### Future research

* Spatial dynamics, particularly policy spillover effects.