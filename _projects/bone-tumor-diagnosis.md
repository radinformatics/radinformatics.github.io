---
layout: single
title: "Bone Tumor Diagnosis Using A Naïve Bayesian Model Of Demographic And Radiographic Features"
author: Vanessa Sochat
excerpt: "Diagnosis of Bone Tumors using Radiographs" 
categories: machine-learning
header:
  teaser: "projects/machine-learning/bone-tumor.png"
sidebar:
  nav: "docs"
---

## Team:

- Bao H. Do, MD
- Rui Shu
- Curtis P. Langlotz, MD, PhD
- Christopher Beaulieu, MD, PhD

<figure>
  <img src="/images/projects/machine-learning/bone-tumor.png"/>
</figure>


## Training Details

- 811 annotated cases, 66 unique diagnoses
- Evaluated 3 overlapping subsets: 
  - **(Rare)** Minimum 5 examples of each diagnosis:
    710 cases, 29 unique diagnoses
  - **(Intermediate)** Minimum 18 examples of each diagnosis:
     559 cases, 14 unique diagnoses
  - **(Common)** Minimum 30 examples of each diagnosis:
     478 cases, 10 unique diagnoses


## Results

<figure class="align-left">
  <img src="/images/projects/machine-learning/bone-tumor-results.png"/>
</figure>

## Future Work

- Test against other machine learning algorithms and against human performance
- Incorporate published priors, e.g. Dahlin’s Bone Tumors
- Analysis of correlations between features
- Compare to image classification using deep learning
- Pair with feature extraction using deep learning
- Increase sample size, ideally N > 30 per diagnosis
