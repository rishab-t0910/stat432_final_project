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
Trimmed down the number of predictors and scaled the inputs. It seems like a better model now. Calculated the accuracy scores, and also checked the quality of the model against the training data. Got the testing error down to 16.5%. The model could be better but we are moving in the right direction. 

##### Next Steps
1. Cluster analysis to see if 3 classes are correct for life expectancy
2. Move on the Random Forest

### 9 April 2024
I learned today that Clustering (K-means) is an unsupervised learning method, hence there is no way to determine the optimal number of clusters. So, there is no way to tell if 3 classes is the ideal, but since it is easy to interpret, I stick with it. I conducted the Random Forest, and the results are quite good. Low MSE and MAPE for both the training and testing data shows that the model does a good job. 

I brought back the variables with low variance as I thought it would be useful, and the results do improve. 

##### Next Steps
1. Find an updated dataset with the current year data, and try to validate the model

### 18 April 2024
I worked on the random forest model, and considered cutting down the size of it. I tried to output the picture of the forest but python isn't very good at that so I moved to R. I will be uploading the R markdown file as well. 

### 22 April 2024
I realized that the Random Forest implementation is not easy in Python especially with visualization. However, the R implementation is very good. So I copied the data files, used the same training and testing data and redid the random forest in R, and removed it from Python. Lastly, I looked to prune the Random forest I constructed but that was the same as the original random forest. I also included a plot of the variable importance. 

##### Next Steps
1. Consider encoding the choice of class as follows
    - Take the average of the probabilities
    - Figure out the percentage of high, low, medium from the original df (eg 60-20-20)
    - Then create the cutoff value based on that
    - See if this changes the confusion matrix

### 25 April 2024
Changing the cutoffs sparked a new thought - what if we changed the way we encode "high", "low", "medium". So after tinkering this and trying 2 classes instead of 3, we get some new results. For 2 classes, we check multiple splits and multiple cutoffs, and finalise that our best model is when we have a 0.3-0.7 high-low split with a 0.5 cutoff. 

### 27 April 2024
Started writing the report for the class, and did the following
1. Included a images and data folder to clean up the file system
2. Included the logistic regression equation
3. Created random forest with multiple parameters

### 1 May 2024
This brings me to the end of the semester and the project. It was quite interesting working with this dataset which did not have the best quality. I learned quite a lot in my modelling and found some very good results. 
1. Logistic Regression - 2 class, 30-70 high-low split, 0.5 cutoff, Test Classification Error = 0.056
2. Random Forest - Test MSE = 3.2212

We can look to use other classification models, or other more complicated models for regression. The current models are good, and can definitely be used. Furthermore, better data would help make better models. 