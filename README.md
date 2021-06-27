
# DLP_2021
Deep Learning project lead by Rafał Nowak from Wroclaw University at Computer Science faculty.

## Project 2 

Team: 

* [Marta Kałużna](https://github.com/mkaluzna)
* [Szymon Czop](https://github.com/szymonczop) 

In the second project, we will focus on sentiment classification in *IMDB* dataset which contains the text of 50,000 movie reviews.
Movie reviews are split into 25,000 for training and 25,000 for testing. The training and testing sets are balanced - they have the same number of positive and negative reviews.        
We are going to split the training set into 15,000 examples for training and 10,000 examples for validation.

Labels are as follow:

* 0 - a negative review
* 1 - a positive review

In order to make our work easier, we will use pre-trained text embedding and weights for neural network
form [Tensorflow Hub](https://www.tensorflow.org/hub)

The whole work is split into two files:

* Colab file (Text classification with TensorFlow Hub: Movie reviews v2.ipynb)
* Jupyter file with the classical approach to the problem.

## COLAB

We will use word embeddings from TFHub. Because they are all pre-trained there is no need to do this again. In **colab** file we set an option that allows us to pick one of 4 different embeddings and use them
in the final model. By clicking on the given model we can see more details and documentation on the offical TensorFlow Hub pages.
After introducing some basic neural network that can be adjusted to the needs of the user we can find the plotted process of training
with information about accuracy and loss for **both** training test and validation set. 
We run models for all 4 embeddings and make a small summary about the final outcome of scores. 

In the second part of Colab, we are using different kinds of BERT neural networks (also imported from TFH).
Again we have plenty of models to choose and we can play with them with the usage of a friendly colab interface

**Some suggestions for choosing a model**       
- Start with a *Small BERT* since they are faster to fine-tune.      
- *ALBERT* might be a good choice if you want a small model but with higher accuracy.       
- Classic *BERT* sizes or their recent refinements like *Electra, Talking Heads, BERT Expert* will have the highest accuracy.

## Jupyter notebook with the classical approach
In this jupyter file user can find:

* Wordclouds concerning negative or positive sentiment
* How many times given word was used in a negative or positive context 
* Usage of Zipf's law
* classical models with different tokenization (Logistic Regression, Naive Bayes)
* plots for all kinds of used models concerning trainable parameters.
* Comparing TFiDF and CountVectorizer for Logistic regression
* Listing top 100 positive and negative words according to models
* Final summary about all tested models in this file.



