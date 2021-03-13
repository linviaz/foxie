# Feature Selection Methods
 - Filter Methods
 - Wrapper Methods
 - Embedded Methods

 Source reference: [udemy.com/course/feature-selection-for-machine-learning](https://www.udemy.com/course/feature-selection-for-machine-learning/)

## Filter Methods
Filter methods:
 - rely on the characteristics of the data (feature characteristics), 
 - do not use machine learning algorithms, 
 - model agnostic, 
 - tend to be less computationally expensive, 
 - ususally give lower prediction performance than a wrapper method, 
 - are very well suited for a quick screen and removal of irrelevant features


## Wrapper Methods
Wapper methods:
 - use predicitive machine learning models to score the feature subsets;
 - train a new model on each feature subset;
 - tend to be very computational expensive;
 - usually provide the best performing feature subset for a given machine learning algorithm;
 - they may not produce the best feature combination for a different machine learning model.


## Embedded Methods
Embedded methods:
 - perform feature selection as part of the model construction process;
 - consider the interaction between features and models;
 - they are less computationally expensive than wrapper methods, because they fit the machine learning model only once.

