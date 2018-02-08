# Imputation of missing data

Traditionally the most common way to deal with missing data has been:
- replace the missing with mean or median value. If categorical, the most common class or a separate missing value.
- include a missing indicator variable
- exclude observations when one or more variable values are missing

## Applications

## Recent papers
### arxiv archive
- 
### ICML archive
### ICLR archive
- Jan 2018, [Deep Sensing: Active Sensing using Multi-directional Recurrent Neural Networks](https://openreview.net/pdf?id=r1SnX5xCb)
- Nov 2016, [Recurrent Neural Networks for Multivariate Time Series with Missing Values](https://openreview.net/pdf?id=BJC8LF9ex)
Deals with health care data, informative missingness, i.e., the missing values and patterns provide rich information about target labels in supervised learning tasks (e.g, time series classification)

Older papers:
- Using Gaussian Mixture Models with EM - Using generative model to fill in the missing
[Supervised learning from incomplete data via an EM approach](http://papers.nips.cc/paper/767-supervised-learning-from-incomplete-data-via-an-em-approach.pdf)

- [Efficient EM Training of Gaussian Mixtures with Missing Data](https://arxiv.org/pdf/1209.0521.pdf) - Combining a discriminant algorithm with the generative Gaussian mixture model works better than the Gaussian mixture alone

- [Recurrent Neural Networks for Missing or Asynchronous Data]() - Unlike in the case of probabilistic models (e.g. Gaussian) of the missing variables, the network does not attempt to model the distribution of the missing variables given the observed variables. Instead it is a more "discriminant" approach that fills in the missing variables for the sole purpose of minimizing a learning criterion

- Feature set embedding strategy for classification with missing data - [Feature Set Embedding for Incomplete Data](https://papers.nips.cc/paper/4047-feature-set-embedding-for-incomplete-data.pdf). Instead of considering examples as feature vectors, they consider examples as sets of (feature, value) pairs which handle the missing feature problem more naturally. In order to classify sets, they propose a new strategy relying on two levels of modeling. At the first level, each (feature, value) is mapped onto an embedding space. At the second level, the set of embedded vectors is compressed onto a single embedded vector over which linear classification is applied.

- Causal graphical models depicting the data generating process can serve as a powerful tool for analyzing missing data problems when data is not missing at random (MAR) - [Graphical Models for Inference with Missing Data](https://papers.nips.cc/paper/4899-graphical-models-for-inference-with-missing-data.pdf)

- [Speech Recognition with Missing Data using Recurrent Neural Nets](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.72.6699&rep=rep1&type=ps)

- [On Missing Data Hybridizations for Dimensionality Reduction](https://link.springer.com/chapter/10.1007/978-3-642-38516-2_15) - Some kind of iterative approach with dimensionality reduction and something called as Unsupervised Nearest Neighbours

- [Multi-directional Recurrent Neural Networks: A Novel Method for Estimating Missing Data](http://roseyu.com/time-series-workshop/submissions/TSW2017_paper_12.pdf) - more recent

Miscellaneous:

- [Distributed Probabilistic Learning for Camera Networks with Missing Data] (https://papers.nips.cc/paper/4629-distributed-probabilistic-learning-for-camera-networks-with-missing-data.pdf)

- https://www.iro.umontreal.ca/~lisa/pointeurs/delalleau+al-emgaussian-2008-poster.pdf

- [A Unified Framework for Missing Data and Cold Start Prediction for Time Series Data (https://chrisdxie.github.io/papers/NIPS_TS_Workshop_Cold_Start.pdf)

- [Missing Data Imputation for Time-Frequency Representations of Audio Signals](http://paris.cs.illinois.edu/pubs/smaragdis-jsps10.pdf)
