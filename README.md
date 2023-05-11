# Yelp Recommender System

[Dataset source](https://www.yelp.com/dataset)

## Introduction

Yelp  is  an  online  review  platform  where  users  can  leave  a  rating  and  detailed  review  based  on their  experiences  with  businesses. To make informed decisions and pick out their dining experiences, consumers often rely on Yelp for existing information on restaurants. However, the vast amount of restaurants listed on Yelp may make it overwhelming for consumers to come to a decision. In this report, we will explore how bandit algorithms can be utilized to provide users with personalized restaurant recommendations and ease their decision making process.

By framing the restaurant recommendation problem as a multi-armed bandit problem, it is possible to apply bandit algorithms to provide personalized restaurant recommendations to users, based on a restaurant's previous ratings and reviews, along with the user profile while maintaining a level of spontaneity by balancing exploration and exploitation of restaurants.

With the sheer size of the dataset, we decided to confine our analysis to only reviews and businesses in Las Vegas and Toronto as proofs of concept. A wide variety of bandit algorithms will be used, including Episilon-decay, Softmax, UCB, Bayesian UCB, Thompson Sampling, as well as contextual bandits like LinUCB and Contextual Thompson Sampling.

## Summary of results

Overall, taking the findings from both the Las Vegas and Toronto results, there is clearly scope for using bandit algorithms to deliver recommendations towards Yelp users. The ability of bandit algorithms to explore different restaurants allows for varied recommendations, while also being able to exploit restaurants that have a track record for positive reviews. The Softmax algorithm was the clear standout, likely due its ability to explore arms with lower expected rewards as it assigns them a non-zero probability. The performance of contextual bandits varied across the datasets, possibly due to the limited number of user features that could be generated from Yelp's open source data. Nevertheless, the LinUCB algorithm showed potential in leveraging  a user’s profile to provide personalized recommendations. With the availability of additional user data and the chance to perform online evaluation, it is possible that bandit algorithms can allow Yelp to deliver an improved user experience by supplying suitable restaurant recommendations.


## Relevant files

Full report found in ```report.pdf```.

Data processing notebook found in ```data-preprocessing.ipynb```, generated output in ```processed_reviews.zip```.

Code for bandit algorithms and offline evaluation found in ```offline_evaluation.ipynb```, with results saved in ```lasvegas_results.csv``` and ```toronto_results.csv```.


