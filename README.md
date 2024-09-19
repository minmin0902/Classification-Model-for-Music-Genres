# Music Genre Classification Project

## Overview
In this project, I focused on building a classification model to identify music genres based on various acoustic features. Several design choices were made to address the challenges of working with the dataset, and the final model demonstrates strong performance with the ability to visualize music genres as clusters in a lower-dimensional space.

## Building the Model and Design Choices

To build the classification model for music genres, I made several design choices to address the challenges presented by the dataset:

### 1. Handling Missing Data
Randomly missing data, such as song durations and auditory feature values, were addressed by dropping rows with missing values. As the percentage of missing values was negligible, I deemed this approach reasonable, ensuring that the integrity of the dataset was maintained without significant information loss.

### 2. Dealing with Non-Normal Distribution
The acoustic features were unlikely to follow a normal distribution. To improve the distributional properties of the features, I applied log transformations to features with skewed distributions. This helped create a more suitable feature set for modeling purposes.

### 3. Encoding Categorical Variables
Certain columns, such as `key` and `mode`, contained string or categorical data. To make these features compatible with the classification model, I used encoding techniques like label encoding and dummy coding, transforming them into numerical values.

### 4. Feature Selection
I conducted a feature importance analysis using a Random Forest classifier to determine which features were most informative. I selected the top features identified for training the classification model, improving model efficiency and accuracy.

### 5. Model Selection
I chose a K-Nearest Neighbors (KNN) classifier due to its simplicity and effectiveness in handling high-dimensional data. I determined the optimal value of `k` using cross-validation to ensure that the model was tuned for the best possible performance.

## Visualization and Clustering in Lower Dimensional Space

I performed dimensionality reduction using Principal Component Analysis (PCA) to reduce the complexity of the feature space and visualize the music genres as clusters in lower-dimensional space. These clusters indicated some degree of separation among the different genres, suggesting that the selected features captured the distinguishing characteristics of each genre.

Further analysis is needed to explore the interpretability of these clusters and their relationships with the original features. 

## Most Important Factor for Classification Success

The most critical factor contributing to the success of the classification model was the selection of informative features. By identifying and utilizing the top important features, the model better differentiated between genres and resulted in a higher overall performance.

## Model Performance

I evaluated the final classification model using the Area Under the Receiver Operating Characteristic Curve (ROC AUC).

- **Final ROC AUC Score**: `0.8577`

This score indicates that the model performs well in distinguishing between different music genres based on the selected acoustic features.

## Non-Trivial Observation

One intriguing finding from the visualization of clusters in the low-dimensional space was the observation that some regions showed overlap between different genres. This suggests that certain types of music share common attributes, and in some cases, the distribution of these features overlaps. As a result, this can make classification more challenging and implies that feature selection alone may not always be sufficient to fully separate genres.

## Conclusion

I successfully addressed the challenges presented by the dataset through strong data preprocessing strategies, feature selection, and model training methods. The following key points summarize the project:

- **Data Preprocessing**: Log transformations and encoding of categorical variables helped handle skewed data and categorical values.
- **Feature Selection**: Random Forest feature importance analysis allowed me to select the most informative features, improving classification accuracy.
- **Model Training**: K-Nearest Neighbors, selected for its simplicity and suitability for high-dimensional data, was optimized using cross-validation for the best results.

Based on the selected features, visualizing clusters in a lower-dimensional space provided insights into the differences between music genres. This visualization helped me understand the characteristic differences between genres, especially regarding transitions between different genres and music types.

The classification model demonstrated promising performance, with a ROC AUC score of `0.8577`. Overall, I succeeded in classifying music genres based on acoustic features.



<img width="411" alt="Screenshot 2024-09-18 at 11 29 24 PM" src="https://github.com/user-attachments/assets/1e2bbf76-5966-49c5-ac28-722a297b206a">
<img width="386" alt="Screenshot 2024-09-18 at 11 29 52 PM" src="https://github.com/user-attachments/assets/fca6dcaf-ec03-4257-a3d5-cdedc0f2ff35">


