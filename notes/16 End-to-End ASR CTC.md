---
typora-copy-images-to: ./assets
---

# 16 End-to-End ASR: CTC

11/6/2024

___

### CTC Condition

- when token length is too large
  - and the input feature is short
- may be because of
  - large down sampling
  - wrong data alignment

![image-20241106161652399](./assets/image-20241106161652399.png)

![image-20241106161932492](./assets/image-20241106161932492.png)





### Inference for CTC

- if using greedy search
  - the final $\arg\max$ is just $\arg\max$ at each point
  - we can parallel the decoding!
  - *non-autoregressive* model









### Shallow Fusion

LM shallow fusion with CTC

![image-20241106162427199](./assets/image-20241106162427199.png)









