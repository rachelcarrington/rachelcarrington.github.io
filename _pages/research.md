---
permalink: /research/
title: "Research"
author_profile: true
redirect_from: 
---

{% include base_path %}

## Post-selection inference for changepoints

Changepoint detection is the problem of detecting a change in time series (or other ordered) data. Commonly we are interested in changes in the mean or variance, although other types of changepoints may also be of interest. [This link](https://www.lancaster.ac.uk/~romano/teaching/2425MATH337/1_intro_cusum.html) provides an introduction to detecting changes in the mean.

One important problem in changepoint analysis is uncertainty quantification. Suppose we have a time series and have applied a changepoint algorithm. We then want to know, how certain can we be that the detected changes are real? Naively, we can calculate the probability that the change in mean before and after a given point is greater than the one we observe. However, the locations we are choosing to test (i.e. the detected changes) were chosen using the data, and this means re-using the same data will give biased results (we will be more likely than we should be to conclude the change is real).

Post-selection inference is one solution to this problem. This is where we calculate the probability of observing a larger change _conditional on_ the information in the data used to choose where to test. In other words, if we consider all possible datasets that would result in the same set of detected changepoints when we apply our algorithm, in what proportion of them would observe a more extreme result?

In practice, we often have to condition on additional information (beyond just the detected changepoints) to implement this, but this can reduce the power of the test (so we are less likely to detect a genuine change).  This first paper is an attempt to mitigate this (building on the work of [Hyun et al. (2021)](https://onlinelibrary.wiley.com/doi/abs/10.1111/biom.13422?casa_token=SwXGqLJHlS0AAAAA:IGBLvkuL0UTGWg7j_ucYpO9ilXf6FVKNPus-CMdKzEcOrl7VUexy_bqRwzct2_s62sz9e56vNgIEqcry) and [Jewell et al. (2022)](https://academic.oup.com/jrsssb/article-abstract/84/4/1082/7073271)), providing a method which allows us to reduce the amount of information we condition on, and hence obtain a test with greater power:

[Improving Power by Conditioning on Less in Post-selection Inference for Changepoints](https://link.springer.com/article/10.1007/s11222-024-10542-1).
Rachel Carrington and Paul Fearnhead. _Statistics and Computing_ 35(8), (2025).

In this second paper, we extend the ideas in our previous paper as well as those of others, to develop a post-selection procedure for detecting changes in variance. This is more challenging, as it is not possible in many cases to calculate exact p-values. We develop here two methods for constructing p-values for detected changes in variance, which are applicable to different types of changepoint algorithms. When the p-values cannot be explicitly calculated, we make use of Gaussian process methods to approximate them.

[Post-selection inference for quantifying uncertainty in changes in variance](https://link.springer.com/article/10.1007/s11222-026-10881-1). Rachel Carrington and Paul Feanhead. _Statistics and Computing_ 36(128), (2026).

The [changepointsPSI](https://github.com/rachelcarrington/changepointsPSI) R package can be used to detect changes in changes in mean, variance, or slope and to implement post-selection inference.

## Urban mapping using multiple data sources

[Urban mapping in Dar es Salaam using Angle-Based Joint and Individual Variation Explained](https://academic.oup.com/jrsssc/article/75/1/247/8236692). Rachel Carrington, Ian Dryden, Madeleine Ellis, James Goulding, Simon Preston and David Sirl. _Journal of the Royal Statistical Society: Series C_ 75(1), (2026).

Producing accurate estimates of deprivation in urban areas is challenging, particularly in areas where traditional census or household survey data is unavailable or difficult to obtain, or where the urban environment is rapidly changing. We here combine novel forms of data, which are more readily available --- satellite imagery and mobile phone data --- for the city of Dar es Salaam, Tanzania. We use dimension reduction techniques to identify low-dimensional structure within the dataset, and to produce deprivation estimates for sub-divisions within the city.

The related GitHub repository can be accessed [here](https://github.com/rachelcarrington/ajive-dar-es-salaam).

## Word embeddings

[Invariance and identifiability issues for word embeddings](https://proceedings.neurips.cc/paper/2019/file/44885837c518b06e3f98b41ab8cedc0f-Paper.pdf). 
Rachel Carrington, Karthik Bharath and Simon Preston. _Advances in Neural Information Processing Systems (NEURIPS)_, 32. (2019).

My PhD thesis can be accessed here: [Mathematical Aspects of Word Embeddings](https://eprints.nottingham.ac.uk/65089/)
