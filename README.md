# GCN-tutorial

Tutorial on GCN using Python on Keras with Coda dataset. The original code can be found at https://github.com/tkipf/keras-gcn but with some minor changes for improving the code's readability. I also put some notes alongside the code so to break it down what each part of it is doing. 

The most interesting part is how the author defined the class GraphConvolution (GraphConvolution.build = core) in graph.py. 

Obs: This code is not intended to reproduce the experiments of the original paper [Semi-Supervised Classification with Graph Convolutional Networks](https://arxiv.org/abs/1609.02907). It only serves as a high-level illustration of the inner workings of the algorithm. 

## Dataset
- Coda 

## Problem
- Multi-class classification. That is, classify machine learning papers that have no labels so far into one of the 7 categories. This problem framework can be thought of semi-supervised learning.  

## Algorithm
- Graph Convolutional Network. Perform convolution operations on a graph using the information embedded into each node. The main idea is to "look" at neighboor nodes and update the currently embedded information into a higher or lower dimensional space by performing a ReLU or softmax operation. 
     - A: graph structure. 
     - X = [x_1, x_2, ..., x_n]^T: one-hot encoded paper list
     - x_i: list of important words contained in the i-th paper
     
## Dependencies
- Python 3.x
- keras (1.0.9 or higher)
- **TensorFlow** or Theano
- Jupyter Notebook
