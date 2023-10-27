```
type: Meeting
date: 2023-10-26
```

## Ability to discuss and share results

- The Census takes data security pretty seriously, and it has very strict rules on what can/cannot be communicated and how results can leave the data center.

	- Basically any kind of result which emerges from statistical analysis (e.g., a descriptive table, a regression analysis, a scatterplot) must go through formal disclosure review. They have a whole 50 page packet outlining the process. Basically, you work with Emily pretty closely to make sure your results can be released publicly. For regression analysis, this would involve generating the size of the samples involved in the estimation (e.g., if you estimate a logistic regression model with 2 categorical independent variables, you would need to generate the sample sizes for how many people were 0/1 on the dependent variable, the number of people in each category, and then a cross-tab for the dependent variable and each independent variable). My understanding is that you basically create specifically formatted sample size tables demonstrating the sample sizes undergirding whatever analysis you are doing.  

	- Geographic-based analyses are also pretty strictly monitored. You cannot ever disclose results for particular geographic areas (basically any geographic area with a population below 500,000). So for example, you would not ever be able to disclose (even through a disclosure review), that Middlesex County in NJ had 100 people arrested in October 2017. Regression-based analyses with geographic areas are allowed since you are pooling together a large amount of geographic areas. Emily was less sure if a "relative ranking" table/chart could be released (e.g., New Jersey has a lower arrest rate than South Dakota without actually saying the arrest rates).  

	- Emily talked a little about how some research teams have used differential privacy and noise-based infusion methods to release some results which otherwise would not have been released. But these cases are infrequent and are evaluated on a more case-by-base basis.  

- The first disclosure review memo you draw up typically will take 4-6 weeks to review. After the first disclosure review, it usually takes 2-3 weeks to review. It can happen a lot sooner. It just depends on how complicated the analysis is.  

- Until such results go through disclosure review, we cannot discuss them outside the data center.  

- What can we talk about outside the data center? Well we can talk about what Emily called "sign and significance results". The direction of effects, how precisely they are estimated. This also encompasses more general things like sample sizes, number of missings, column headers/variable availability, data linkage results. **But** we can only talk about the **sign and significance** results with people who have data access on our project **in person** (or I suppose if we both happened to be in a data center and we call each other using the landlines in the data center). We cannot Zoom/email/call/etc. these results to each other even though we all have data access.  

- Thankfully there is an expedited review process for sign and significance disclosure reviews. Basically as long as one's results are sufficiently general or narrowly focused on things like sample sizes, number of missings, etc. you can apply for the sign + significance disclosure review. The turnaround for this is usually a few days.

- All handwritten notes/typed notes/code must stay in the data center unless they go through some form of disclosure review. I believe this process is much faster than the disclosure review process for results. I think Emily just quickly scans through to make sure your notes/code do not explicitly talk about any results.  

	- As a side effect of this rule, any **sign + significance** results when discussed **in person** can only be from memory (unless they have gone through some form of disclosure review).  

- User-provided data and externally written code are easy to add to the data center. Simply send them to Emily, and she will upload them to your project workspace.  
    
- And then basically when you are in the data center, no tech is allowed. Cellphones and smart watches are allowed, but you cannot use them for communication purposes nor can you use the Internet. None of the computers have Internet access. You can listen to music you have downloaded ahead of time, though.  

## Working in the environment

* If you have ever used a VPN, it is very similar to that experience. You log on to a computer in the Data Center, you then VPN into another computer, and you have access to the computing environment and your data. The actual work area is large. They have about 20 computers. You could work as a group there and discuss things (as long you kept your voices down since it is in a library).
  
* Working on the data center computer seemed pretty straightforward. It did not feel slow or laggy. The computer you VPN into is running a version of the Linux OS so it is not the same as Windows or Mac, and there will be a slight learning curve. I found the documentation to be useful and up-to-date, though. I have a lot of familiarity in terms of working with Linux (and in fact I mainly work on a Linux computer), but I do not think the environment is that hard to navigate at all.
  
	* One small hurdle will be in developing a workflow to work with the data. When working in the VPN, when you launch an application (R, Stata), you can launch it in compute mode or interactive mode. Interactive mode opens a GUI, and you load the data and work with the data in the ways we are all used to. However, the environment is limited computationally (small amount of memory and processing power). This is by design. Computationally intensive tasks should be launched in compute mode. In compute mode, the GUI is not invoked. You simply run your script or do file, and then it outputs the desired results. The key will be specifying ahead of time (in your script or do file) where and how the results should be stored.
  
* The data files for all the requested data sets were there (ACS, Census, Mortality, CJARS). None of it was linked as far as I can tell. I believe we must do all the linking (sad). They provide crosswalk files for linking the datasets. It will require some time to wrap our heads around the data naming structures, data locations, and structure of the individual data files and tables. Especially the variable headers which do not have intuitive names so we will have to refer to the documentation a lot.

* They have R, Stata 18, SAS, Matlab, and Python all installed (and a few other programs as well). The data are provided in as a SAS dataset. The options are to: 1) use SAS to transform the data into a data format one can use with other programming languages/software, or 2) They have a utility called Stat Transfer which allows one to transform the data without using Stata. So I used this utility, and it seemed to work well. I was able to easily access it in R. They have a process in place, as well, for requesting additional R/Stata/Python packages as one needs.