---
type:
  - Note
aliases:
  - Surprise
  - information content
  - Information Content
  - Self-information
  - Self-Information
  - self-information
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #information_theory #shannon_entropy

## Surprise

Before we can discuss entropy, we need to understand [[surprise]]. Let us prime our intuition. Suppose you have three boxes with different amounts of differently colored balls in each box. Let's say we have only two types of balls: red and blue. Box 1 has a lot of red balls and very few blue balls. Box 2 has a lot of blue balls and very few red balls. Box 3 has an equal amount of each type of ball.

If you were to pick a ball from box 1, you would not be surprised if you picked a red ball, but you would be surprised if you picked a blue ball. Notice how there is a high probability of picking a red ball but a low probability of picking a blue ball. Thus, we want to encode in our definition of surprise is that it is inversely related to probability.

## Formal axioms

[[Claude Shannon]] wanted to encode a few properties about information using some axioms:

1. An event with probability 1 is completely unsurprising thus it should have a surprise of 0. Similarly, an event with probability 0 is impossible. If it were to happen, it would be infinitely surprising.
2. The amount of surprise given some event happens should be monotonically decreasing in probability. As demonstrated above, the two are inversely related. The higher the probability that something happens, the less surprising that it does happen.
3. If two independent events are measured separately, the total amount of surprise is the sum of the surprise of the individual events.

He went on to demonstrate that given those requirements, the equation governing surprise should be:
$$I(X) = log( \frac {1}{p(x)}) $$

where where $I(X)$ is read as the information or surprise given by event X happening and $p(x)$ is the probability of $X$ happening. Note that the range of this function is $[0, \infty]$ so you can never have negative surprise.

The relationship is fractional to indicate the relationship is an inverse.

The $log()$ function is useful for achieving several of the properties Shannon laid out. It helps us deal with cases where the probability of an event is equal to 1 (and 0). It also allows us to add surprises versus having to multiply them.

For example, suppose you have 1,024 discrete events which could happen all with the same probability. The surprise of any one of those events happening would be: $$log_2 (\frac {1}{\frac{1}{1024}}) = 10$$
10 *shannons* or *bits*. We say *shannons* or *bits* because we use base 2.

Suppose now, we have another 1,024 discrete events which all could also happen with the same probability. The surprise of any one of those events happening would also be 10 *shannons*. Assuming these two events are independent, the joint surprise of both events happening would be 20 *shannons*. Using the *log()* function allows us to add these values together. If we were to use $\frac{1}{p(x)}$, we would have to multiply our results together to get an accurate understanding of the new amount of surprise: $$\frac{1}{\frac{1}{1024}} * \frac{1}{\frac{1}{1024}} = 1048576$$
Notice that $$log_2 \frac{1}{\frac{1}{1048576}} = 20$$
The basic arithmetic of logarithms.

A final note on calculating surprise. You will often see the formula for surprise simplified to: $$ I(X) = -log_b[p(x)]$$