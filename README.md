# Generate faces with GAN
Generate faces using Generative Adversarial Networks

This project has been done as a part of the [Udacity Deep Learning Nanodegree](https://eu.udacity.com/course/deep-learning-nanodegree--nd101)

## Project's objective
The objective of this project has been to generate images containing human faces after training on a dataset. In order to achieve this, a Generative Adversarial Network has been used.

## About the model's architecture
The GAN (Generative Adversarial Network) is composed of a Generator and a Discriminator. The role of the Generator is to generate fake images which are then evaluated by the Discriminator. Mainly the Generator tries to fool the Discriminator in order to label the fake generated images as fakes. The Discriminator takes some images as input and it classifies them into 2 categories: fake or real.

**The Generator's architecture:**
![alt text](https://github.com/andreipop95/face-generation-gan/blob/master/generator_architecture.png)

As it can be observed in the above image, there are 3 types of layers as descrbed below: <br/>
**Linear layer** - takes a random generated array and then converts it into an image of depth 3 <br/>
**Convolutional layer** - increases the depth of the images and decreases the widht and height <br/>
**Batch normalization layer** - normalizes data after each convolutional layer <br/>


**The Discriminator's architecture:**
![alt text](https://github.com/andreipop95/face-generation-gan/blob/master/generator_architecture.png)

For the discriminator, the following layers have been used: <br/>
**Transpose convolutional layer** - increases the width and the hight of the image by decreasing the depth <br/>
**Batch normalization layer** - normalizes data after each convolutional layer <br/>
**Linear layer** - the final layer that gices the result for an image - if it is fake or real <br/>

## Resources used
[Celebrity faces dataset](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)

## Results obtained
After training for 50 epochs, the following images have been generated:
![alt text](https://github.com/andreipop95/face-generation-gan/blob/master/results.png)

## How to run the current project

The prerequisites in order to set the project on a local machine are:
* [Github](https://gist.github.com/derhuerst/1b15ff4652a867391f03)
* [Anaconda and python](https://docs.conda.io/projects/conda/en/latest/user-guide/install/windows.html)

1. Git clone the repository
   
   `git clone https://github.com/andreipop95/face-generation-gan.gitt`

2. Create a conda environment using python 3.5. As an alternative for package management, pip can be used

   `conda create --name <your_project_name> python=3.5`
   `source activate <your_project_name>`

3. Install needed packages
   
   `conda install <package_name_1 package_name_2...>`
   
4. Install jupyter notebook
   
   `conda install jupyter notebook`
 
5. Lunch the notebook
   
   `jupyter notebook dlnd_face_generation.ipynb`
