## Introduction

Traditional RL conducts numerous simulation and saves to RAM prior to uploading to GPU to train policy DNN. Using data uploaded to GPU, the policy network is updated to conduct simulations. This method causes inefficient data transfer and bottleneck effect of GPU resulting time-consuming computation. On the other hand, Issac Gym takes advantage of GPU computation which eliminates data transfer between RAM and GPU. Although CPU can perform parallel simulation, the physical number of cores are limited while GPU consists of more number of cores which are suitable for parallel simulation. 

## Memory Management

Let's assume a simulation enviroment with 