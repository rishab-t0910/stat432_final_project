# STAT 432 Final Project Readme.md
This is my group project for STAT 432 - Basics of Statistical Learning at UIUC. The goal is to construct 2 classification models and 2 regression models on a World Health Organization (WHO) dataset to determine Life Expectancy. I will be working on the Logistic Regression (Classification) and Random Forest (Regression) model, while my group mate does Linear Regression and K-nearest neighbours. 

Should be fun!

### 31 March 2024
Created the Github repo with the files. Finished the initial logistic regression portion. I have found some variables of interest based on correlation analysis, and conducted my regression. We find a relatively low classification error ~ 0.25, but this also means 1 in 4 classifications is wrong. This is something I need to fix in the future. 

##### Next Steps
1. Better the error for the model
    a. This could be changing the inputs, scaling, creating multiple classes for life expectancy
2. Calculate sensitivity and specificity

### 6 April 2024
Trimmed down the number of predictors and scaled the inputs. It seems like a better model now. Calculated the accuracy scores, and also checked the quality of the model against the training data. Again, could be better but we are moving in the right direction. 

##### Next Steps
1. Cluster analysis to see if 3 classes are correct for life expectancy
2. Move on the Random Forest

### 9 April 2024
I learned today that Clustering (K-means) is an unsupervised learning method, hence there is no way to determine the optimal number of clusters. So, there is no way to tell if 3 classes is the ideal, but since it is easy to interpret, I stick with it. I conducted the Random Forest, and the results are quite good. Low MSE and MAPE for both the training and testing data shows that the model does a good job. 

I brought back the variables with low variance as I thought it would be useful, and the results do improve. 

##### Next Steps
1. Find an updated dataset with the current year data, and try to validate the model