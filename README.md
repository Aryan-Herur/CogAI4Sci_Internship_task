# CogAI4Sci_Internship_task
This repository contains the Jupyter Notebook for implementing memory recall and consolidation using a Modern Hopfield Network and a VAE as detailed in the work "***A Generative Model of Memory Construction and Consolidation***."

## Tools Used
### The primary frameworks used here include:
* Torch - To build the MHN and VAE
* Numpy - Linear algebra
* os - File management

## The Objective
The purpose of this code is to emulate the working of the human brain, including the short-term memory recall of the hippocampus, memory consolidation as seen in the neocortex, and the process of hippocampal replay, i.e., the training of the neocortex to understand the latent space better and store long-term memory.

## Methodology
### The following steps briefly explain the algorithm in the Jupyter Notebook:
1. 40,000 images from the MNIST dataset are encoded in the Modern Hopfield network (MHN), and the reconstruction matrix is learned through Hebbian Learning.
2. 40,000 samples of Gaussian noise are fed to the MHN to generate stored memories.
3. A Variational Auto Encoder (VAE) is trained on these memories to reconstruct the original images, thereby learning the latent space. (Memory Consolidation)
4. Now random noisy inputs are fed to the MHN to reconstruct an image (Recall by the Hippocampus) and to the VAE for the same purpose (Recall by the Neocortex).

## The Official Paper and Repository
The official paper can be found [here](https://www.nature.com/articles/s41562-023-01799-z).  
The official GitHub repository for this paper can be found [here](https://github.com/ellie-as/generative-memory).
