---
type:
  - Note
aliases:
  - Mutual Information
  - mutual information
  - mutual information index
  - Mutual Information Index
  - Mutual information index
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #information_theory #shannon_entropy 

See [[Shannon entropy]] to help understand the building blocks which got us here.

$$MI(X, Y) = \sum_{i=1}^n{ \sum_{j=1}^m{p(x_i, y_j) \times log_b[\frac{p(x_i, y_j)}{p(x_i)p(y_J)}]}} \tag{Mutual Information}$$
Mutual information quantifies the notion about how much information one variable communicates about another variable. Unlike conditional entropy, it is symmetric.

Building off of what we know from Shannon entropy, mutual information can also be considered the reduction in uncertainty about some variable $X$ (expected reduction in the number of yes/no questions needed to guess $X$) after observing $Y$.

I will note here that continuous variables are a bit harder to work with. It is not as straightforward as simply substituting in integrals for summation symbols. You will not get all the nice properties you get with discrete variables e.g., you can get negative information with continuous variables. The reason for the conceptual difficulties is that you are dealing with infinities and events with probability equal to zero.

Also note that for discrete events with 0 probability: $$\lim_{x\rightarrow\infty} x\times log(x) = 0 $$
## Applications to segregation

Given some set of $N$ (e.g., schools) observations and *G* groups (e.g., racial groups), we can calculate the mutual information between them as a proxy for segregation. If groups and units were independent, the joint probability ($p(x_i, y_j)$) is equal to the marginal probability ($p(x_i) \times p(y_J)$) which is what you would expect if the variables were truly independent. Thus, we learn nothing about one variable by learning the values of the other variable, and the Mutual Information is 0. We would say, in this case, school attendance and the racial distribution of the students attending those schools is unrelated.

The upper bound for Mutual Information is $log_b(min(G, N))$. In other words, it will be the $log_b$ of the minimum length between the number of groups and the number of units.

You could then divide the Mutual Information Index by the highest possible Mutual Information to get a sense of how much segregation there is relative to how much there could ever possibly be.