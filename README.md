# Recommender System for Amazon Pet Supplies 

## Overview 

This project involves the creation of a recommender system using Amazon's Pet Supplies ratings data. The dataset, sourced from UCSD's Amazon review data [1], includes ratings from 1 to 5 for various pet products. The project focuses on building two types of recommendation models: a Popularity-Based Recommender System and a Collaborative Filtering Recommender System utilizing Singular Value Decomposition (SVD).

## Data Preparation

1. **Data Loading**: The dataset is loaded from a CSV file, and columns are renamed for clarity.
2. **Data Cleaning**: The 'timestamp' column is dropped as it is not necessary for building the recommendation model.
3. **Exploratory Data Analysis (EDA)**: Initial EDA is conducted to understand the distribution of ratings, identify unique users and products, and check for missing values.
4. **Filtering Data**: Users who have rated at least 25 items are selected for focused analysis, reducing data sparsity and improving model performance.
5. **Data Splitting**: The dataset is split into training (70%) and testing (30%) sets for model evaluation.

## Popularity-Based Recommender System
- **Methodology**: Products are ranked based on the number of ratings they receive.
- **Recommendation**: The top-rated products are recommended to all users irrespective of their personal preferences or past behavior.
- **Limitation**: This approach lacks personalization as it recommends the same set of products to every user.

## Collaborative Filtering Recommender System
- **Methodology**: Utilizes SVD to decompose the user-item rating matrix into lower dimensions.
- **Prediction**: Missing ratings are predicted using the decomposed matrices, allowing for the estimation of user preferences.
- **Personalization**: Recommends products to users based on predicted ratings, ensuring that recommendations are tailored to individual user preferences.
- **Evaluation**: The model's performance is evaluated using RMSE, with a low RMSE indicating accurate predictions.

## Results
- **Popularity-Based Model**: Effective for recommending generally popular products but not tailored to individual users.
- **Collaborative Filtering Model**: Provides personalized recommendations, ensuring that different users receive different suggestions based on their historical ratings.
- **Model Accuracy**: The collaborative filtering model demonstrates high accuracy with a low RMSE value.

## Conclusion
This project illustrates the implementation of two types of recommender systems. The popularity-based model offers simplicity but lacks personalization, while the collaborative filtering model delivers personalized recommendations, making it more suitable for diverse user preferences. The provided script allows users to load data, train models, and generate recommendations by modifying `userID` and `num_recommendations` variables for customized outputs.

## References 

1. https://jmcauley.ucsd.edu/data/amazon/

---

## License

This project is licensed under an **All Rights Reserved** license. Unauthorized use, distribution, or modification of the code is strictly prohibited. For inquiries or permission requests, please contact [sm3924@georgetown.edu or msheeba00@gmail.com].
