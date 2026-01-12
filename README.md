# -- Capstone Project, 15 January 2026 --
# Final Report for a Crop Recommendation System
#

## Goal -
The goal of this project is to apply Machine Learning (ML) concepts and technicques acquired in program to build classification/ 
predictive model that aids in the making recommendations for suitable crops to grow based on input Features of dataset (features include
weather and soil nutrients).
This exercise aims to classify the most suitable crop for cultivation based on soil and weather conditions. Given input features 
as soil nutrient levels (N, P, K), pH, moisture, temperature, rainfall, and humidity, the system predicts a single crop class that 
is most likely to perform well under those conditions. This enables the farmer in making decisions that optimize productivity and efficient 
use of resources, reduce uncertainty, avoid unsuitable crop choices, and improve consistency in farm output.

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

## Proposal -
- Research question I expect to answer (in one sentence, if possible) : Are farmers better off using recommendations based on analysis applying ML tecchniques?
- Data source(s): [https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset/data]
   Kaggle Data Summary ... "Recommendations from evaluation of this dataset with Machine Learning techniques will aid farmers in making informed decisions in their farming strategy.   
   This dataset allows the users to build a predictive model to aid in recommendations for suitable crops to grow in a particular farm based on weather and soil characteristics."

- Approach and Techniques expected to use in analysis: Random Forest, Decision Tree, K-Nearest Neighbors, Support Vector Machine (SVM), Logistic Regression.
- Expected results: Presented through data visualization, models used for evaluations, accuracy of models, correlation driving recommendations.
- Why this question is important: a) water and land are critical resources b) supports sustainable farming and minimizes application of chemicals,
  which are generally bad for the environment c) optimizes the production of crops based on nutritional needs. Overall, contribute to a healthy
population one nutritional crop at a time.

## Challenges, Pitfalls - 
Developing a robust and effective model for crop recommendation has several challenges. Accurate recommendations depend on 
reliable (soil & weather) data. This data may be incomplete, outdated, or inconsistent across regions. The models trained on data 
from one location may not generalize well to different climates, soil types, or farming practices without local adaptation. Further, 
unpredictable weather patterns can reduce the reliability of historical data used for training the model. Most importantly, farmers may 
be hesitant to rely on ML-based recommendations without proven past results and clear explanations.

## Potential Benefits -
An ML-based crop recommendation system offers several important benefits for farming. By matching crops to local soil and weather 
conditions, it helps improve crop yields and overall productivity. More accurate crop selection leads to lower operational costs
by reducing spending on water, fertilizers, and pesticide. The system minimizes farming risks by discouraging unsuitable crop choices, 
reducing the likelihood of crop failure under poor farming conditions. In addition, optimized crop planning promotes sustainable farming 
practices by supporting better soil health and more efficient use of natural resources over time.

## Approach and Steps -
The features of the dataset (from Kaggle platform) include following parameters: soil nutrients phosphorus (P), potassium (K), and nitrogen (N),
and weather characteristics temperature, humidity, rainfall, and soil pH. The target is the crop label (crop name).
We apply the following steps in this exercise: 
1) data cleaning & pre-processing 2) data visualization & understanding 3) Feature Selection 4) employ multiple ML algorithms with
hyperparameter tuning 5) select optimal ML algorithm 6) select the important Features (permutation importance) and 
7) make recommnedations using optimal ML algorithm with most important Features.

## Data Visualization & Understanding -
Data Visualization is an essential step before ML modeling because it helps in understanding the structure & quality of the data. 
Visualizing features in the data allows us to identify patterns & relationships between variables that may influence model performance. 
It also helps detect missing values, outliers, and data imbalance that could negatively affect modeling process.
This step aids in reducing errors, improving model design, and increasing confidence that the ML model is built on well-understood 
data.
We first load and visualize the data to gain understanding of dataset, features & distributions through Histograms, Scatter plots, 
Boxplots, Violin plots, and features relationship uisng Correlation matrix, Covariance matrix, and Pairplots. Understanding of data
facilitates in selection and application of appropriate ML techniques in the data analysis.
The data contains 2,200 samples with 22 unique crops types in "label" column, for a total of 100 samples per crop type.
The data is eight (8) columns with seven (7) Features and a Target ("label" column).

