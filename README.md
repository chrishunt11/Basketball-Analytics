# NBA Home Games
## Analyzing Home Wins

**Author**: Christopher Hunt

### Business Problem:

The main objective for NBA teams is to win as many games as possible, but the challenge is figuring out the most efficient way possible. Since the game is constantly changing, the most efficient way to win has varied over the years. Should teams shoot more 3's? Should they shoot as many shots as possible regardless if they are good shots or not? Figuring out the answer to these questions is what I am trying to solve.

### Data Source:

NBA Database: https://www.kaggle.com/datasets/wyattowalsh/basketball

In this dataset there are 65698 rows and 55 features.

### Data Dictionary


### To prepare this datam the data was cleaned, and the following processes were performed:

#### Exploratory Data Analysis

- During exploratory data analysis, a histogram and a countplot was visualized for all columns.
- This gave a good baseline for the stats amongst all Home games played.

- ** insert graph here **

  description of graph here

#### Explanitory Data Analysis

- During explanitory data analysis, countplots of 3 point percentage over the years, 3 pointers attempted over the years, and distribution of points amongst field goals made.
- Taking a look at these graphs gave a good understanding of the types of shots taken over the years and the percentage they were made.
- This also gave a better understanding of more field goals made means more points scored.

** insert graph here **

description of graph here

### Machine Learning Using the following Models:
  - KNN Model
  - Tuned KNN Model
  - Decision Tree Classifier
  - Tuned Decision Tree Classifier
  - XGBoost
  - LightGMB
  - Logisitic Regression
  - Tuned Logisitic Regression

## Models Evalustaed & Results:
  - KNN Model (Testing Set):
    
                   precision / recall / f1-score
        0 (loss):     .76    /   .69   /   .72
        1 (win):      .80    /   .85   /   .82
        accuracy:                      /   .78
        macro avg:    .78    /   .77   /   .77
        weighted avg: .78    /   .78   /   .78
  
  - KNN Tuned Model (Testing Set):
    
                   precision / recall / f1-score
        0 (loss):     .81    /   .70   /   .75
        1 (win):      .81    /   .89   /   .85
        accuracy:                      /   .81
        macro avg:    .81    /   .79   /   .80
        weighted avg: .81    /   .81   /   .81

  - Decision Tree Classifier Model (Testing Set):
    
                    precision / recall / f1-score
        0 (loss):     .68    /   .68   /   .68
        1 (win):      .78    /   .78   /   .78
        accuracy:                      /   .74
        macro avg:    .73    /   .73   /   .73
        weighted avg: .74    /   .74   /   .74

  - Tuned Decision Tree Classifier Model (Testing Set):
    
                   precision / recall / f1-score
        0 (loss):     .72    /   .69   /   .71
        1 (win):      .80    /   .82   /   .81
        accuracy:                      /   .77
        macro avg:    .76    /   .76   /   .76
        weighted avg: .77    /   .77   /   .77

  - XGBoost Model (Testing Set):
    
                   precision / recall / f1-score
        0 (loss):     .82    /   .78   /   .80
        1 (win):      .85    /   .88   /   .87
        accuracy:                      /   .84
        macro avg:    .84    /   .83   /   .83
        weighted avg: .84    /   .84   /   .84

  - LightGMB Model (Testing Set):

                   precision / recall / f1-score
        0 (loss):     .82    /   .78   /   .80
        1 (win):      .86    /   .88   /   .87
        accuracy:                      /   .84
        macro avg:    .84    /   .83   /   .83
        weighted avg: .84    /   .84   /   .84

  - Logisitic Regression Model (Testing Set):

                   precision / recall / f1-score
        0 (loss):     .82    /   .80   /   .81
        1 (win):      .86    /   .88   /   .87
        accuracy:                      /   .85
        macro avg:    .84    /   .84   /   .84
        weighted avg: .85    /   .85   /   .85

  - Tuned Logisitic Regression Model (Testing Set):

                   precision / recall / f1-score
        0 (loss):     .82    /   .80   /   .81
        1 (win):      .86    /   .88   /   .87
        accuracy:                      /   .85
        macro avg:    .84    /   .84   /   .84
        weighted avg: .85    /   .85   /   .85

- The Final Model chosen was the 'Tuned Logisitic Regression Model' with the 
