---
title: "Inside Information: Sorting, Screening, and Signaling Desistance in Correctional Settings"
author:
  - Shawn Bushway
  - Carolyn J. Heinrich
  - Janos Toevs
year: 2026
journal: CrimRxiv
type: Article
study type: Theory
sample size:
sampling frame:
sample location:
study method:
study start:
study end:
dependent variable(s):
main independent variable(s):
hypotheses supported?:
---
[Zotero entry](zotero://select/items/@bushwayInformationSortingScreening2026)
**Tags**: #signaling_theory #prison_rehabilitation #postdoc_signaling_edovo 
## Abstract
Correctional staff face an inference problem. They are legally required to support and recognize an incarcerated person's efforts at rehabilitation, but they cannot directly observe their true identity or the effort they are making to change. This paper applies the concepts of sorting, screening, and signaling from information economics to create an analytical framework to guide improved correctional practice. The paper first classifies the incarcerated population into three “types”: committed criminals, conformists, and desisters. Sorting at intake in the criminal justice system reliably separates out committed criminals using criminal history, but desisters are often pooled with conformists because intent to change is a dynamic, self-authored process that no risk-needs instrument, however refined, is designed to capture. Screening, whereby staff provide explicit rewards for behavioral compliance, fosters a safer environment, but likewise does not differentiate conformists from desisters, as desisters would comply even without incentives. Signaling solves this problem by shifting the initiative to the inmate, whereby desisters would be motivated to act without any guarantee of an explicit reward. Continued investment in ever more refined risk-prediction tools misdiagnoses the problem: risk instruments detect risk, not intent to change. Parole boards and correctional institutions should shift weight at reclassification and release away from risk scores and toward screens and primarily signals, including microsignals such as consistent attendance at a work assignment or willingness to accept added supervision. Correctional institutions should expand access to voluntary rehabilitative opportunities without layering on extrinsic rewards. They should also avoid the temptation to make programs mandatory, which dilutes their value as a signal. This framework for solving the inference problem generalizes beyond incarceration settings to any situation where decision makers need to identify desisters among a group of people with criminal history records.

## Notes

* **Quick history** --> Rehabilitation was seen as the central goal of the corrections system. Research in the late 1970's and early 1980's cast doubt on this goal i.e., *nothing works*. Philosophically, deterrence and incapacitation became the central goals of the corrections system. Actuarial, risk-based management and [[determinate sentencing]] practices emerged in response (although I would argue this was not all bad). In the early 2000's, rehabilitation re-emerged not only as an unattainable ideal but something which would be achieved. Specifically, the [[risk-need-responsivity]] (RNR) model emerged.
  
* The **first problem** faced in correctional institutions is *correctly classifying* individuals. It is impossible to directly observe an individual's risk and potential for change. When every individual, regardless of true risk or potential for change, self-selects into a program because of extrinsic benefits, this creates a [[pooling equilibrium]] where participation in the program communicates no information to principals (i.e., decision-makers) as to the true type of the agent. The **second problem** is *correctly identifying individuals who are trying to change their type*. Their *type* can change while in a correctional facility, and it is very hard (similar to the problem above) to identify who is simply going through the motions for a reward vs. who is actually working to change.
  
* Authors identify 3 types:
	* **Committed criminals**: Their sense of self involves identifying as a criminal. They are very resistant to change and interpret programming primarily through its costs and benefits.
	* **Conformists**: Their sense of self is not rooted in criminal behavior. They engaged in criminal behavior due to early socialization or peer influence. They are responsive to incentives and will change their behavior. However, this group also has the highest uncertainty as to whether or not they want to truly desist or not.
	* **Desisters**: These individuals are redefining their sense of self and want to move away from their criminal identity.
	  
* What tools do we have to identify individual types as well as the likelihood of switching between types?
  
	* **Sorting**: Principals directly attribute a type onto an agent on the basis of some test. It is different from the other tools primarily due to the fact that the agent is an object of inspection (**note**: the degree to which an external reward is placed on the test is the degree to which sorting becomes screening as individuals will respond to the incentives and become more active participants rather than objects of observation) rather than someone actively participating in something. Typically, an assessment is done which translates the test performance into a type prediction. This allows for an efficient allocation of resources. Those individuals most likely to respond to programming (i.e., conformists) will have the resources targeted at them. Of course, different tests can be more or less informative of the true type of an individual. The issue is that current sorting techniques conflate *risk* or *criminal history* with *intent* or *desire to change*. Risk is largely static while intent is dynamic, and the two may (or may not) be correlated. I.e., what a person did is not a reliable indicator of how they want to proceed moving forward. There are no observable characteristics we can use to really differentiate intent to change between two, otherwise similar looking individuals.
	  
	* **Screening**: A principal posts a contract (i.e., a benefit tied to an action) and let's the agent's choice reveal their type. Formalizing things a bit using [[principal-agent theory]]:
		* $V$ is the value of moving a conformist to a desister.
		* The principal's job is to foster actions and efforts $a$ which increase $V$. Examples of $a$ include participating in an educational course or participation in a rehabilitation program.
		* However, $V$ is not observable. Principals design some proxy measures of $V$ called $P$ which should reveal how much an agent's actions and efforts are contributing to $V$.
		* However, the effect of an action $a$ on $P$ (called $g$) will not be the same as the effect of $a$ on $V$ (called $f$). For example, an individual may participate in an educational course (increasing $P$) but only for its extrinsic rewards (e.g., improved cell conditions) and thus does not increase $V$. Individuals are rewarded for actions which increase $P$ but not $V$.
		* We can try and come up with a way of to determine how much weight to assign to a proxy measure. Basically, it is a function of: 1) $S_{p}$ which is the signal to noise ratio in $P$ or how well $g$ measures $P$, and 2) ${cos(\theta)}$ which is the angle between $f$ and $g$ are how aligned $f$ and $g$ in their effect on both increasing (or decreasing) $V$ and $P$, respectively.
			* I.e., $S_p*cos(\theta)$ is the simplified form of the equation (i.e., it is missing parts, but this is the part emphasized in the paper). If the $f$ and $g$ are the same, then the value becomes 1 and the optimal incentive weight is purely a function of the signal to noise ratio. If $f$ and $g$ are completely different, then the value becomes 0 and no weight should be assigned to this proxy measure.
				* As $cos(\theta)$ increases (meaning $f$ and $g$ are more similar, meaning there is less opportunity to game $P$ and not actually increase $V$), all else equal, more weight should be placed on the proxy.
		* The problem is we often have little information on both $g$ and $f$ making it hard to determine the extent to which they align. The extent to which a proxy measure is gameable is largely unknown ahead of time but can be learned by principals by observing agents (and thus may necessitate constant changing and re-weighing of proxy measures). Agents are typically able to identify and learn very quickly how to game $P$ so that they exert an efficient amount of effort to increase $P$ but not $V$ (thus hiding their type effectively). Assuming two proxy measures $P_1$ and $P_2$ (and simplifying the mathematical notation from the paper):
			* $V = f_0 * a_0 + f_1 * a_1 + f_2 * a_2$
			* $P_1 = g_0 * a_0 + g_1 * a_1 + w_1 * a_1$
			* $P_2 = g_0 * a_0 + g_2 * a_2 + w_2 * a_2$
			* $g_i = f_i + n_i$
			* $a_0$ is the effort common to both of the proxy measures and to $V$, $a_1$ is common to $P_1$ and $V$, and $a_2$ is common to $P_2$ and $V$. The principal wants to rewards these efforts as they increase $V$. **Complication 1:** A proxy measure may not perfectly capture how productive an effort is (i.e., $n_i \neq 0$). **Complication 2**: An agent can take an action which increases some $P$ but not $V$ i.e., when $w_i > 0$.
			  
	* **Signaling**: Agents can signal to principals to give them more reliable information about their type particularly for desisters to differentiate themselves from conformists. Desisters are not motivated by extrinsic rewards. In order for signalling to work, desisters must: **1)** have their signals be observable, and **2)** the signal must be costly (i.e., high level of $a$) so as to deter conformists from participating and faking their type (although, ideally, the costs would decrease as the agent moves further and further along the desistance pathway).
		* As conformists try to game the system, desisters must constantly change their signals so they remain useful.
		* The same signal can mean different things in different settings. Access and environmental factors dictate the quality of a signal e.g., **1)** availability of educational programming and expectations around participation in the programming, **2)** in some prison settings, peers may determine participation is a sign of weakness which increases the costs for individuals with otherwise similar intentions of desisting, **3)** on a similar note, a principal may determine access to a program is only available to those who snitch or become informants.
		* The ability for an agent to have their signal be observed is not a given. E.g., institutional staff often interpret agent actions for the parole board (agents may not have as much of an opportunity to present their case themselves) or reentry programs often have to sell the individual to employers rather than the agent doing it themselves.
		  
* **Implications**
	* Create more opportunities for agents to signal. Allow for agents to craft their own narratives and bypass third parties to present the signals themselves.
	* Of course, compliance with programming (regardless of one's type) may be desired for its own benefits (i.e., creating a safer prison environment). This can lead to competing desires e.g., prison guard vs. parole officer (one cares more about creating a safe environment whereas the other is more concerned about ascertaining their true type).
	* Sorting by risk is very valuable at intake and for initial assignment of resources. However, once assigned, the risk assessment tool is no longer as useful. Risk assessments are not good at identifying potential for change. Risk assessments should not be used for forecasting recidivism (which is a combination of current risk and potential for change). Improved risk assessment tools will not be able to overcome this fundamental limitation.
	* Principals will often rely on proxies which are more easily measured biasing principals towards compliance rather than desistance.
	* The mix of screens and signals should be determined by the relative mix of types in the population.
	* More attention should be placed on *microsignals* i.e., principals should be open to seeing signals where they previously had not (e.g., nature of one's work assignment while incarcerated).
	* We must work toward applying these principles outside of prison, as well, to help tailor programming post-release and during reentry.