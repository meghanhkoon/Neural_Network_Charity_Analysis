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

## Summary 