## Data Outcome and Predictions -
As classification exercise, we compared various ML models (including K-Nearest Neighbors, Random Forest, Gradient Boost, 
Support Vector Machine (SVM), Logistic Regression and then select the optimal ML model (through hypeparameter tuning) to 
employ for crop recommendation.
To further optimize model, we apply Feature Engineering and K-fold Cross-Validation techniques to improve precision of recommendation 
from the data. The optimal ML model is determined by comapring performance measures of precision, recall, F1 score, and Confusion Matrix.


## Data preprocessing & Visualizations -
- Check for possible Null (NaN) values in data for removal before analysis. Then filtered NaN data as appropriate.
- Action: remove missing (NaN) data in columns.

We display data with Freatures (columns) and Samples (rows); how many Features? How many samples? identify data Features? Is data "balanced"? Does data contain missing values? ...
splitting data into train and test sets is essential for building ML models. The "train" set is used to teach the model about 
patterns and relationships between input features and target class. The "test" set evaluates how well the model performs on new,
unseen data.

Correlation, Covariance Matrices Heatmaps:
Covariance is a measure of how two features in the data vary together.
Correlation helps identify which Feature in the data is strongly correlated to the Target.
- Plots: >> [https://github.com/altruizim101/Final-Project]
- Strong positive correlation of about +0.76 observed betwee Potassium (K) and Phosphorous (P).
- Weak positive correlation (~0.22) between Humidity and rainfall.
- Weak positive correlation (~0.19) between Humidity and Nitrogen (N).

Histograms and Feature Distribution:
- Plots: >> [https://github.com/altruizim101/Final-Project]
- A Binomial distribution is observed for Nitrohen.
- Temperature and pH approach a normal distribution.
- Humidity is left-skewed.
- Rainfall is right-skewed distribution.
- Potassium (K) is right-skewed distribution.

PairPlots:
- Plots: >> [https://github.com/altruizim101/Final-Project]
Pairpolts provide a quick, comprehensive view of relationships between the Features in dataset. A pairplot creates scatterplots for every pair of 
Features, revealing correlations and potential patterns that might influence predictions.

Boxplots of Features:
- Plots: >> [https://github.com/altruizim101/Final-Project]
- pH shows the narrowest distribution, with smallest variance, followed by Teamperature.
- Humidity and Potassium (K) shows comaprable variances.
- Rainfall and Nitrgen shows the laragest variances.

ViolinPlots of Features:
- Plots: >> [https://github.com/altruizim101/Final-Project]
- pH shows the narrowest distribution, with smallest variance, followed by Teamperature.
- Humidity and Potassium (K) shows comaprable variances.
- Rainfall and Nitrgen shows the laragest variances.

## Evaluation, Models & Metrics -
Several ML models are employed. We perform hyperparameter tuning using GridSearch and Cross validation.
Exploring various ML algorithms: choosing the appropriate model for a crop recommendation system depends on several factors, including 
data size, feature characteristics, interpretability needs, and performance requirements. Evaluating and comparing several models enables 
us to choose the best model. Models selected for evaluation include K-Nearest Neighbors, Random Forest, Gradient-Boost, Support-Vector Machine (SVM) and 
Logistic Regression.
Grid Search: we perform grid search to find the best combination of hyperparameters for the models, and to optimize model performance on the data.
We evaluate combinations of hyperparameters in a structured approach, to enables a fair comparison between the different models considered, in order to 
improve the confidence in the recommendation system.

## Permutation Importance of Features: best model from GridSearchCV -
In applying Feature Importance in the crop recommendation system, we understand which soil, weather variables have 
the greatest influence on the most suitable crop to grow, and use such insights to guide crop recommendation. To guide selection of 
Features that are most important in dataset for better prediction, we apply Feature Importance and remove data with neglible importance.
We then do performance comparison by observing metrics of "top picks" of the Features list. 
- how do the Accuracies compare? ... did accuracy improve/ degrade/ remain the same ? 
- Plots: >> [https://github.com/altruizim101/Final-Project]
- Feature Engineering


## Explainability of Evaluation & Metrics -
- What is results of analysis telling us?
We employ the Confusion Matrix. The Confusion Matrix for this task provides a detailed view of how well the model predicts each crop class. 
It shows the number of correct and incorrect predictions for each class.
Diagonal entries in the Matrix represent crops that were correctly recommended, while off-diagonal entries show those misclassified.
The Confusion Matrix allows computation of important metrics, including Accuracy, F1-score,  Precision (how often recommended crop(s) 
are actually suitable), Recall (how many of truly suitable crop(s) correctly recommended). 
Through these metrics, the Matrix provides transparent evidence of model performance for each crop, and where recommendations are 
reliable, or where to apply with caution.

## Crop Recommendation - 
The crop recommendation system is implemeted by means of a User-interaction function() that takes in "Input" data from User and outputs a 
recommended crop to user (farmer), with a corresponding Confidence score. The recommendation is presented by means of a
Classification Confidence Report.
- Recommendation via Confidence Report >> [https://github.com/altruizim101/Final-Project]

  
## Classification Report -
From the classification report above, we observe that the crop recommendation system had a perfect score for recommending
Rice, Maze, Kidneybeans, Muskmelon, Apple, Coffee (Accuracy = 1, Precision = 1, F1-score =1).
The system also had a very high score (score >= 0.99) for many other crops, indicating very good recommendation system.
Furthermore, macro-average = 0.98 (overall unbiased), weighted-average = 0.98 (accounting for actual distributions of the data), 
accuracy = 0.98 (system correclty recommends 98% of the time) indicate a consistent strong performance across all crop types, 
The close alignment of the averages indicate unbiased performance of recommendation system with no significant issues that may 
arise due to unbalanced data. The system generalizes well, and not favoring certain crops types over others.
With these observations, it is reasonable to conclude the recommendation system can be considered fair for most of the crop types.
This indicates a robust and fair recommendation system that can deliver accurate, consistent crop recommendation across a borad range of
weather conditions and soil types.


## Project Deliverables -
The final submission should include the Jupyter Notebook and other relevant files, such as the dataset provided and uploaded to a GitHub repository.
## Links to Project Deliverables -
- READMe file with summary of findings >>  [https://github.com/altruizim101/Final-Project]
- 
- Jupyter Notebook Python Code: Link to Jupyter notebook >> [??? xxx ??? ]
-        
- Data Analysis & Results >> [https://github.com/altruizim101/Final-Project]


