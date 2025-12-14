# -- Final Capstone Project -- 

## Title: Precision Agriculture & Crop Recommendations.

### Data Source: [https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset/data]
### Data Summary:
[Kaggle] ... "Recommendations from evaluation of this dataset with Machine Learning techniques will aid farmers in making informed decisions in their farming strategy. 
This dataset allows the users to build a predictive model to aid in recommendations for suitable crops to grow in a particular farm based on weather and soil characteristics."

## Proposal -
- Research question I expect to answer (in one sentence, if possible) : Are farmers better off using recommendations based on analysis applying ML tecchniques?
- Expected data source(s): [https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset/data]
- Approach and Techniques expected to use in analysis: Decision Tree, KNN, SVM, among others.
- Expected results: Presented through data visualization, models used for evaluations, accuracy of models, correlation driving recommendations.
- Why this question is important: a) water and land are critical resources b) supports sustainable farming and minimizes application of chemicals,
  which are generally bad for the environment c) optimizes the production of crops based on nutritional needs. Overall, contribute to a healthy
population one nutritional crop at a time.

## Goal -
The goal of this exercise is to succesfully apply the AI/ML concepts and ML technicques acquired in this program to build classification model
predictive model to aid in recommendations for suitable crops to grow in a particular farm based on Features of dataset (weather and soil nutrients).

## Overview - 
The drive to produce, healthy, nutritous, and abundant food supply with less resources by applying responsible, thoughtful planning and farming best practices,
through accessible and affordable technologies en mass for efficient farming resource utilization and environmental preservation.
This approach will inform farmers in their strategies to safeguard harvests from crop diseases, improving yield.

The features of the dataset include the following parameters: soil nutrients phosphorus (P), potassium (K), and nitrogen (N),   
and weather characteristics temperature, humidity, rainfall, and soil pH. The target is the crop label (crop name).

We first visualize the data to gain understanding of the dataset, features distributions through Histograms, Scatter plots, 
Boxplots, Violin plots, and features relationship uisng Correlation matrix, Covariance matrix, and Pairplots.

Identified as a ML classification exercise, we compare various ML models (including K-Nearest Neighbors, Random Forest, Gradient Boost, 
Support Vector Machine (SVM), Logistic Regression and select the optimal ML model to employ for crop recommendation.

We apply Feature Engineering and K-fold Cross-Validation techniques to improve the precision of recommendation from the data. 
The optimal ML model is determined by comapring performance measures of precision, recall, F1 score, and Confusion Matrix.

To improve model performance and guide selection of features that are most important in the dataset for classification, 
we remove data with neglible importance by applying (Feature) Permutation Importance.

The next steps in the analysis will attemopt to apply Ensemble Techniques & Recommendation Systems to improve Crop Recommendation.
- Bagging, Bootsrapping, Boosting, Voting Ensemble
- Content Based Filtering, Collaborative, Hybrid

## Deliverables
The final submission should include the Jupyter Notebook and other relevant files, such as the dataset provided and uploaded to a GitHub repository.

## Links to Project Deliverables
- READMe file with summary of findings >>  [https://github.com/altruizim101/Final-Project]
- Link to Jupyter notebook here >>         
- Data Analysis & Results >> [https://github.com/altruizim101/Final-Project]

## (Data Understanding)
Checked for possible Null (NaN) values in data for removal before analysis. Then filtered NaN data as appropriate.
Action: removed missing (NaN) data in columns

## Data Visualizations
Correlation Matrix:
-- Plots: >> [https://github.com/altruizim101/Final-Project]
- Strong positive correlation of about +0.76 observed betwee Potassium (K) and Phosphorous (P).
- Weak positive correlation (~0.22) between Humidity and rainfall.
- Weak positive correlation (~0.19) between Humidity and Nitrogen (N).

Histograms and Feature Distribution:
-- Plots: >> [https://github.com/altruizim101/Final-Project]
- A Binomial distribution is observed for Nitrohen.
- Temperature and pH approach a normal distribution.
- Humidity is left-skewed.
- Rainfall is right-skewed distribution.
- Potassium (K) is right-skewed distribution.

Boxplots of Features:
-- Plots: >> [https://github.com/altruizim101/Final-Project]
- pH shows the narrowest distribution, with smallest variance, followed by Teamperature.
- Humidity and Potassium (K) shows comaprable variances.
- Rainfall and Nitrgen shows the laragest variances.

ViolinPlots of Features:
-- Plots: >> [https://github.com/altruizim101/Final-Project]
- pH shows the narrowest distribution, with smallest variance, followed by Teamperature.
- Humidity and Potassium (K) shows comaprable variances.
- Rainfall and Nitrgen shows the laragest variances.

## Data Analysis & Transformation
-- Plots: >> [https://github.com/altruizim101/Final-Project]
- Feature Engineering

## Evaluations - Models and Metrics
-- Plots: >> [https://github.com/altruizim101/Final-Project]
- Technicques & ML models (Random Forest, K Nearest Neighbors, Gradient Boost, SVM, Logistic Regression)
- Metrics for evaluation: accuracy score, F1 score, Recall, Precision 
- Additional techniques (TBD)

## Explainability of Analysis
-- What is results of analysis telling us?

## Recommendations
- Make recommendations on crops based on evaluations from above (TBD)

