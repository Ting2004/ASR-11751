---
typora-copy-images-to: ./assets
---

# Forward-backward Algorithm for HMM

9/25/2024

---

### Distributions mentioned last time...

![image-20240925155622470](./assets/image-20240925155622470.png)

On a diagram like this:

- the first posterior distribution is the probability of a path given the exact state at the exact time stamp
- the second posterior distribution is the probability of a path given a state transition point between exact two time stamps

![image-20240925155659831](./assets/image-20240925155659831.png)



-> use **forward probability** and **backward probability**





## Forward Backward Probability

![image-20240925160016433](./assets/image-20240925160016433.png)

### Conditional Independence Assumption

- given the HMM model, we can simplify the probability
  - it is *assumption* based on the model

![image-20240925160558154](./assets/image-20240925160558154.png)

![image-20240925160752898](./assets/image-20240925160752898.png)

{forward} * {Gaussian distribution} * {backward} * {transition}

[IMPORTANT]





### Forward Algorithm

- derive the first one

- recursively compute the next

![image-20240925161720106](./assets/image-20240925161720106.png)

- complexity $O(J^2T)$



### Backward Algorithm

![image-20240925163003182](./assets/image-20240925163003182.png)







### Baum-Welch Algorithm

![image-20240925163107557](./assets/image-20240925163107557.png)

