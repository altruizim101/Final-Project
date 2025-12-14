# -- Final Capstone Project -- 

## Title: Precision Agriculture & Crop Recommendations.

### Data Source: [https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset/data]
### Data Summary:
[Kaggle] ... "Recommendations from evaluation of this dataset with Machine Learning techniques will aid farmers in making informed decisions in their farming strategy. 
This dataset allows the users to build a predictive model to aid in recommendations for suitable crops to grow in a particular farm based on various parameters."

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
The drive to produce, healthy, nutritous, and abundant food supply with less resources through thoughtful planning and responsible farming practices,
by employing accessible and affordable technologies ien mass.



## Deliverables
The final submission should include the Jupyter Notebook and other relevant files, such as the dataset provided and uploaded to a GitHub repository.

## Links to Project Deliverables
- READMe file with summary of findings >>  
- Link to Jupyter notebook here >>         
- Data Analysis & Results >>

## (Data Understanding)
Checked for possible Null (NaN) values in data for removal before analysis. Then filtered NaN data as appropriate.
Action: removed missing (NaN) data in columns

## Data Visualizations
Correlation Matrix:
- Strong positive correlation of about +0.76 observed betwee Potassium (K) and Phosphorous (P).
- Weak positive correlation (~0.22) between Humidity and rainfall.
- Weak positive correlation (~0.19) between Humidity and Nitrogen (N).

![plot](/Users/m.jalloh/Downloads/00_FinalApp_CropRecommend/CorrMatrtix.png)

![plot](/Users/m.jalloh/Downloads/00_FinalApp_CropRecommend/CovaMatrix.png)


Histograms and Feature Distribution:
- A Binomial distribution is observed for Nitrohen.
- Temperature and pH approach a normal distribution.
- Humidity is left-skewed.
- Rainfall is right-skewed distribution.
- Potassium (K) is right-skewed distribution.
![plot](/Users/m.jalloh/Downloads/00_FinalApp_CropRecommend/Histogram.png)

Boxplots of Features:
- pH shows the narrowest distribution, with smallest variance, followed by Teamperature.
- Humidity and Potassium (K) shows comaprable variances.
- Rainfall and Nitrgen shows the laragest variances.
![plot](/Users/m.jalloh/Downloads/00_FinalApp_CropRecommend/Boxplots.png)

ViolinPlots of Features:
- pH shows the narrowest distribution, with smallest variance, followed by Teamperature.
- Humidity and Potassium (K) shows comaprable variances.
- Rainfall and Nitrgen shows the laragest variances.
![plot](/Users/m.jalloh/Downloads/00_FinalApp_CropRecommend/Violinplots.png)


## Data Analysis & Transformation
- Feature Engineering

## Evaluations - Models and Metrics
- Technicques & ML models applied
- Metrics for eval: MMSE, MAE, Accuracy score, ...
- ...

## Recommendations
- Make recommendations on crops based on evaluations from above.

