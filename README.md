# Imputation of missing data

Traditionally the most common way to deal with missing data has been:
- replace the missing with mean or median value. If categorical, the most common class or a separate missing value.
- include a missing indicator variable
- exclude observations when one or more variable values are missing
- interpolation when it comes to time series

## Thoughts
It has a very broad application area - structured or timeseries data, images, audio. In terms of verticals, I see quite a few recent papers in the lifesciences/healthcare industry or using a medical dataset to demonstrate the algorithm. Other than the traditional approaches - EM, matrix completion, some form of RNNs, GANs and using auto-encoders have been part of the recent research. One other interesting perspective of missing data is when the data is multi-modal, meaning for some samples we have brain signal data and for some we have let's say brain scans.

## Recent papers
### arxiv archive
- Jan 2018, Yoshua Bengio et al. [Efficient EM Training of Gaussian Mixtures with Missing Data](https://arxiv.org/pdf/1209.0521.pdf) - Combining a discriminant algorithm with the generative Gaussian mixture model works better than the Gaussian mixture alone
- Nov 2017, [VIGAN: Missing View Imputation with Generative Adversarial Networks](https://arxiv.org/pdf/1708.06724.pdf)
- Dec 2016, [MISSING DATA IMPUTATION IN THE ELECTRONIC HEALTH RECORD USING DEEPLY LEARNED AUTOENCODERS](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5144587/)
- Nov 2016, [Recurrent Neural Networks for Missing or Asynchronous Data](https://arxiv.org/pdf/1606.01865.pdf) - Unlike in the case of probabilistic models (e.g. Gaussian) of the missing variables, the network does not attempt to model the distribution of the missing variables given the observed variables. Instead it is a more "discriminant" approach that fills in the missing variables for the sole purpose of minimizing a learning criterion
- Nov 2016, [Modeling Missing Data in Clinical Time Series with RNNs](https://arxiv.org/pdf/1606.04130.pdf)
- Oct 2016, [MISSING DATA IMPUTATION FOR SUPERVISED LEARNING](https://arxiv.org/pdf/1610.09075.pdf). This paper is mostly a comparison of results based on NNs, Random Forest, etc. after imputing missing data 

### ICML archive
- 2015, [Classification with Low Rank and Missing Data](http://proceedings.mlr.press/v37/hazan15.pdf)

### ICLR archive
- Jan 2018, [Deep Sensing: Active Sensing using Multi-directional Recurrent Neural Networks](https://openreview.net/pdf?id=r1SnX5xCb)
- Nov 2016, [Recurrent Neural Networks for Multivariate Time Series with Missing Values](https://openreview.net/pdf?id=BJC8LF9ex)
Deals with health care data, informative missingness, i.e., the missing values and patterns provide rich information about target labels in supervised learning tasks (e.g, time series classification)

### NIPS
- 2017, [Multi-directional Recurrent Neural Networks: A Novel Method for Estimating Missing Data](http://roseyu.com/time-series-workshop/submissions/TSW2017_paper_12.pdf)
- 2016, NIPS[A Unified Framework for Missing Data and Cold Start Prediction for Time Series Data](https://chrisdxie.github.io/papers/NIPS_TS_Workshop_Cold_Start.pdf)


## Criteria
1. Is it exciting to the team? Would not classify it as exciting but definitely something that needs our attention
2. Can it be framed as a strong capability (rather than an algorithm)? probably no
3. Is it a subject that is more possible now than in two years, and likely to be more possible/transformative still in a couple of years. That usually means some or all of the following things are true:
  i. There is excitement (ideally including concrete breakthroughs) in the research community - maybe
  ii. Economic constraints (e.g. hardware) have lessened/disappeared
  iii. There has there been a commoditization of tooling - no
  iv. Data is available (especially to FFL!) - using some kind of patient healthcare data might make an interesting usecase
4. Is it useful to our existing clients? yes
5. It is appealing to potential clients? yes
6. It it possible to build a prototype? 

Older or other papers:
- 2010, [Feature Set Embedding for Incomplete Data](https://papers.nips.cc/paper/4047-feature-set-embedding-for-incomplete-data.pdf). Instead of considering examples as feature vectors, they consider examples as sets of (feature, value) pairs which handle the missing feature problem more naturally. In order to classify sets, they propose a new strategy relying on two levels of modeling. At the first level, each (feature, value) is mapped onto an embedding space. At the second level, the set of embedded vectors is compressed onto a single embedded vector over which linear classification is applied.
- Using Gaussian Mixture Models with EM - Using generative model to fill in the missing
[Supervised learning from incomplete data via an EM approach](http://papers.nips.cc/paper/767-supervised-learning-from-incomplete-data-via-an-em-approach.pdf)
-  2017, [Missing Modalities Imputation via Cascaded Residual Autoencoder](http://cvlab.cse.msu.edu/pdfs/Tran_Liu_Zhou_Jin_CVPR2017.pdf)
- 2013, Causal graphical models depicting the data generating process can serve as a powerful tool for analyzing missing data problems when data is not missing at random (MAR) - [Graphical Models for Inference with Missing Data](https://papers.nips.cc/paper/4899-graphical-models-for-inference-with-missing-data.pdf)
- 2013, [On Missing Data Hybridizations for Dimensionality Reduction](https://link.springer.com/chapter/10.1007/978-3-642-38516-2_15) - Some kind of iterative approach with dimensionality reduction and something called as Unsupervised Nearest Neighbours
- 2011, [Missing Data Imputation for Time-Frequency Representations of Audio Signals](http://paris.cs.illinois.edu/pubs/smaragdis-jsps10.pdf)
- 2002, [Speech Recognition with Missing Data using Recurrent Neural Nets](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.72.6699&rep=rep1&type=ps)

Miscellaneous, a bit probably unrelated at times:
- [Distributed Probabilistic Learning for Camera Networks with Missing Data] (https://papers.nips.cc/paper/4629-distributed-probabilistic-learning-for-camera-networks-with-missing-data.pdf)
