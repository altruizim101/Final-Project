# -- Capstone Project, 15 January 2026 --
# -- Final Report for a Crop Recommendation System ---
#

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

## -- Goal -- 
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

## -- Challenges, Pitfalls --
Developing a robust and effective model for crop recommendation has several challenges. Accurate recommendations depend on 
reliable (soil & weather) data. This data may be incomplete, outdated, or inconsistent across regions. The models trained on data 
from one location may not generalize well to different climates, soil types, or farming practices without local adaptation. Further, 
unpredictable weather patterns can reduce the reliability of historical data used for training the model. Most importantly, farmers may 
be hesitant to rely on ML-based recommendations without proven past results and clear explanations.

## -- Potential Benefits -- 
An ML-based crop recommendation system offers several important benefits for farming. By matching crops to local soil and weather 
conditions, it helps improve crop yields and overall productivity. More accurate crop selection leads to lower operational costs
by reducing spending on water, fertilizers, and pesticide. The system minimizes farming risks by discouraging unsuitable crop choices, 
reducing the likelihood of crop failure under poor farming conditions. In addition, optimized crop planning promotes sustainable farming 
practices by supporting better soil health and more efficient use of natural resources over time.

## -- Approach and steps --
The features of the dataset (from Kaggle platform) include following parameters: soil nutrients phosphorus (P), potassium (K), and nitrogen (N),
and weather characteristics temperature, humidity, rainfall, and soil pH. The target is the crop label (crop name).
We apply the following steps in this exercise: 
1) data cleaning & pre-processing 2) data visualization & understanding 3) Feature Selection 4) employ multiple ML algorithms with
hyperparameter tuning 5) select optimal ML algorithm 6) select the important Features (permutation importance) and 
7) make recommnedations using optimal ML algorithm with most important Features.

## -- Data Visualization & Understanding --
We first load and visualize the data to gain understanding of dataset, features & distributions through Histograms, Scatter plots, 
Boxplots, Violin plots, and features relationship uisng Correlation matrix, Covariance matrix, and Pairplots. Understanding of data
facilitates in selection and application of appropriate ML techniques in the data analysis.
The data contains 2,200 samples with 22 unique crops types in "label" column, for a total of 100 samples per crop type.
The data is eight (8) columns with seven (7) Features and a Target ("label" column).

## -- Data Outcome and Predictions --
As classification exercise, we compared various ML models (including K-Nearest Neighbors, Random Forest, Gradient Boost, 
Support Vector Machine (SVM), Logistic Regression and then select the optimal ML model (through hypeparameter tuning) to 
employ for crop recommendation.
To further optimize model, we apply Feature Engineering and K-fold Cross-Validation techniques to improve precision of recommendation 
from the data. The optimal ML model is determined by comapring performance measures of precision, recall, F1 score, and Confusion Matrix.


## Data preprocessing & Visualizations
>> Check for possible Null (NaN) values in data for removal before analysis. Then filtered NaN data as appropriate.
>> Action: remove missing (NaN) data in columns.

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

## Explainability of Analysis
-- What is results of analysis telling us?

## Recommendations
- Make recommendations on crops based on evaluations from above (TBD)



## Project Deliverables
The final submission should include the Jupyter Notebook and other relevant files, such as the dataset provided and uploaded to a GitHub repository.
## Links to Project Deliverables
- READMe file with summary of findings >>  [https://github.com/altruizim101/Final-Project]
- Link to Jupyter notebook here >> [https://github.com/altruizim101/Final-Project/blob/main/00_CapstoneProj_cropRecommend_JupiterNotebook_DataAnalysis_20p1.ipynb]         
- Data Analysis & Results >> [https://github.com/altruizim101/Final-Project]


