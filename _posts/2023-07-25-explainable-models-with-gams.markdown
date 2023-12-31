---
title: "Trading off complexity and epxlainability with GAMs"
layout: post
date: 2023-07-25 22:10
tag: 
- GAM
- explainability
headerImage: true
projects: true
hidden: true 
description: "GAMs are awesome and here is why"
category: project
author: viktoriiaoliinyk
externalLink: false
---

Understanding the inner workings of ML algorithms is key to unlocking informed decision-making and responsible AI deployment. Explainability transforms opaque algorithms into interpretable insights, enabling us to trust, improve, and navigate the decisions guided by AI systems. Unlike black-box ML algorithms, Generalised Additive Models (GAMs) offer a structured framework that captures sophisticated relationships between variables in a transparent manner offering balance between complexity and explainability.

---
### 1. What is GAM
![Imgur](https://i.imgur.com/mfai6yK.png)
<figcaption class="caption">GAMs are just a generalisation of Linear Regression</figcaption>

---
### 2. Pros
<ul>
    <li><b>Interpretability</b>: Additivity makes possible interpretation of the marginal impact of a single variable independent of the values of the other variables</li>
    <li><b>Flexibility</b>: GAM can capture common nonlinear patterns that a classic linear model would miss</li>
    <li><b>Statistical nature</b>: You get confidence intervals for weights, significance tests, prediction intervals and much more</li>
</ul>

### 3. Cons
<ul>
    <li>Any link function that is not the identity function complicates the interpretation. Interactions also complicate the interpretation </li>
    <li>Nonlinear feature effects are either less intuitive (like the log transformation) or can no longer be summarized by a single number (e.g. spline functions)</li>
    <li>Performance of tree-based ensembles like the random forest or gradient tree boosting is in many cases is better</li>
</ul>

