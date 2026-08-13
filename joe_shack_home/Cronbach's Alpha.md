## Overview
It is used to quantify the internal consistency of a survey item or some test. It basically measures how closely related a set of items in a group are. Scores range from 0 to 1, and researchers generally want to see a coefficient of 0.7 or greater to be certain the different questions are effectively measuring the same construct. Of course, the coefficient can also be too high which indicates the questions are redundant and maybe aren't capturing all the dimensions of the construct you are trying to measure (usually values at or above 0.95).

As a technical note, Cronbach's Alpha is only one type of [[coefficient of reliability]] (also known as coefficients of consistency or scale reliability coefficients).

Interpretation-wise, a high Cronbach's Alpha means when a participant gives a high response on one of the items, they are likely to also provide a high response on the other items. As an example, if someone had high self-esteem, and the items measured self-esteem, then they would have a high response on all items. More concretely, a value of 0 means there is no correlation between the items at all. Knowing the value of one response provides no information on the other items. On the other hand, a value of 1 means the items are perfectly correlated. Knowing the value of one response provides complete information on the other items.

You typically want to include at least 3 (and maybe even ideally 4) items when calculating Cronbach's Alpha. When you have two items, the equation basically simplifies to a correlation coefficient.
## Assumptions
In Psychology, much work has been done in trying to understand the relationship between observed scores and the unobserved constructs they claim to be measuring. [[True score theory]] posits: $$Y = T + E$$where $Y$ is the observed score, $T$ is the true score, and $E$ is the measurement error.  This equation has several assumptions baked into it:

1. The error must be randomly distributed. If errors are not randomly distributed but instead are systematically skewed (e.g., a scale constantly reads 2 lbs. heavier than an object actually is), then taking more measurements or averaging them will not correct the inaccuracy.
2. The errors must uncorrelated with each other. Common ways this assumption can be violated include *the fatigue effect* (e.g., if you measure reaction time and your subject gets tired, the errors across observations become correlated with time), *the halo effect* (e.g., if someone takes a personality test while in a good or bad mood, the errors across every question will be correlated with the shared mood), *instrument drift* (e.g., if a water quality sensor degrades over time, then the error again will be correlated with time).
3. The errors must be centered around 0 i.e., $E[error] = 0$ or the average amount of error should be 0.

Essentially, the measurement error should not exhibit any systematic patterns or biases which would skew the observed scores. Additionally, the test items when calculating Cronbach's Alpha should...

4. be unidimensional meaning all items are measuring the same underlying latent construct.
5. demonstrate [[tau-equivalence]] meaning they all should be measuring the same construct (basically same as the above unidimensionality requirement) **and** all have similar levels of precision and accuracy (i.e., each item contributes equally to the construct).
6. all be measured on the same scale and in the same direction (i.e., higher values indicate higher levels of the observed trait for all items). Although if the items are not all measured on the same scale, you can calculate the standardized Alpha's Cronbach.
	1. As will be discussed below, when calculating the standardized Alpha's Cronbach, you use correlation coefficients. Typically, one might assume you would use [[Pearson's Correlation Coefficient]]. However, when working with ordinal data (particularly data using [[Likert scales]]), it may make more sense to use the [[polychoric correlation coefficient]].  If your ordinal variable has five or more categories and is not heavily skewed, the Pearson coefficient and the polychoric coefficient often give similar results.
## Best practices for reporting
1. Typically, confidence intervals are calculated using [[bootstrapped confidence intervals]].
2. You can calculate [[corrected item-total correlations]] which is where you sum each item in the scale except for the focal item and observe how correlated the two items are. Items which have a correlation below 0.3 are usually considered suspect for inclusion in the scale.
3. In a similar vein, you can calculate the [[alpha if item deleted]] where the alpha coefficient is calculated with each item removed. Items whose removal increases the alpha would be considered suspect.
## Limitations
1. It can be artificially inflated by simply adding more items even if they measure different concepts.   
2. Cronbach's Alpha indicates if a set of questions are *reliable* (i.e., yield consistent scores or how consistently do these questions measure something), but it does not indicate if the set of questions is *valid* (i.e., it is not measuring what you claim it is measuring). Cronbach's Alpha assumes the measures are valid already (i.e., unidimensional ) and all equally contribute to the underlying construct (i.e., tau-equivalence).
	1. There are other methods of testing *validity* like examining the correlation matrices between items or comparing the distributions of the items. The distributions and correlations should be roughly equivalent and if not, this is preliminary evidence that the items are perhaps not measuring the construct or do not equally contribute. One can also conduct a [[Principal Component Analysis]], [[Exploratory Factor Analysis]], [[Confirmatory Factor Analysis]], and/or [[parallel analysis]] to further confirm.
	2. Other coefficients like [[McDonald's Omega Coefficient]] can be used which have less assumptions.
## Equations
$$\tag{Cronbach's Alpha}\frac{k}{k - 1}(1 - \frac{\Large{\sum\limits_{i = 1}^{k}\sigma_i^2}}{\Large{\sigma_t^2}})$$

$$\tag{Standardized Alpha's Cronbach}\frac{k\overline{r}}{1 + (k - 1)\overline{r}}$$
 where:
* $k$ is the number of items included.
* $\Large{\sigma_i^2}$ is the variance of item $i$.
* $\Large{\sigma_t^2}$ is the total variance of all items included in the scale.
* $\overline{r}$ is the average of all between item correlation coefficients.
## Useful sources
* https://rpubs.com/abova/alpha-cronbach