# Movie-Recommender


# The Data
The data contains information for all 45,000 movies 
These files contain metadata for all 45,000 movies listed in the Full MovieLens Dataset. The dataset consists of movies released on or before July 2017. Data points include cast, crew, plot keywords, budget, revenue, posters, release dates, languages, production companies, countries, TMDB vote counts and vote averages.

This dataset also has files containing 26 million ratings from 270,000 users for all 45,000 movies. Ratings are on a scale of 1-5 and have been obtained from the official GroupLens website.

# Methods
We used the ALS method to obtain our predicted scores

# Addressing the Cold Start problem
We generated our initial recommendations... We did not address the cold-start problem with this model. 

The first model obtained a score of: 3.6543285287829677

Pretty good for a baseline!

## Addressing the Cold-Start problem
Our next step in addressing this problem was to assign the specific average movie rating to each absent value. 

This resulted in a score of: score= 4.331470453504352

We should probably quit now while we're ahead...

To try to further improve this score, we used the user metadata to find the average movie rating for each gender and then filled in our absent user values with predictions based on the average rating by gender.

This resulted in a score of:

# Next Steps
We cleaned all of the metadata, so we would have like to have refined our recommender to use more user specific info to generate a recommendation. 

