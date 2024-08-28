# Introduction to Speech Recognition

8/28/2024

___



## Evaluation Metric

- Sentence error rate (strict)
- Word error rate (WER) 👑
  - by word edit distance
  - require word boundary
- Character error rate (CER) 👑
- Phoneme error rate
  - need a pronunciation dictionary
- Frame error rate ==?== 
- speed, computation complexity, latency...
- NIST speech recognition scoring toolkit



#### Edit distance

- ==Levenshtein distance algorithm==
  - setup table
  - initialize dummy values
  - calculate cost based on above, left and diagonal grids
  - find the best path from right-bottom
- characteristics
  - error rate could go above 100%
  - error break down is not unique (multiple best paths)
  - too many insertion - usually the end of the sentence is incorrect
  - too many deletion - usually noisy environment



Compared to ASR, other areas of speech study have way more and more complex metrics. 





## Before evaluation

### Text normalization - task dependent

- case sensitive?
- punctuations
- filtering words like, "ah, hmmm ..."





## Dataset and Benchmarks

may have different recording environments, style and transcribe

### Style

- read speech
  - read a prompt
  - free transcription, easy to collect
  - easy to anonymize
- spontaneous speech
  - record conversation
  - need manual transcription
    - tools: Audacity, Wavesurfer
  - need post-processing (anonymization, filter handling, etc.)

### Mic distance

- distance/close
- CHiME-3: read speech in noisy environment
- CHiME-6: spontaneous speech in noisy environment

### Available sources

![image-20240828163106942](C:\Users\tingc\AppData\Roaming\Typora\typora-user-images\image-20240828163106942.png)





