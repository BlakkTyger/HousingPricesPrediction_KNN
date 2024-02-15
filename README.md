# Housing price prediction using K Nearest Neighbour Regression

The notebook presents a pipeline to predict Housing Prices, given 79 features that might influence the prices. The project utilizes KNN in order to make the predictions and K Means Clustering to analyze the data. Then, the model is deployed via Gradio. The following methodology has been used for the same:

A) Segregation of Features: Features are segregated into three segments: Continuous, Categorical Values, Discrete Numerical Values


B) Exploratory Data Analysis

Metrics/Toos Used: Coefficient of Variation,  Box Plots, Correlation Matrix

Outcome: To analyze the outliers, Relevance of certain features, and correlation between features


C) Data Preprocessing

    I) Removing features with a huge amount of missing data
  
    II) Imputation of Missing data for remaining columns via KNN Imputation for Numerical Data (continuous and discrete both)
  
    III) Mode-Based Imputation of Object-typed Categorical Values
  
    IV) Winsorizing of data to remove outliers
  
    V) Removing the features which have a Coefficient of Variation of less than or equal to 1
  
    VI) Splitting Object and Num type features and tokenizing Object-typed features, then combining the data
  
    VII) Elimination of features based on a Mutual Info Classification Threshold (heuristically determined threshold)
  
    VIII) Scaling the data via minmax scaler
  

D) Fitting the data in a KNN Model (n = 19)


E) Evaluation of Root Mean Squared Error of log of the output (RMSE = 0.19838051208068913)


F) Implementing K-Means Clustering for insights into the model (No useful insights obtained)


G) Building a user-friendly interface using Gradio

____________________________________________________________________________________________________________________________

Dependencies:
1) pandas, numpy, matplotlib, seaborn, csv, sklearn, scipy, warnings
2) openai, tiktoken, kaleido, cohere, typing-extensions, jiwer, gradio typing-extensions, cast_control==0.10.11

Important Instructions:
1) train.csv and test.csv must be in the same directory as that of the .ipynb file to successfully load them.
2) Kernel Must be restarted post installation of the packages and modules mentioned in point (2) to import gradio successfully.

Submission.csv contains the Predicted Sale Price values for the test dataset 
