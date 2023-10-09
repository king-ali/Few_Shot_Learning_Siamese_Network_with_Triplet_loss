# Few Shot Learning Siamese Network with Triplet loss


## Introduction

One-shot learning is a challenging task in the field of computer vision and machine learning. Unlike traditional problems where a model is trained on a large dataset with numerous examples of each class, one-shot learning aims to recognize new classes with only a single or very few examples. Siamese Networks, combined with the Triplet Loss function, offer an effective approach to address this problem.

## One-Shot Learning

One-shot learning is a form of machine learning where a model is trained to classify objects or entities based on just one or a few examples per class. This is in contrast to conventional deep learning approaches that require a large dataset with abundant samples for each class. One-shot learning is particularly relevant in situations where acquiring a significant amount of data for each class is impractical or costly, such as in facial recognition, signature verification, or rare disease diagnosis.


## Siamese Networks

Siamese Networks are a type of neural network architecture that consist of two identical subnetworks, referred to as 'twins' or 'branches,' which share the same weights and architecture. Both branches of the Siamese Network share the same architecture, which is typically a convolutional neural network (CNN). This shared structure is responsible for extracting meaningful features from the input data. The output layers of both branches generate embeddings or feature vectors for their respective inputs. These embeddings are then compared to determine the similarity between the input samples.

<img src="/img/a1.png" width="600" height="400">


## Triplet Loss
Triplet loss will allow our model to map two similar images close and far from dissimilar sample image pairs.

This approach is done by using triplet constituting:

Anchor Image — This is a sample image.

Positive Image — This is just another variation of the anchor image.

This helps the siamese network model learn the similarities between the two images.

Negative Image — This is a different image from the above two similar image pairs.
This helps our model learn dissimilarities with anchor images.

<img src="/img/l1.png" width="500" height="100">

## Dataset
Dataset from huggingface https://huggingface.co/datasets/Matthijs/snacks
For simplicity we used only two classes apple and banana and prepared dataset as shown below:

<img src="/img/d1.png" width="600" height="300">

<img src="/img/d2.png" width="600" height="300">


## Training Process
During training, the Siamese Network learns to minimize the Triplet Loss by adjusting its weights to ensure that the distance between anchor-positive pairs is smaller than the distance between anchor-negative pairs by at least the specified margin.



## Results
Getting the five most similar images

<img src="/img/r1.png" width="500" height="500">




