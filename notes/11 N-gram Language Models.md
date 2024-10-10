---
typora-copy-images-to: ./assets
---

# 11 N-gram Language Models

10/7/2024

___

### Language Model in ASR Pipeline

- $\arg\max{P(W|O)}$: find the best word sequence given observation
  - most probably word sequence

![image-20241007160411148](./assets/image-20241007160411148.png)



### Markov Assumption

- assume the probability of $w_i$ is only dependent of $n$ previous words, $W_{i-n+1:i-1}$
  - n-gram assumption

![image-20241007161116286](./assets/image-20241007161116286.png)

note that *ML* means *Maximum Likelihood* here





#### Unigram

- just the product of probability of all words
  - no context/condition
  - order does not affect final score



#### Bigram

- only consider the previous word
  - $p(\text{I want to go to}) = p(\text{I}) p(\text{want} | \text{I}) p(\text{to} | \text{want}) \cdots$





### Zero-count problem

- n-gram (e.g. bigram) trellis is very sparse
  - many word combo have zero count from the corpus
  - and we compute the product... oops everything ZERO-OUT
- use **smoothing**



#### Laplace Smoothing (Additive Smoothing)

![image-20241007162258419](./assets/image-20241007162258419.png)

- $\alpha = 0$ is Maximum Likelihood
- $\alpha \rightarrow \infin$ is uniform distribution



  

#### Jelinek Mercer Smoothing (Interpolation Smoothing)

![image-20241007162432968](./assets/image-20241007162432968.png)

- still need to satisfy the *sum-to-one* property, so we assign $\lambda$ and $1-\lambda$ as coefficient





#### Kneser-Ney Smoothing

![image-20241007163038927](./assets/image-20241007163038927.png)

- The example of "reading glasses" and "reading Francisco"
  - "Francisco" has a high count, so it has higher unigram probability
  - BUT "Francisco" is always associated with "San"
  - and Kneser-Ney takes it into account







