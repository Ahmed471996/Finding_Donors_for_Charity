# ML_Udacity


## Introduction

In this project, you will employ several supervised algorithms of your choice to accurately model individuals' income using data collected from the 1994 U.S. Census. You will then choose the best candidate algorithm from preliminary results and further optimize this algorithm to best model the data. Your goal with this implementation is to construct a model that accurately predicts whether an individual makes more than $50,000. This sort of task can arise in a non-profit setting, where organizations survive on donations. Understanding an individual's income can help a non-profit better understand how large of a donation to request, or whether or not they should reach out to begin with. While it can be difficult to determine an individual's general income bracket directly from public sources, we can (as we will see) infer this value from other publically available features.

## The dataset

The dataset for this project originates from the UCI Machine Learning Repository. The datset was donated by Ron Kohavi and Barry Becker, after being published in the article "Scaling Up the Accuracy of Naive-Bayes Classifiers: A Decision-Tree Hybrid". You can find the article by Ron Kohavi online. The data we investigate here consists of small changes to the original dataset, such as removing the 'fnlwgt' feature and records with missing or ill-formatted entries.

## Used Models 

# Support Vector Machines:

One real world application:

Hand writing recognition can be deployed using SVM. Strengths of the model:

Works well in high dimension spaces - for example, image recognition where every pixel may be treated as a feature. Maintains effectiveness even in cases where the number of dimensions exceeds the number of samples - again applicable in the field of image recognition. It is memory efficient due to its use of a subset of training points in the decision function. It provides versatility through the deployment of common and custom kernels. Works well in a complicated domain where there is a clear degree of seperation. Weaknesses of the model:

Overfitting must be avoided through the selection of the correct kernel choice and regularisation term if the number of features far exceeds the number of samples. Inefficient five-fold cross-validation is deployed to calculate probability estimates. Can only be applied to two class tasks. As a result, multi-class tasks must be reduced to several binary problems. The parameters of a model that has been solved can be difficult to interpret. Does not perform well in large datasets as training is cubic in the size of the dataset. Does not work well with lots of noise, so when classes are overlapping you have to count independant evidence (this is where a NB classifier would work better). What makes it a good candidate for the problem:

Sample size is greater than 50 samples (have enough data to train with). Data is labelled. Predicting a categorey (works with classification) Sample size is less than 100k. Works well with large feature sets (ours is relatively small -> medium size).

# SGD Classifier:

One real world application:

Text classification and natural language processing. It is useful as when the given data is sparse, the function can easily scale to problems with more than 10^5 training examples and more than 10^5 features. Strengths of the model:

It is efficient. It is easy to implement and provides a lot of opportunities for code tuning. Weaknesses of the model:

A number of hyperparameters are required for SGD, such as the number of iterations and the regularisation parameter. It (SGD) is sensitive to feature scaling. What makes it a good candidate for the problem :

Sample size is greater than 50 samples (have enough data to train with). Data is labelled. Predicting a categorey (works with classification) Sample size is less than 100k, but SGD works well with sizes greater than this, meaning greater computational efficiency and speed.

# K Nearest Neighbour:

One real world application:

KNN can be used to provide recommendations. A real world example of this would be video streaming services such as Netflix or Amazon Prime. If a given user likes an item in the library, similar items that they may like, but are unaware of can be recommended to them by using data from other users and their likes. If it is seen that a similar set of users like two different items, these items are probably similar and to each the respective users taste, and worthy of a recommendation. Strengths of the model:

Easy to understand and implement - not much code is required. No probability distributions are assumed based on the input data. This is useful with inputs where the probability distribution is unknown, making it robust. KNN is a lazy learner. This means it generalises data during the training phase, not the testing phase. This allows it quickly adapt to changes as it does not expect a generalised data set. Weaknesses of the model:

KNN gets its information from its input neighbours. As a result of this, localised outliers can affect outcomes significantly when compared with other algorithms which have a generalised view of the data. It is sensitive to localised data. One of its strengths, lazy-learning, is also one of its weaknesses. As most of the computation is done during testing, rather than during training, this can result in long computation times when dealing with large datasets. If there is a type of categorey that is present much more than another, classifying an input will result in a bias to this more abundent categorey. This can be dealt with by adjusting the weights based on occurences, but will still pose a problem near the decision boundary. Inputs can be close to many points when there are many dimensions. The effectiveness of k-NN is reduced as a result. This is as it relies on the correlation between closeness and similarity. Dimension reduction can be used to reduce the effects of this, but variable trends may be lost as a result. What makes it a good candidate for the problem :

Sample size is greater than 50 samples (have enough data to train with). Predicting a categorey (works with classification). Sample size is less than 100k Data is labelled. 

## Results 

![image](https://user-images.githubusercontent.com/101316217/210415980-f0aba2b7-67c0-40c6-a185-a3f6671c5d56.png)


## Future Work 

Trying different Supervised Machine Learning Models 
