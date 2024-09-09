---
permalink: /research/
title: "Research"
author_profile: true
redirect_from: 
  - /md/
  - /papers.html
---

### Post-selection inference for changepoints

Uncertainty quantification in detected changepoints is an important problem: given a set of time series (or other ordered) data, we apply a changepoint algorithm (for example binary segmentation or PELT) to detect changes. We then want to know: how certain can we be that the detected changes are real? Since we have already used the data to estimate the locations of the change, re-using the same data to calculate uncertainty will introduce bias, and so we need to use post-selection inference to calculate uncertainty conditional on the locations of estimated changes. However, it is challenging to do this in ways that are both accurate and computationally efficient.

[Improving Power by Conditioning on Less in Post-selection Inference for Changepoints](https://arxiv.org/pdf/2301.05636.pdf).
Rachel Carrington and Paul Fearnhead. _arXiv preprint arXiv:2301.05636_, (2023).

In this paper, we consider the univariate piecewise constant mean model. We extend existing methods by showing how we can use Monte Carlo sampling to obtain p-values for detected changepoints that have greater power than those generated using existing methods, whilst still being uniform under the null hypothesis.

[Post-selection inference for quantifying uncertainty in changes in variance](https://arxiv.org/pdf/2405.15670). Rachel Carrington and Paul Feanhead. _arXiv preprint arXiv:2405.15670_, (2024).

The piecewise constant variable model is more challenging, as it is not possible in many cases to calculate exact p-values. We develop here two methods for constructing p-values for detected changes in variance, which are applicable to different types of changepoint algorithms. When the p-values cannot be explicitly calculated, we make use of Gaussian process methods to approximate them.

### Urban mapping using AJIVE

[Urban mapping in Dar es Salaam using AJIVE](https://arxiv.org/pdf/2403.09014). Rachel Carrington, Ian Dryden, Madeleine Ellis, James Goulding, Simon Preston and David Sirl. _arXiv preprint arXiv:2403.09014_, (2024).

Producing accurate estimates of deprivation in urban areas is challenging, particularly in areas where traditional census or household survey data is unavailable or difficult to obtain, or where the urban environment is rapidly changing. We here combine novel, more readily available forms of data -- satellite imagery and mobile phone data -- for the city of Dar es Salaam, Tanzania. We use dimension reduction techniques to identify low-dimensional structure within the dataset, and to produce deprivation estimates for sub-divisions within the city.

### Word embeddings

[Invariance and identifiability issues for word embeddings](https://proceedings.neurips.cc/paper/2019/file/44885837c518b06e3f98b41ab8cedc0f-Paper.pdf) 
Rachel Carrington, Karthik Bharath and Simon Preston. _Advances in Neural Information Processing Systems (NEURIPS)_, 32. (2019).

My PhD thesis can be accessed here: [Mathematical Aspects of Word Embeddings](https://eprints.nottingham.ac.uk/65089/)
