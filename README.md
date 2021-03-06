# Awesome Distributed Deep Learning

<p align="center">
	<img src="https://img.shields.io/badge/stars-30-brightgreen.svg?style=flat"/>
	<img src="https://img.shields.io/badge/forks-12-brightgreen.svg?style=flat"/>
	<img src="https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat">
</p>

A curated list of awesome Distributed Deep Learning resources.

## Table of Contents

### **[Frameworks](#frameworks)** 

### **[Blogs](#blogs)** 

### **[Papers](#papers)**  
<!--
### **[Tutorials](#tutorials)**  

<!--
### **[Miscellaneous](#miscellaneous)**  
<!--
### **[Contributing](#contributing)** -->

## Frameworks

1. [MXNet](https://github.com/dmlc/mxnet) - Lightweight, Portable, Flexible Distributed/Mobile Deep Learning with Dynamic, Mutation-aware Dataflow Dep Scheduler; for Python, R, Julia, Go, Javascript and more.
2. [go-mxnet-predictor](https://github.com/songtianyi/go-mxnet-predictor) - Go binding for MXNet c_predict_api to do inference with pre-trained model.
3. [deeplearning4j](https://github.com/deeplearning4j/deeplearning4j) - Distributed Deep Learning Platform for Java, Clojure, Scala.
4. [Distributed Machine learning Tool Kit (DMTK)](http://www.dmtk.io/) - A distributed machine learning (parameter server) framework by Microsoft. Enables training models on large data sets across multiple machines. Current tools bundled with it include: LightLDA and Distributed (Multisense) Word Embedding.
5. [Elephas](https://github.com/maxpumperla/elephas) - Elephas is an extension of Keras, which allows you to run distributed deep learning models at scale with Spark.
6. [Horovod](https://github.com/uber/horovod) - Distributed training framework for TensorFlow.

## Blogs

1. [Keras + Horovod = Distributed Deep Learning on Steroids](https://medium.com/searchink-eng/keras-horovod-distributed-deep-learning-on-steroids-94666e16673d)
2. [Meet Horovod: Uber’s Open Source Distributed Deep Learning Framework for TensorFlow
](https://eng.uber.com/horovod/)
3. [distributed-deep-learning-part-1-an-introduction-to-distributed-training-of-neural-networks/](https://blog.skymind.ai/distributed-deep-learning-part-1-an-introduction-to-distributed-training-of-neural-networks/)

## Papers 
### General:
1. [Demystifying Parallel and Distributed Deep Learning: An In-Depth Concurrency Analysis](https://arxiv.org/abs/1802.09941):discusses the different types of concurrency in DNNs; synchronous and asynchronous stochastic gradient descent; distributed system architectures; communication schemes; and performance modeling. Based on these approaches, it also extrapolates the  potential directions for parallelism in deep learning. 
### Synchronization:
#### Synchronous techniques: 
1. [Deep learning with COTS HPC systems](http://ai.stanford.edu/~acoates/papers/CoatesHuvalWangWuNgCatanzaro_icml2013.pdf): Commodity Off-The-Shelf High Performance Computing (COTS HPC) technology, a cluster of GPU servers with Infiniband interconnects and MPI.
2. [FireCaffe: near-linear acceleration of deep neural network training on compute clusters
](https://arxiv.org/abs/1511.00175): The speed and scalability of distributed
algorithms is almost always limited by the overhead of communicating between servers; DNN training is not an exception to
this rule. Therefore, the key consideration this paper makes is to reduce communication overhead wherever possible, while not degrading the accuracy of the DNN models that we train. 
3. [SparkNet](https://arxiv.org/abs/1511.06051): Training Deep Networks in Spark. In Proceedings of the
International Conference on Learning Representations (ICLR).
4. [1-Bit SGD](https://www.microsoft.com/en-us/research/publication/1-bit-stochastic-gradient-descent-and-application-to-data-parallel-distributed-training-of-speech-dnns/): 1-Bit Stochastic Gradient Descent and Application to
Data-Parallel Distributed Training of Speech DNNs, In Interspeech 2014.
5. [Scalable Distributed DNN Training Using
Commodity GPU Cloud Computing](https://s3-us-west-2.amazonaws.com/amazon.jobs-public-documents/strom_interspeech2015.pdf):It introduces a new method for scaling up distributed Stochastic Gradient Descent (SGD) training of Deep Neural
Networks (DNN). The method solves the well-known communication bottleneck problem that arises for data-parallel SGD because compute nodes frequently need to synchronize a replica of the model.  
6. [Multi-GPU Training of ConvNets.](http://arxiv.org/abs/1312.5853): Training of ConvNets on multiple GPU's
#### Stale-Synchronous techniques: 
1. [Model Accuracy and Runtime Tradeoff in Distributed Deep Learning](https://doi.org/10.1109/ICDM.2016.0028): A Systematic
Study.
2. [A Fast Learning Algorithm for Deep Belief Nets.](https://www.cs.toronto.edu/~hinton/absps/fastnc.pdf):A fast learning algorithm for deep belief nets
3. [Heterogeneity-aware Distributed Parameter Servers.](http://net.pku.edu.cn/~cuibin/Papers/2017%20sigmod.pdf): J. Jiang, B. Cui, C. Zhang, and L. Yu. 2017. Heterogeneity-aware Distributed Parameter Servers. In Proc. 2017 ACM International Conference on Management of Data (SIGMOD ’17). 463–478.
4. [Asynchronous Parallel Stochastic Gradient for Nonconvex Optimization](https://papers.nips.cc/paper/5751-asynchronous-parallel-stochastic-gradient-for-nonconvex-optimization.pdf):X. Lian, Y. Huang, Y. Li, and J. Liu. 2015. Asynchronous Parallel Stochastic Gradient for Nonconvex Optimization. In Proc. 28th Int’l Conf. on NIPS - Volume 2. 2737–2745. 
5. [Staleness-Aware Async-SGD for Distributed Deep Learning](https://www.ijcai.org/Proceedings/16/Papers/335.pdf): W. Zhang, S. Gupta, X. Lian, and J. Liu. 2016. Staleness-aware async-SGD for Distributed Deep Learning. In Proc. Twenty-Fifth International Joint Conference on Artificial Intelligence (IJCAI’16). 2350–2356.
#### Asynchronous techniques: 
1. [A Unified Analysis of HOGWILD!-style Algorithms.](https://arxiv.org/abs/1506.06438): C. De Sa, C. Zhang, K. Olukotun, and C. Ré. 2015. Taming the Wild: A Unified Analysis of HOGWILD!-style Algorithms. In Proc. 28th Int’l Conf. on NIPS - Volume 2. 2674–2682.
2. [Large Scale Distributed Deep Networks](https://papers.nips.cc/paper/4687-large-scale-distributed-deep-networks.pdf): J. Dean et al. 2012. Large Scale Distributed Deep Networks. In Proc. 25th International Conference on Neural Information Processing Systems - Volume 1 (NIPS’12). 1223–1231.
3. [Asynchronous Parallel Stochastic Gradient Descent](https://arxiv.org/abs/1505.04956):J. Keuper and F. Pfreundt. 2015. Asynchronous Parallel Stochastic Gradient Descent: A Numeric Core for Scalable Distributed Machine Learning Algorithms. In Proc. Workshop on MLHPC. 1:1–1:11. 
4. [Dogwild!-Distributed Hogwild for CPU & GPU.](https://papers.nips.cc/paper/7289-hogwild-gibbs-can-be-panaccurate.pdf): C. Noel and S. Osindero. 2014. Dogwild!-Distributed Hogwild for CPU & GPU. In NIPS Workshop on Distributed Machine Learning and Matrix Computations.
5. [GPU Asynchronous Stochastic Gradient Descent to Speed Up Neural Network Training.](https://arxiv.org/abs/1312.6186): T. Paine, H. Jin, J. Yang, Z. Lin, and T. S. Huang. 2013. GPU Asynchronous Stochastic Gradient Descent to Speed Up Neural Network Training. (2013). arXiv:1312.6186
6. [HOGWILD!: A Lock-Free Approach to Parallelizing Stochastic Gradient Descent](https://arxiv.org/abs/1106.5730): B. Recht, C. Re, S. Wright, and F. Niu. 2011. Hogwild: A Lock-Free Approach to Parallelizing Stochastic Gradient Descent. In Advances in Neural Information Processing Systems 24. 693–701.
7. [Asynchronous stochastic gradient descent for DNN training](https://ieeexplore.ieee.org/document/6638950): S. Zhang, C. Zhang, Z. You, R. Zheng, and B. Xu. 2013. Asynchronous stochastic gradient descent for DNN training. In IEEE International Conference on Acoustics, Speech and Signal Processing. 6660–6663.

**Feedback: If you have any ideas or you want any other content to be added to this list, feel free to contribute.**
