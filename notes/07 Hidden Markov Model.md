---
typora-copy-images-to: ./assets
---

# Hidden Markov Model

9/23/2024

___

## HMM Hidden Markov Model [IMPORTANT]

- based on the EM (Expectation Maximization) algorithm
  - introduce latent variable
  - complete data likelihood
  - auxiliary function (E-step)
  - parameter estimation (M-step)
- Pros
  - monotonic behavior (of Likelihood (likelihood must be increased
    during the iterations. Easy to debug)
  - easy to distribute
- Cons
  - local optimum
  - initialization dependent



### Introduction of latent variable

- introduce **alignment variable** ($S$) as the latent variable
- $p(O|\theta) = \sum_{s}p(O, S|\theta)$



### Complete data likelihood

![1727121525180](./assets/1727121525180.png)

In the first order HMM model, we assume the current observation is independent of all previous observations; the current state is only dependent of ONE previous state.

[IMPORTANT]

![image-20240923160214575](./assets/image-20240923160214575.png)



#### Actual functions for each probability term

- NN
- plug in an *appropriate* distribution

![image-20240923160915609](./assets/image-20240923160915609.png)

![image-20240923160934212](./assets/image-20240923160934212.png)





#### Diagonal Covariance vs. Full Covariance

![image-20240923161102616](./assets/image-20240923161102616.png)



Consider performance, use Gaussian mixture with multiple diagonal covariance

![image-20240923161441829](./assets/image-20240923161441829.png)







### Auxiliary Function

- Expectation of the complete data likelihood with respect to the posterior distribution of a latent variable sequence
- $Q(\theta, \theta') = \sum_{s \in S} p(s|O, \theta')\log{p(O, s | \theta)}$
  - summation over all possible sequences
  - 3 states per phoneme, TOO MANY possible sequences
- 



==revisit==







### Parameter Estimation 

- we have an auxiliary function
  - take derivative and find argmax











