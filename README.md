Challenge 19
# Neural_Network_Charity_Analysis

## Overview of the analysis

### i. Project purpose
A nonprofit foundation, Alphabet Soup, has raised and donated over 10 billion dollars in the past 20 years to invest in lifesaving technologies and organize reforestation groups. The foundation needs an analysis to ensure that its money is being used effectively. To meet this need, a deep learning neural network will be designed and trained through the project.

### ii. Dataset received for analysis
The dataset contains more than 34,000 organizations that have received funding from Alphabet Soup and captures the following data about organizations:
- **EIN** and **NAME** - Identification columns
- **APPLICATION_TYPE** - Alphabet Soup application type
- **AFFILIATION** - Affiliated sector of industry
- **CLASSIFICATION** - Government organization classification
- **USE_CASE** - Use case for funding
- **ORGANIZATION** - Organization type
- **STATUS** - Active status
- **INCOME_AMT** - Income classification
- **SPECIAL_CONSIDERATIONS** - Special consideration for application
- **ASK_AMT** - Funding amount requested
- **IS_SUCCESSFUL** - Whether the money was used effectively

### iii. Project goal
The goal of the project is to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.


## Results

### i. Data preprocessing
- **Target variable**\
**IS_SUCCESSFUL** is considered the target of the model.
- **Features variables**\
The following variables are considered the features: **APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, ASK_AMT**.
- **Removed variables**\
**EIN** and **NAME** are removed as they are identification. In addition, after further review of the dataset, it has been noted that almost all organizations are active in **STATUS** with No **SPECIAL_CONSIDERATIONS**. These features are eliminated for simplification. Finally, the number of categories in **APPLICATION_TYPE, CLASSIFICATION,** and **INCOME_AMT** are reduced.

### ii. Compiling, training, and evaluating the model
- **Neural network specifications**\
  Each layer is defined as follows:
    - First layer – 80 neurons and “relu” activation function
    - Second layer – 40 neurons and “relu” activation function
    - Third layer – 20 neurons and “tanh” activation function, expecting a different type of activation to improve the model performance.
    - Output layer – one neuron with “sigmoid” activation function
- **Model performance**\
  The model results in 72.47% of accuracy eventually.
- **Steps for model performance improvement**\
  The steps include the following:
    - Eliminating of **STATUS** and **SPECIAL_CONSIDERATIONS** columns
    - Binning of **INCOME_AMT** column
    - Increasing the number of neurons from 30 to 40 in the second layer
    - Adding the third layer with 20 neurons and “tanh” activation function which is never used in other layers


## Summary
### i. Overall results
The first model achieved 72.52% of accuracy. However, in spite of multiple times of trial with different preprocessing and layer definitions, 75% of accuracy has never been achieved. 

### ii. Recommendations
  ### Analysis of numerical feature
  ASK_AMT is the only numerical value in the dataset, and there are some outliers as shown below. Although values are scaled through preprocessing, it may be appropriate to determine whether those outliers result in the model performance without achieving 75% of accuracy.
  
  <img src="https://github.com/Ryoichi2022/Neural_Network_Charity_Analysis/blob/main/Funding_Amount.png" width="600"/>  

  ### Improvement of features
  Performance of a neural network will be dependent on the quality of features. By reviewing how significantly each feature i.e., APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT influence the target variable and preprocessing the dataset accordingly, the model could improve its performance.
  
  ### Possibility of overfitting
  80 neurons are used in the first layer, 40 in the second layer, and 20 in the third layer. It is necessary to ensure that the number of neurons is reasonable and does not cause overfitting issue in the model.
