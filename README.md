# COMP8536 Group Project

This repository contains the group project for COMP8536. Our team members include:

- Zezhou Wang
- Angxuan Li
- Guangxing Mi
- Xinni Song

We are all students at the Australian National University, pursuing a degree in **Machine Learning and Computer Vision**.

## Project Introduction

In the domain of 3D computer vision, Neural Radiance Field (NeRF) \cite{mildenhall2021nerf} has shown its capability in complex 3D representation and view synthesis. Through optimizing the weights of the specially designed MLP based on positional encoding and differentiable volume rendering, NeRF learns a volumetric representation of the scene, allowing the model to synthesize highly realistic views of different camera angles. NeRF has many variations and advanced versions, which expand the application fields of the model. For example, the benchmark model Nerfacto \cite{tancik2023nerfstudio}, which has optimized the sampler and the encoder components of the original model while reduced the layers of the MLP, improves its anti jitter ability and reconstruction efficiency. In this paper, we are aimed to evaluate and improve the performance of the Nerfacto model by modifying the positional encoding, loss function, and model architectures and testing on different versions of datasets.


The experiments in this paper mainly evaluate and improve the benchmark model Nerfacto from the following aspects: 

- Replace the original Mean Squared Error (MSE) loss function with the Huber loss [Huber, 1992](#) to enhance the model's anti-jitter ability.
- Use Integrated Positional Encoding (IPE) that considers sample size instead of the original hash encoding to focus on fine details.
- Implement the self-attention [Vaswani et al., 2017](#) and skip connection (residual learning) [He et al., 2016](#) mechanisms to enhance training accuracy and stability.


In terms of datasets, we conducted the experiments on the official Poster dataset \cite{tancik2023nerfstudio} and the custom Peppa dataset, and launched multiple tests on different model improvements. 
