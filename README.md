![nba-logo](https://github.com/chrishunt11/Prediction-Of-Home-Wins/assets/123383359/585476e4-7dfd-4f3c-a530-c7ba8c322ee1)

# NBA Home Games Analysis
## Unveiling Patterns in Home Wins

**Author**: Christopher Hunt Jr.


### Business Challenge:

The primary objective of NBA teams is to optimize their performance by winning as many games as possible. However, navigating the constantly evolving game landscape poses a challenge in determining the most efficient approach. Decisions like increasing 3-point attempts or prioritizing shot quality are pivotal in achieving success. This project aims to address these questions to enhance team performance.

### Data Source:

[NBA Database](https://www.kaggle.com/datasets/wyattowalsh/basketball): 65,698 rows and 55 features.

### Data Dictionary

Access the [Data Dictionary](https://docs.google.com/document/d/1GjDnyGpwIL14WoHZABzBqnB7sjCTNyHZxJRKZSyqwlg/edit?usp=sharing) for comprehensive insights.

###### **To prepare the data, a cleaning process was performed, followed by Exploratory Data Analysis (EDA).**

#### Exploratory Data Analysis:


- During EDA, histograms and countplots were visualized for all columns, providing insights into Home game statistics. 
- Notably, the top 5 seasons with the highest attempted three-pointers were observed, as well as the bottom 5 seasons with the lowest attempted three-pointers.

![3pt-year](https://github.com/chrishunt11/Prediction-Of-Home-Wins/assets/123383359/012551ae-aa68-40a7-b848-3c11bc7ec00d)

The top 5 three pointers attempted seasons are as follows:

  - 2021:    `56,967`
  - 2022:    `46,646`
  - 2019:    `41,917`
  - 2018:    `39,849`
  - 2017:    `37,685`
  
The bottom 5 three pointers attempted seasons are as follows:

  - 1986:     `3,397`
  - 1987:     `4,526`
  - 1988:     `5,433`
  - 1989:     `7,724`
  - 1990:     `7,826`

![avg-3ptm-top-vs-bot](https://github.com/chrishunt11/Prediction-Of-Home-Wins/assets/123383359/e21ff5fd-0f3e-4699-aadb-1728f1436233)


**The visual aid provided shows a clear trend:**
- Among the upper echelon of the league's standings, top teams distinguished by their superior home win records have conspicuously raised their average number of successful 3-pointers made per game.

- This strategic transition serves as a testament to their adeptness in adapting to evolving competitive landscapes.

- By incorporating an amplified emphasis on long-range shots into their gameplay strategy, these teams are strategically positioning themselves to:
  - Exploit scoring opportunities 
  - Enhance their overall on-court performance.


#### Explanitory Data Analysis:

Further analysis included countplots illustrating 3-point percentage over the years, 3-pointers attempted over the years, and the distribution of points from field goals made. These graphs shed light on shot trends and their effectiveness over time.

![3pt-per-year](https://github.com/chrishunt11/Prediction-Of-Home-Wins/assets/123383359/ee440553-67a6-4bb5-887f-a2ce63687875)


### Machine Learning Leveraging Multiple Models:
  - KNN Model (default/tuned)
  - Decision Tree Classifier (default/tuned)
  - Logisitic Regression (default/tuned)
  - XGBoost
  - LightGMB

## Evaluated Models & Results:
  - Default KNN Model (Testing Set):
    
                   precision / recall / f1-score
        0 (loss):     .76    /   .69   /   .72
        1 (win):      .80    /   .85   /   .82
        accuracy:                      /   .78
        macro avg:    .78    /   .77   /   .77
        weighted avg: .78    /   .78   /   .78
  
  - Tuned KNN Model (Testing Set):
    
                   precision / recall / f1-score
        0 (loss):     .81    /   .70   /   .75
        1 (win):      .81    /   .89   /   .85
        accuracy:                      /   .81
        macro avg:    .81    /   .79   /   .80
        weighted avg: .81    /   .81   /   .81

  - Default Decision Tree Classifier Model (Testing Set):
    
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

  - Default Logistic Regression Model (Testing Set):

                   precision / recall / f1-score
        0 (loss):     .82    /   .80   /   .81
        1 (win):      .86    /   .88   /   .87
        accuracy:                      /   .85
        macro avg:    .84    /   .84   /   .84
        weighted avg: .85    /   .85   /   .85

  - Tuned Logistic Regression Model (Testing Set):

                   precision / recall / f1-score
        0 (loss):     .82    /   .80   /   .81
        1 (win):      .86    /   .88   /   .87
        accuracy:                      /   .85
        macro avg:    .84    /   .84   /   .84
        weighted avg: .85    /   .85   /   .85


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





### **Suggested Model:**

Among the evaluated models, the 'Tuned Logistic Regression Model' performed the best, yielding high precision and recall scores for both wins and losses.

## **Recommendations**:

Based on the analysis, teams are encouraged to consider increasing the number of 3-point attempts to enhance their total points, as the 3-point percentage has been increasing over time. Moreover, prioritizing field goals can lead to improved overall point production.

## Limitations & Next Steps:

It's essential to acknowledge the limitations of this data, such as the influence of game pace and playstyle on team performance. For future projects, exploring defensive statistics and their impact on winning games could offer valuable insights.

#### Contact information:

For any further inquiries or information, please contact:
- Christopher Hunt Jr.
- LinkedIn Profile: [Christopher Hunt Jr. on LinkedIn](https://www.linkedin.com/in/christopher-hunt-jr)
- Email Address: cjhunt592.1@gmail.com
