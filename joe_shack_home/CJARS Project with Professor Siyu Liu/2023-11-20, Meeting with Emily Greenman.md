```
type: Meeting
date: 2023-11-20
```

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #CJARS #meeting 
## Review and disclosure

* Sign and significance ***should not*** be used for sample sizes and match rates, unfortunately. We would need to do a full disclosure review for these results. However because the results are relatively simple and straightforward, they should be able to be processed within a week or two. I would need to go through the full disclosure request process and create an excel table and all of that.
  
	* Additionally, I would need to separate out my *notes* (without any numbers) to be processed as a notes and program file disclosure request.
	  
	* Emily also said the disclosure review process for program files may be much longer during these busy months (and potentially moving forward). She was a bit confused about why the program disclosure requests would be taking longer moving forward, and she was also a bit skeptical they actually would take longer.
  
* October through November are usually the busiest months in terms of disclosure review because of deadlines. Things should ease up in January (unless the government shuts down).
  
* We are also a relatively new research team for the FSRDC in the sense that we are almost all fully remote. So Emily is still learning what the best way would be for us to collaborate and communicate. To that end, she did mention that we would be able to talk about numbers in a non-specific fashion. 
  
## PIK Matching

* CNUM/PID matching to multiple PIKs is a documented problem which results from the fact that the [[Person Identification Validation System]] (PVS) is probabilistic. People are not matched only in cases where there is an exact match. They match on records which clear some probability of certainty that it is the correct match. As a result, one CNUM/PID (one person) can match to multiple PIKs. Emily indicated there is SAS code (maybe STATA code) somewhere which details how to make the linked data table 1:1.
  
	* The other solution (which one researcher recommended that Emily talked to) was to drop all cases which matched to more than one PIK. They argued the quality (i.e., certainty) of the matches is not as good as in cases where the matches are 1:1. If the sample sizes are small enough, it may not wind up making that big of a difference in the final analysis. If the resulting analysis was going to be household-based, one might want to even drop the entire household when an individual did not have a PIK or matched to multiple PIKs.
  
* I also cleared some things up with Keith Finlay that you need to merge cjars_id with PIK to de-duplicate the cjars_id roster (which is very confusing). I am still confused about why, for example, dozens of records might match to the same cjars_id. 