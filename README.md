# Movie-Recommender


# The Data

# Methods
We used the ALS method to obtain our predicted scores

# Addressing the Cold Start problem
Our first model performed well, but there were many absent values. Our first solution to this problem was to assign the average rating for all movies to absent values. This resulted in a score of:

To try to further improve this score, we used the user metadata to find the average movie rating for each gender and then filled in our absent user values with predictions based on the average rating by gender.

This resulted in a score of:

# Next Steps
We cleaned all of the metadata, so we would have like to have addressed the cold-start

