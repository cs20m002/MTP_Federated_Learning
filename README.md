## Title 
An implementation of the one-shot learning using GMM for generation of proxy-data according to federated learning paradigm 

## Description
Traditional machine learning approaches require centralizing the training data on a single machine or in a data center. This process has a disadvantage in terms of privacy or data of users who provide the training data. All this data is directly visible to one central entity that collected it. Also, all the data is stored at a single location where the model will be trained therefore there is a chance of a single point of failure due to data loss or theft, hazard, natural disaster, etc... also in terms of an organization; this is expensive; maintaining and running the data-centre for 24 X 7. So, to solve this problem, a new form of machine learning technique is evolved called Federated learning. Federated Learning enables edge devices to collaboratively learn a shared prediction model while keeping all the training data on the device, decoupling the ability to do machine learning from the need to store the data in the cloud.

## Aim
To study federated learning paradigm using proxy-data by means of GMMs.

## Datasets Used
1. Extended MNIST ( keras.tensorflow.datasets.mnist.load_data() ) 
2. CIFAR-10 ( use first 5 cell of SGD_CIFAR10.ipynb for data preparation if locally downloaded)

## Methodology
1. FedAvg (as decribed in the paper Communication-Efficient Learning of Deep Networks from Decentralized Data.)
2. Proxy-Data using GMMs (Expectation-Maximization (EM) algorithm according to the vanilla federated learning paradigm.) 

## Requirements
●	 Pyhton > 3.5
●	 Tensorflow > 1.4

## Installation
1. Install Anaconda using this link https://www.anaconda.com/products/distribution
2. Create New Environment other than base
3. Install keras and tensorflow using uninstalled tab
4. Install Jupyter Notebook
5. Run Notebook

## Results
  
                                  Accuracy
FedAvg (over 300 iteration)         70%
GMM (one-shot)                      72%


## Summary


## Conclusion
Our experiments show that federated learning is feasible and can be made pratical, as GMM(one-shot) can train high-quality models by building good GMMs using Silhoutee method which help in cluster prediction as demontrated by our results on varity of models for spatial data.

## Resources
  ## Blogs
  1. https://ai.googleblog.com/2017/04/federated-learning-collaborative.html
  2. https://www.tensorflow.org/tutorials
  3. https://www.kdnuggets.com/2021/11/difference-distributed-learning-federated-learning-algorithms.html
  
  ## Papers
  ●	Article 1 https://arxiv.org/pdf/1602.05629.pdf
  ●	Article 2 https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8889996
  ●	Article 3 https://ieeexplore.ieee.org/document/9463409
  ●	Article 4 https://ieeexplore.ieee.org/document/9492755
  ●	Article 5 https://ieeexplore.ieee.org/document/9121290
  ●	Article 6 https://ieeexplore.ieee.org/document/9260194
  ●	Article 7 https://openreview.net/pdf?id=7x_47XJULn


