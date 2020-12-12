# Movie-Recommender
Josh Bernd, Katie Johnson, Isabella Sun

# The Data

# Matrix Factorization

1. Alternative Least Squares
    
    We used Spark's Alternative Least Squares (ALS) recommender class to predict user's movie ratings. The model left approximately half of the requested predictions empty. Without addressing this cold-start problem, the initial model achieved a score of **3.6543**.

2. Using Average Movie Rating

    To address the cold-start problem, we calculated the average rating each movie received and replaced any missing values from the predictions with the average rating that movie received from all other users in the training data. This achieved a score of **4.3315**. 115 predictions remained empty where a few movies did not appear in the training data. 

3. Average Rating Overall

    Next, we filled in those remaining missing predictions with the average overall rating for all movies. This resulted in a score of **4.3308**

4. Average Movie Rating by User's Gender
    
    To try to further improve this score, we used the user metadata to find the average movie rating by gender and then filled in our absent user values with predictions based on the average rating by gender.


# Next Steps
With next steps, we would like to use additional information from the metadata about users and movies to address the cold-start problem. For example, instead of using a movie's average rating where there is a cold-start, we could use the average rating among that user's age group as a more accurate prediction. 

Additionally, we would have liked to use gradient descent to tune the parameters of our ALS model. 