[//]: # (Image Reference)

[image1]: ./example.jpg "Generated Faces"

# Face Generation

## Project Overview

In this project, I defined and trained a DCGAN on a dataset of faces. The goal of this project is to get a generator network to generate _new_ images of faces that look as realistic as possble. The image below is a result of the training:

![example](https://user-images.githubusercontent.com/26524467/56185030-db4a6900-6039-11e9-8337-5d05ce5025ec.jpg)



## Project Instruction

### Instruction

1. Clone the repository and navigage to the downloaded folder.
	```
		git clone https://github.com/choonghee-lee/Face-Generation
		cd Face-Generation
	```
2. Open the `dlnd_face_generation.ipynb` file. Of course, you can find HTML version of the file.
	```
		jupyter notebook dlnd_face_generation.ipynb
	```
3. Read and follow the instructions! This repository does not include the dataset of faces. You can find and download it in the notebook.

## Project Information

### Contents

- Pre-processed Data
- Create a DataLoader
- Define the Model
	- Discriminator
	- Generator
	- Initialize the weights of your network
	- Build complete network
- Discriminator and Generator Losses
- Optimizers
- Training
- Training Loss
- Generator samples from training

### Model - Discriminator
| Layer | Input Dimension | Output Dimension | Batch Normalization|
|-------|-----------------|------------------|-------------|
|Conv1|3|64|False|
|Conv2|64|128|True|
|Conv3|128|256|True|
|Conv4|256|512|True|
|FC|2048|1|False|

### Model - Generator
| Layer | Input Dimension | Output Dimension | Batch Normalization|
|-------|-----------------|------------------|-------------|
|FC|100|2048|False|
|Deconv1|512|256|True|
|Deconv2|256|128|True|
|Deconv3|128|64|True|
|Deconv4|64|3|False|

### Libraries

The list below represents main libraries and its objects for the project.
- [PyTorch](https://pytorch.org) (Generator and Discriminator)

### Accelerating the Training Process

In the training phase, it takes your time too much so I recommend you to use a GPU to train the dataset of faces.

### Amazon Web Services

You can use Amazon Web Services to launch an EC2 GPU instance. (This costs money!)
