---
type:
  - Note
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #information_theory

## Average surprise 

See [[surprise]] to gain a better intuition for what is happening here.

The Shannon entropy is the average level of *surprise* or *information* or *uncertainty* given by a random variable's set of possible outcomes. So given some random variable $X$ with a probability function $p: X \rightarrow [0,1]$ and $n$ possible outcomes, the Shannon entropy is given by:
$$
H(X) = -\sum_{i=1}^n {p(x) \times log_b[p(x)]} \tag{Entropy}
$$
$$
H(X) = \sum_{i=1}^n {p(x) \times log_b(\frac{1}{p(x)})} \tag{Intuitive Entropy}
$$
It is the summation (across all possible events) of the probability of some event happening multiplied by the surprise of that event happening. Then, you take the negative of that value which is related to the definition of surprise.
## Joint and Conditional Entropy

Joint entropy is the amount of surprise we would get if some event $x$ and $y$ were to both happen. In this case, the more surprising something is, the more uncertain it is (higher surprise = higher uncertainty). Additionally, the more surprising something is, the more information you might need to communicate it happened (higher surprise = higher information). No surprise (ha ha), it is an extension of our above definition of entropy.
$$H(X, Y) = -\sum_{i=1}^n\sum_{j=1}^m p(x_i, y_j) \times log_b[p(x_i, y_j)] \tag{Joint Entropy}$$
$$H(X, Y) = \sum_{i=1}^n\sum_{j=1}^m p(x_i, y_j) \times log_b(\frac{1} {p(x_i, y_j)}) \tag{Intuitive Joint Entropy}$$

Conditional entropy quantifies the amount of information needed to describe the outcome of some random variable $X$ given that $Y$ is known. Notice how in step 1, we state rather directly that entropy is the expected information value (i.e., expected surprise, expected uncertainty, average information, average surprise, average uncertainty).
$$ H(X|Y) = \mathbb{E}[\frac{1}{log_b[p(x|y)]}] \tag{Step 1}$$
$$ H(X|Y) = -\mathbb{E}[log_b[(p(x|y)]] \tag{Step 2}$$
$$H(X|Y) = -\sum_{i = 1}^n{\sum_{j = 1}^m{p(x_i, y_j) \times log_b[p(x_i|y_j)]}} \tag{Step 3}$$
$$H(X|Y) = -\sum_{i = 1}^n{\sum_{j = 1}^m{p(x_i, y_j) \times log_b(\frac{p(x_i, y_j)} {p(x_i)})}} \tag{Step 4}$$

Note that conditional entropy is not symmetrical.
## New definition

We are going to introduce some new ways of interpreting surprise and entropy to help us further our understanding. Suppose $x$ is a random variable drawn from some probability distribution $P$. You know the probability distribution, and you are tasked with guessing the value of $x$ using as few yes/no questions as possible. The optimal search strategy will be akin to using a [[binary search]] where you divide the space in half and ask if the value is greater than the midpoint. So the Shannon entropy can also be thought of as the the number of yes/no questions you would need to ask, on average, to guess the random variable. **It is the amount of information, on average, needed to specify the value of a random variable.**

We can see this through the logic of the binary search. If you have 16 elements, and you guess the midpoint (and are wrong), you go to 8 elements. Then 4. Then 2. Then finally 1. This is the worst-case scenario. Given 16 elements, you had to make 4 guesses to find the right answer: $log_2(16) = 4$ or $log_2(n) = k$ where $k$ is the number of iterations needed to find the right value in an array of size $n$.
