# Data Representations and Clustering
## Introduction
This is a project for exploring feature extraction and clustering techniques for text and image data with a final goal of using these techniques to automatically separate a document set or an image dataset into groups that match known labels (or categories). 
The project will contain the following parts:
- Exploring feature extraction from text data
- Clustering techniques using K-means, DBSCAN, HDBSCAN and Hierarchical clustering
- Exploring how to use deep learning or deep neural networks (DNNs) to obtain image features. 
- Using pre-trained networks that have learned to discover features that are salient for image understanding, and can be used for transfer learning.
- Evaluating models by using a common set of multiple evaluation metrics (contingency matrix, homogeneity score, completeness score, V-measure score, adjusted Rand Index score, and adjusted mutual information score) to compare the groups extracted.

## Data Set
The text data set consists of 7882 data points. The original classes of the news group contains the data about which news column it was originally written in. This target variable contains 20 classes.
The image dataset consists of 3670 images, which are resized to 150,5286 pixels in size (224 x 224 x 3), with the width and height being equal to 224 and the number of RGB color channels being 3. The features extracted by VGG from each image in the final layer of the network are equal to 25,088. However, these features are then processed through a fully connected layer to reduce their number to 4096 per image. Thus, each feature vector for an image sample is of dimension (4096,).



## Exploring feature extraction from text data
For the text data there were 20 calsses where we will only be focusing on 8 of the 20 categories. This will be transformed into a two-class clustering problem by merging all of the "comp" related classes into one and all of the "rec" related classes into another. Then the data was cleaned, lemmatized and count vectorized then modified into a TF-IDF matrix.

## Dimensionality Reduction
Methods used:
- SVD with hyper parameter tuning
- NMF with hyper parameter tuning
- UMAP with hyper parameter tuning

## Clustering
Methods Used:
- K-means
- DBSCAN
- HDBSCAN
- Hierarchical clustering

## Metrices
Metrices used:
- Homogeneity score
- Completeness score
- V-measure score
- Adjusted Rand Index score
- Adjusted mutual information score

## VGG network
Using pretrained VGG network to extract the features from the image data. The number of features extracted is 4096 per image.

## Using dimensionality reduction and clustering models on features extracted
These 4096 features are then used to evaluate different dimensionality reduction techniques and clusterting models on this specific data.