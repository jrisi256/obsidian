---
type: [Article]
author: [Marie Ouellet, Sadaf Hashimi, Jason Gravel, Andrew V. Papachristos]
journal: [Criminology & Public Policy]
date: 2019
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`

## Metadata

* **Author(s)**: Marie Ouellet, Sadaf Hashimi, Jason Gravel, Andrew V. Papachristos
* **Title**: Network exposure and excessive use of force
* **Date of publication**: 2019
* **Journal**: Criminology & Public Policy
* **Volume**: 18
* **Issue**: 3
* **Pages**: 675-704
* **URL**: [https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9133.12459](https://onlinelibrary.wiley.com/doi/abs/10.1111/1745-9133.12459)
* **Tags**: #comps_exam, #crim501, #policing, #social_network_analysis
* **PDF Attachments**:
  * [ouelletNetworkExposureExcessive2019.pdf](zotero://open-pdf/library/items/ATBXJ3AE)

## Abstract

Research Summary In this study, we investigate how a police officer's exposure to peers accused of misconduct shapes his or her involvement in excessive use of force. By drawing from 8,642 Chicago police officers named in multiple complaints, we reconstruct police misconduct ego-networks using complaint records. Our results show that officer involvement in excessive use of force complaints is predicted by having a greater proportion of co-accused with a history of such behaviors. Policy Implications Our findings indicate officers’ peers may serve as social conduits through which misconduct may be learned and transmitted. Isolating officers that engage in improper use of force, at least until problematic behaviors are addressed, seems to be critical to reducing police misconduct and department-wide citizen complaints. Future studies should be aimed at investigating how social networks shape police misconduct and the ways network analysis might be used to diffuse intervention strategies within departments.

## My notes

### Introduction

- Officer involvement in excessive use of force is predicted by having a greater proportion of co-accused with a history of such behaviors.
    
- Police need good relationships with civilians to do their job effectively and excessive force harms those relationships. Previous research focused on individual characteristics or organizational characteristics but not social network dynamics.
    
- Mixed results as to the effects of individual-level variables (e.g. race) -> perhaps due to differential shift assignments.
    
- Organizational research focuses on police hyper-masculinity and confrontational culture -> authors argue police agencies do not teach misconduct so transparently even if it’s an unfortunate (predictable) by-product of the culture. Learned through formal/informal social interactions.
    
- Consider police misconduct a form of deviance, behavior diverging from the expressed mission of police institutions, then like other forms of deviance it’s a learned social behavior a la [[differential association]].

### Data and Methods

- This paper uses the complaint data from the Invisible Institute. 8,624 officers named in more than one complaint from 2007 to 2015.
	- #question #disagree By only including officers with one complaint, are they missing those officers who were never subsequently complained against? Failed cultural transmission.
- Look at officer misconduct networks -> all co-accused officers named in the same complaint with the focal officer.
    
- **Variables**:
	- Proportion of officers in complaint network with a prior use of force complaint.
	- Mean years of service in the complaint network.
	- Gender/racial ethnic composition.
	- Individual-level controls (race, gender, tenure).
	- Try to control for exposure to citizens and high-crime neighborhoods using officer rank and unit variables (specialized or non-specialized unit).
	- Control for the year of the complaint to account for complaint filing policy change.
    
- **Method**: Officers can experience an event (involvement in UOF) more than once. There’s dependence between events. Extend [[hazard models]] to include a [[frailty component]] (analogous to random effects, accounting for unobserved variability within individuals over time).
    
- **Results**:
  
	- Being male increases odds of being involved in a future use of force complaint.
	  
	- Experience has accumulating returns on reducing the likelihood of being involved in a use of force complaint.
	  
	- The number of solo prior complaints is positively related to the likelihood of being involved in a future use of force complaint.
		- However, the number of prior **use of force** complaints is negatively related to the likelihood of being involved in a future use of force complaint.
		  
	- As the number of co-accused officers in your prior complaint increases, the smaller the likelihood you will be involved in a future use of force complaint.
	  
	- Race, rank, unit, and mean experience in the network were not statistically significantly related to the likelihood of being involved in a future use of force complaint.

	- **Big, headline finding** -> The higher the number of officers who had a use of force complaint (in your prior complaint), the greater the likelihood of your involvement in a future use of force complaint. **Big coefficient size** as well.
	 
	- One big finding is that the percentage of your co-offenders who are female greatly decreases the odds of being involved in a future use of force complaint -> odd policy recommendation, greater exposure to female officers. Additionally it is younger and less experienced officers who are at the highest risk for future UOF complaints (are these effects mediated by assignment though, where you are assigned).
    
- **Future Research**:
	- Information on the complainants and outcomes of the complaints has lots of missingness. I could check and verify this perhaps.
	- Information on officer beat and other geographic assignments are useful controls.
	- #paper_idea 