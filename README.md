# Neural_Network_Charity_Analysis
Neural Networks and Deep Learning Models 

## Overview of the Analysis
**Background and Purpose**
With knowledge from machine learning and neural networks, the features in the dataset will help create a binary classifier to help predict whether applicants will be successful if funded by Alphabet Soup. The purpose of this project is to use deep-learning neural networks to analyze and classify the success of charitable donations funded by Alphabet Soup. 

Specifically, we will: 
- Deliverable 1: Preprocessing Data for a Neural Network Model
- Deliverable 2: Compile, Train, and Evaluate the Model
- Deliverable 3: Optimize the Model
- Deliverable 4: A Written Report on the Neural Network Model (README.md)

### Resources 
- Original Data Source: [charity_data.csv](https://github.com/meghanhkoon/Neural_Network_Charity_Analysis/blob/main/Resources/charity_data.csv)
- Software: Python, Anaconda ```mlenv``` environment, Jupyter Notebook/ Google Colab, Python Libraries: ```sklearn```, ```pandas```, and ```tensorflow```

## Results
### Data preprocessing
Original DataFrame containing our original data source: [charity_data.csv](https://github.com/meghanhkoon/Neural_Network_Charity_Analysis/blob/main/Resources/charity_data.csv)
<img width="1892" alt="Screenshot 2023-01-13 at 9 32 27 AM" src="https://user-images.githubusercontent.com/110576028/212403358-c683ff7d-7d7d-4173-8927-6841c16c1c97.png">

1. What variable(s) are considered the target(s) for your model?
- The variable column ```IS_SUCCESSFUL``` is the **target** for this model. This column determines (using binary data - 1 (Successful) and 0 (Not Successful)) if the money was used effectively. 

2. What variable(s) are considered to be the features for your model?
- The **features** of this model are: ```APPLICATION_TYPE```, ```AFFILIATION```, ```CLASSIFICATION```, ```USE_CASE```, ```ORGANIZATION```, ```STATUS```, ```INCOME_AMT```, ```SPECIAL CONSIDERATIONS```, and ```ASK_AMT```. Using these features, we first looked at value counts for binning, if there were more than 10 values we replaced the dataframe with binning, encoded the categorical variables with ```OneHotEncoder``` function, merged and dropped the originals, then split, scaled and standardized the training and testing datasets. 

3. What variable(s) are neither targets nor features, and should be removed from the input data?
- Originally, the only variables that were removed from the input data were ```NAME``` and ```EIN```. These are both identification columns. However, after optimization, we ended up dropping ```STATUS``` and ```SPECIAL_CONSIDERATIONS``` as well. 


### Compiling, Training and Evaluating the Model 
1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
- In the original model, layer 1 had 80 neurons with a relu activation. The second hidden layer had 30 neurons. Lastly, the output layer used an activation "sigmoid". 

2. Were you able to achieve the target model performance?
- After the original model, we were able to achieve only 72.5% Accuracy with a Loss of 0.56. This is not a satisfying target model performance for predicting the outcome of success for the charity donations.

3. What steps did you take to try and increase model performance?
- Since we had below a 75% Accuracy rate, the following trials were done to try and reach for optimization levels. However, after trying three different times, we were still not able to reach 75% accuracy levels. 
- First, features ```STATUS``` and ```SPECIAL_CONSIDERATIONS``` were dropped. 
- Then, binning numbers were increased to reduce the value counts for the ```CLASSIFICATION``` column. 
- Next, we experimented with adding neurons, hidden layers, and changing the activation functions. 
- Overall, we could not get the desired 75% Accuracy levels for this deep-learning model. 

## Summary 
The deep learning neural network model could not reach 75% Accuracy Levels even with experimenting with different techniques for optimization. For future reference, we could try a different machine learning model such as a Supervised Random Forest Classifier since Random forest models and neural networks can handle nonlinear and tabular data.  Both output and feature selection of random forest models are able to handle outliers and nonlinear data. From looking at the value counts for some of the features, we know that ```ASK_AMT``` column had many outliers. 
