![nba-logo](https://github.com/chrishunt11/Prediction-Of-Home-Wins/assets/123383359/585476e4-7dfd-4f3c-a530-c7ba8c322ee1)

# NBA Home Games
## Analyzing Home Wins

**Author**: Christopher Hunt


### Business Challenge:

The primary objective of NBA teams is to optimize their performance by winning as many games as possible. However, navigating the constantly evolving game landscape poses a challenge in determining the most efficient approach. Decisions like increasing 3-point attempts or prioritizing shot quality are pivotal in achieving success. This project aims to address these questions to enhance team performance.

### Data Source:

NBA Database: https://www.kaggle.com/datasets/wyattowalsh/basketball

In this dataset there are 65698 rows and 55 features.

### Data Dictionary

** insert dictionary here **

###### To prepare the data, a cleaning process was performed, followed by Exploratory Data Analysis (EDA).

#### Exploratory Data Analysis


- During EDA, histograms and countplots were visualized for all columns, providing insights into Home game statistics. 
- Notably, the top 5 seasons with the highest attempted three-pointers were observed, as well as the bottom 5 seasons with the lowest attempted three-pointers.

![3pt-year](https://github.com/chrishunt11/Prediction-Of-Home-Wins/assets/123383359/012551ae-aa68-40a7-b848-3c11bc7ec00d)

The top 5 three pointers attempted seasons are as follows:

  - 2021:    `56,967.0`
  - 2022:    `46,646.0`
  - 2019:    `41,917.0`
  - 2018:    `39,849.0`
  - 2017:    `37,685.0`
  
The bottom 5 three pointers attempted seasons are as follows:

  - 1986:     `3,397.0`
  - 1987:     `4,526.0`
  - 1988:     `5,433.0`
  - 1989:     `7,724.0`
  - 1990:     `7,826.0`

#### Explanitory Data Analysis

Further analysis included countplots illustrating 3-point percentage over the years, 3-pointers attempted over the years, and the distribution of points from field goals made. These graphs shed light on shot trends and their effectiveness over time.

![3pt-per-year](https://github.com/chrishunt11/Prediction-Of-Home-Wins/assets/123383359/ee440553-67a6-4bb5-887f-a2ce63687875)


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



Model Evaluation & Results:

Among the evaluated models, the 'Tuned Logistic Regression Model' performed the best, yielding high precision and recall scores for both wins and losses.

## Recommendations:

Based on the analysis, teams are encouraged to consider increasing the number of 3-point attempts to enhance their total points, as the 3-point percentage has been increasing over time. Moreover, prioritizing field goals can lead to improved overall point production.

Model Performance:

The 'Tuned Logistic Regression Model' outperformed other models, demonstrating its reliability in predicting game outcomes based on team statistics.

## Limitations & Next Steps

It's essential to acknowledge the limitations of this data, such as the influence of game pace and playstyle on team performance. For future projects, exploring defensive statistics and their impact on winning games could offer valuable insights.

#### For further information:


- Christopher Hunt Jr.
- cjhunt592.1@gmail.com

