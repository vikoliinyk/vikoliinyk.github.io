---
title: "Why it's important to build fair and ethical ML models"
layout: post
date: 2023-08-30 10:10
headerImage: false
tag:
- fairness
- responsible AI
star: false
category: blog
author: viktoriiaoliinyk
description: Introduction to fair and ethical AI
---

For many years, others made vital decisions for us, and now, machine learning often takes the lead.

Within justice, defendants get scores predicting future crime risks, guiding decisions on bail, sentencing, and parole. In finance, statistical tools dictate our mortgage approvals and credit ratings. In business, ML sifts through job applications. In education, it determines our school admissions.

Beyond the critical, ML subtly shapes our culture daily. From search engines to news feeds to ads, it shapes our knowledge and views.

However, erratic or flawed decisions can stifle our ambitions and opportunities. We trust that admissions, job, and loan decisions hinge on truly pertinent factors.

Algorithmic decision making carries the risk of discrimination. Given the reliance on algorithms, it is important to ensure:
* They do not discriminate against groups on the basis of sensitive attributes: race, gender, age, religious beliefs, etc.
* They do not encode or replicate societal biases
* Their outcomes do not go unchecked, especially where risk of discrimination is present.

---
### 1. ML cycle --- how ML predictions change the world

![Imgur](https://i.imgur.com/RGSKyyg.png)
<figcaption class="caption">Cycle of ML models</figcaption>

Historically, our records often mirror society's biases, stereotypes, and unequal demographics. Analyzing such data risks perpetuating these very issues.

Thus, it's paramount that our models don't amplify these prejudices, especially related to race, gender, or other sensitive traits. Simply put, they shouldn't just echo society's ingrained biases, nor should they introduce new ones.

The reliability of evidence-based decision-making hinges heavily on the quality of the evidence itself. Just because machine learning thrives on data doesn't guarantee its decisions will be accurate, consistent, or just.

---
### 2. What can we do about it?

So, how can we ensure decisions are made with integrity and for the right motives?

The answer lies in rigorous data standards: ample examples to reveal nuanced patterns; a wide variety of examples to represent diverse scenarios; well-documented examples to provide machine learning with dependable ground truth, and so forth.

To maintain these standards, we should consistently review the model's decisions, ensuring fairness metrics are met—similar to how we monitor the model's overall performance over time.

---
### 3. What to read next
- [Blog to kick off](https://towardsdatascience.com/a-tutorial-on-fairness-in-machine-learning-3ff8ba1040cb)
- Moritz Hardt's [talks and course](https://fairmlclass.github.io/)
- Fairness for ML developers by Google: [article](https://developers.google.com/machine-learning/fairness-overview/)
- [Algorithmic decision making and the cost of fairness](https://arxiv.org/abs/1701.08230) by Sam Corbett-Davies et al.
- Seminal [Equality of Opportunity in Supervised Learning](https://arxiv.org/abs/1610.02413) by Hardt et al. NeurIPS 2016
- [On Fairness and Calibration](https://arxiv.org/abs/1709.02012) by Pleiss et al. NeurIPS 2017
