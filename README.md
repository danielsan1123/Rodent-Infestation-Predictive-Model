# Rodent-Infestation-Predictive-Model
A simple predictive model to calculate the probability of rat existence with estimated geographical data and infestation status

# Introduction
This project is developed in my Summer course at Baruch College, Data Analytics with machine learning (CIS3920). This is a time-sensitive project due to a short approach in the summer, and we need to learn the concept of Machine Learning and deploy a predicable Machine Learning model in a month. My goal is to estimate the existence of rats in the greater metropolitan area of New York. 

# Data
I contacted DOHMH's (Department of Health and Mental Hygiene) Rodent Inspection and Restaurant Inspection data with the key value of NYC Zip codes. 

# Process
Business understanding: rodents bring economic damage and health hazards to the city area; we primarily know the correlation of rats living with humans hundreds of years ago. 

Data understanding: the dataset I provided a lot of Features, including latitude, longitude, X coordinate, and Y coordinates for Geospatial prediction and precise lot number and block code. The restrain data provides similar and more features such as violation, cuisine description, streets, and phone number. 

# Data Preparation 
I planned to do a numerical prediction base model and eliminate the geographical data.

1. Convert Str to Int/float - Assign Borough to numbers
2. Dropping all missing values
3. Combine two data frames; here rodent data frame has significantly more rows than restaurant data. After combining with an inner merge, there are 56354 rows of data left.
4. Class balancing - both reports in Manhattan is significantly more data points than in other boroughs. We will randomly select 2000 rows for each borough when deploying
      Manhattan        32524
      Bronx             9859
      Brooklyn          6696
      Queens            3875
      Staten Island     3589
   
# Model Selecting 
In this project, I will focus on numerical output and distance base model for fast calculation and optimal result.

KNearestNeightbor Classification

KNN is suitable for recognizing data. As my professor in class said, "If it looks like a duck, it's a duck." The theory is easy to understand, and the concept is easy to implement. This is a greedy approach to the question, and the predicted result is controlled by K (distance value) in the algorithm. The model tends to overfit if we have too few features and low K-values.

Gaussian Naive Bayes Classification

Suitable for continuous variables (5 Borough to 1,2,3,4,5), less complex, and provides good scaling with high dimensional features. However, this classification suffers from subject zero frequency, meaning this classification should not be used for regression. 

Support Vector Machine Classification

Suitable for simple text classification tasks, which represent the frequencies of different words that appear in a data frame. 
Three of the classification employed are very similar since they are all distance-based models. 

Ultimately, I implement voting ensembles to combine the models' prediction and predict for a single data point(Y).

# Example
Here is an example of a prediction, I choose Greenwich Village in Manhattan.
<img width="483" alt="Screenshot 2023-08-22 at 4 06 34 PM" src="https://github.com/danielsan1123/Rodent-Infestation-Predictive-Model/assets/16438259/38b10850-902e-49b8-9f0e-6e0edf2c8656">
# Output
<img width="321" alt="Screenshot 2023-08-22 at 4 05 51 PM" src="https://github.com/danielsan1123/Rodent-Infestation-Predictive-Model/assets/16438259/413fec6f-20bc-466f-af84-2c361b9e0827">

download the file and try today =)

