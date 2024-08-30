# Movie Recommendation System
## Overview
This project is a Movie Recommendation System built using collaborative filtering with the FastAI library. The system predicts user ratings for movies and generates personalized movie recommendations based on user behavior.

We trained the model using the MovieLens 100k dataset, a widely used dataset for recommendation systems, containing 100,000 ratings from 943 users on 1,682 movies.

## Features
Collaborative Filtering: Utilizes user and movie embeddings to predict movie ratings.
Latent Factors Optimization: We experimented with different values of n_factors (latent factors) to improve the model’s performance.
Constrained Predictions: Ensures predictions stay within the valid movie rating range (between 0.5 and 5).
Evaluation: Uses RMSE to evaluate the accuracy of the predicted ratings.
## Dataset
MovieLens 100k Dataset: Link to the dataset
100,000 ratings from 943 users on 1,682 movies.
Data is separated into training and validation sets to evaluate the model's performance.
## Model
The model was trained using FastAI’s collab_learner, which automatically handles the training of user and movie embeddings. We tuned the number of latent factors (n_factors) and constrained the output using a y_range to ensure valid predictions.

## Results
The system was able to predict movie ratings with reasonable accuracy, with top movie recommendations including titles that align with users' preferences. After tuning the latent factors, we were able to minimize the root mean squared error (RMSE) on the validation set.

Here’s an example of top 10 recommendations generated for a sample user:
Top 10 movie recommendations for user 10:
1. Love! Valour! Compassion! (1997) - Predicted Rating: 5.15
2. Guantanamera (1994) - Predicted Rating: 5.09
3. Deep Rising (1998) - Predicted Rating: 5.01
4. Bringing Up Baby (1938) - Predicted Rating: 4.94
5. Kalifornia (1993) - Predicted Rating: 4.92
6. Captives (1994) - Predicted Rating: 4.91
7. Wend Kuuni (God's Gift) (1982) - Predicted Rating: 4.91
8. Beautiful Girls (1996) - Predicted Rating: 4.90
9. Star Trek: The Motion Picture (1979) - Predicted Rating: 4.89
10. Coldblooded (1995) - Predicted Rating: 4.88

## Future Improvements
- Address Cold Start Problem: Implement content-based filtering to recommend movies for new users or items.
- Enhance Recommendations: Incorporate metadata such as movie genres, release dates, or user demographics.
- Model Deployment: Deploy the model using a web framework like Flask or FastAPI, so users can get recommendations in real-time based on their input.
