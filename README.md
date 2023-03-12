# movie_genre_predictor

## Dataset

https://raw.githubusercontent.com/sukhjitsehra/datasets/master/CP322/movies.csv

Here, we are exploring movie screenplays. We'll be trying to predict each movie's genre from the text of its screenplay. In particular, we have compiled a list of 5,000 words that occur in conversations between movie characters. For each movie, our dataset tells us the frequency with which each of these words occurs in certain conversations in its screenplay. All words have been converted to lowercase.

## Simulating K-Nearest Neighbors

We are going to `simulate` the steps that `K-Nearest Neighbors (k-NN)` algorithm will use for classification, i.e.,  Given some numerical *attributes* (also called *features*) of an unseen example, it decides which category that example belongs to based on its similarity to previously seen examples. Predicting the category of an example is called *labeling*, and the predicted category is also called a *label*.

An attribute (feature) we have about each movie is *the proportion of times a particular word appears in the movie*, and the labels are two movie genres: comedy and thriller.  The algorithm requires many previously seen examples for which both the attributes and labels are known: that's the `train_movies` table.

### Classifying a Movie in K-Nearest Neighbors

In k-NN, we classify a movie by finding the `k` movies in the *training set* that are most similar according to the features we choose. We call those movies with similar features the *nearest neighbors*.  The k-NN algorithm assigns the movie to the most common category among its `k` nearest neighbors.

### Our Simulated K-Nearest Neighbours Accuracy

![image](https://user-images.githubusercontent.com/57271684/224519060-109ca0d6-9ffd-4795-b7cc-a01bcca3cc02.png)

Classification using Euclidean Distance between all features

## Using SKLearn Models (K-Nearest Neighbors and Random Forest)

### Grid Search

Grid Search was used for hyperparam tuning in KNN and Random Forest to find the best values for k (# of neighbours) and n (# of trees)

### Performance Metrics

![image](https://user-images.githubusercontent.com/57271684/224519030-48117d52-9abd-4010-b04c-67fba9631676.png)

![image](https://user-images.githubusercontent.com/57271684/224519035-6ad92f95-b6bd-4e0b-a02a-70cb6a521bec.png)
