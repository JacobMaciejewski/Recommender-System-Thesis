# Recommender-System-Thesis
Implementation of Novel Hybrid Recommender System based upon Light-FM and Custom Embeddings, Benchmarking 🤖 

## Introduction:

This is the working [Google Collab](https://research.google.com/colaboratory/faq.html) environment of what was supposed to be my *University Thesis*,
which explores the topic of [Recommender Systems](https://en.wikipedia.org/wiki/Recommender_system) in the domain of Movie Recommendations. Specifically,
I focused on the [Top-K Retrieval](https://www.sciencedirect.com/science/article/abs/pii/S002002551830714X) Algorithms, that return the $k$ best
answer to the query at task (best movie recommendations in our case). [IMBD Dataset](https://www.imdb.com/interfaces/) became my dataset of choice.

I aimed to make use of the wide variety of *Rating Prediction Algorithms*, but most of them have no one-way approach for their adaptation to the *top-N
Recommendation Task*. My approach is based upon [Candidates Sets](https://www.sciencedirect.com/topics/mathematics/candidate-set), containing all
the movies eligible to be recommended to a user. Ratings are predicted for all the members of the Candidate Set and the top-N rated movies are being
suggested to the user. All the top-N evaluation metrics are applied by comparing the *Test Set Interactions* (user ratings for specific users) with
the ranking of the candidates.

I followed the policy of **Candidates Choosing**, based upon one of the most popular approaches, where for each user that appears in the test set,
all the movies that appeared in the *Train Set* and have not been interacted with by the specific user, are eligible for suggestion.
Ratings given by each test user for the movies he has not interacted with in the train set, are being calculated with the algorithm of choice,
then highest rated movies are suggested for each user.

## Contents

*Collab script consists of:*

* **Recommendation Pipeline** - developed from the scratch, stands as a custom, support library for fast deployment of future Recommendation Experiments
* **Novel Hybrid RS** - implementation of a *New Recommendation Algorithm* that takes advantage of [LightFM](https://github.com/lyst/lightfm)
and the Custom Movie Embeddings (currently only Audio supported)
* **Benchmarks** - a wide variety of Recommendation Algorithms is being tested out and compared with our novel approach

*Comment cells include:*

1. Broad analysis of benchmarked algorithms (including the novel one)
2. Recommendation Pipeline's design analysis and operation guide
3. Experiment results analysis

### Further Information:

This extensive script is the main setup of what was supposed to be my University Thesis and it was done as a collaboration with representatives
if an important Greek Research Center. I was supplied me with some natively produced, custom embeddings, for which I lack rights over. Once proper
permission is acquired, repository will be fully updated to reflect the state of my own Google Collab working directory.
Currently,  **I CANNOT SHARE** a big portion of the necessary files and folders! 
