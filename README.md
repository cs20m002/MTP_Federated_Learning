## Title 
Federated learning for multi-class classification based on proxy data and GMMs.

## Introduction
With an increase in phones and gadgets as the primary computing devices in daily activity
for many people.[6; 2 ]. The robust hardware detectors on these devices (including ai
cameras, microphones, GPS, etc. ) added that these are on-the-go devices. One
can carry it everywhere, meaning they have access to massive private data. So, a
model trained on such data can provide a better user experience by powering more
intelligent applications.[ 4 ]. Since the data is confidential and private, there are risks and
responsibilities for holding it in some centralized location.
There is already a machine learning technique that allows users to learn a model without
disclosing their data; collaboratively. This technique is termed federated learning.[ 5 ].
Since the teaching is the happened by an open federation of participating devices ( we
call them local clients ) coordinated by a client-server with an appropriate load. Each
client has a local dataset ( which can be constant or variable in every iteration ) that is
never revealed to a central server. Instead of sending the local dataset to central server,
each client trained the current global model maintained by the central sever and only
update like parameters or weights are communicated. This adheres to the application of
the principle of focused collection or data minimization proposed by the 2012 White
House report on the privacy of consumer data.[3 ] Since these parameters or weights are
specific to improve the central model, so once it is applied, there is no need to store it.
The main advantage of federated learning is the decoupling of training the model from the
need for direct access to the client’s private data. Still, some trust from the coordinating
servers is also required. However, for our application, where data privacy is of utmost
importance, federated learning can significantly reduce privacy risk by limiting the attack
surface to only clients.
Our primary contributions are 1) an implementation of the one-shot learning using
GMMs for the generation of proxy data according to the federated learning paradigm
and 2) an improvisation of silhouette coefficient (a measure of similarity of a data point
is within-cluster (cohesion) compared to other clusters (separation)) 3) an extensive
empirical evaluation of the proposed approach. More precisely, we used a vanilla
federated learning paradigm. The catch is instead of training a stochastic gradient
descent(SGD), we fitted GMMs to the training data and sent the parameters to a central
server for sampling. We perform extensive experiments on this approach, both on IID
and non-IID data distribution.

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


