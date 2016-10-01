---
layout: single
title: "Deep Neural Nets: Pediatric Hand Radiographs"
author: Vanessa Sochat
excerpt: "Performance of a Deep Neural Network Model in Assessing Skeletal Maturity on Pediatric Hand Radiographs" 
categories: deep-learning
header:
  teaser: "projects/deep-learning/bone-age.png"
sidebar:
  nav: "docs"
---

## Team:

 - Matthew Chen
 - David B. Larson, MD, MBA
 - Matthew P. Lungren, MD, MHA
 - Safwan Halabi, MD
 - Curtis P. Langlotz, MD, PhD

<figure>
  <img src="/images/projects/deep-learning/bone-age.png"/>
</figure>


## Training Details

(4363 images)

### Architecture

 - Deep Residual Network
 - 50 layers
 - Adam SGD optimizer
 - Decaying learning rate
 - Pre-trained Weights

<figure class="align-left">
  <img src="/images/projects/deep-learning/neural-net-bone-age.png"/>
<small>Larson, DB, Chen, MC, Lungren, MP, Halabi, S, Langlotz, CP. Performance of a Deep Neural Network Model to Assess Skeletal Maturity on Pediatric Hand Radiographs. Annual Conference on Machine Intelligence for Medical Imaging (SIIM MIMI). Society for Imaging Informatics in Medicine, Alexandria, VA, 2016
</small>
</figure>

### Data Pre-Processing

#### Training Time

 - Random rotations
 - Random crops
 - Random contrast
 - Random Left Right Flips
 - Mean subtraction

### Test Time

 - Ten fixed crops
 - Mean subtraction

