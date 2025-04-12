# Big Data Course Project

### The aim of the project was to work with a large dataset, and to learn to pre-process and analyze it.

Our group found similar interests in recommender systems in machine learning and big data. Our objective was to create a model that learns user preferences from past user-item interaction data to predict future user preferences and recommend items that we predict the user would rate well.

Our group found a dataset containing books information, user information, and user-item interactions: ratings.
- 17GB book dataset from Kaggle, which needed a vast amount of preprocessing
- Handled duplicates and exploded nested lists
- We removed all rows with null rating values, since ratings were our label feature for the supervised learning model
- We selected 2000 of the most popular books and filtered the dataset to include only these books. After this step, the dataset contained 423,224 instances.

### Results

The best RMSE (Root Mean Squared Error) score was achieved using GridSearchCV with KNNWithMeans algorithm was 1.053. 

![image](https://github.com/user-attachments/assets/215c6af9-b6f5-4549-b78c-e6698833e621)

This result was obtained with the following hyperparameters: 
* Mean Squared Difference (MSD) similarity metric, and
* user-based collaborative filtering.

User-based collaborative filtering outperformed item-based filtering for this dataset, which suggests that similarities between users was more effective in predicting user preferences than similarities between items.

We found a slight improvement in RMSE the higher the number of neighbors, and that user-based performs slightly better than item-based.
![image](https://github.com/user-attachments/assets/3e3eff5c-3f5f-4ab5-a3a2-1384ac8c7622)

