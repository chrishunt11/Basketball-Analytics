# NBA Game Prediction & Model Risk Analysis

**Author:** Christopher Hunt Jr.

## Project Overview

This project predicts whether the home team will win an NBA game using historical team performance from games that occurred before the game being predicted.

This is a rebuilt version of an earlier NBA machine learning project. While reviewing the original model, I found that it used statistics from the same game it was trying to predict. This created data leakage and made the original accuracy of about 85% misleading.

I rebuilt the project to remove that leakage, use a time-based validation approach, compare multiple machine learning models, and analyze how the final model performed on newer data.

## Data Source

[NBA Database](https://www.kaggle.com/datasets/wyattowalsh/basketball)

The original dataset contains **65,698 NBA games**. Because several statistics had large amounts of missing data in older seasons, I limited the modeling period to games from **1995 onward** and included regular-season and playoff games.

After cleaning the data and creating the historical features, the final modeling dataset contained **34,410 games**.

## Preventing Data Leakage

Preventing data leakage was one of the most important parts of rebuilding this project.

Instead of using statistics from the game being predicted, each team's features were calculated using its **previous 10 games**.

The rolling calculations were shifted by one game so the current game's statistics could not be included in its own prediction.

Features included:

- Recent win percentage
- Average points
- Field goal percentage
- Three-point percentage
- Free throw percentage
- Rebounds
- Assists
- Turnovers

## Train, Validation, and Test Split

Because NBA games happen over time, I used a chronological split instead of randomly splitting the data.

- **Training:** 1995–2018
- **Validation:** 2019–2020
- **Test:** 2021–2023

The test period was kept separate while selecting the model, tuning hyperparameters, and choosing the classification threshold.

## Models Compared

I compared four machine learning approaches:

- Logistic Regression
- Random Forest
- XGBoost
- Neural Network

The tuned **XGBoost** model performed best on the validation data and was selected as the final model.

Final XGBoost configuration:

- Maximum tree depth: 4
- Learning rate: 0.03
- Number of estimators: 200
- Classification threshold: 0.55

## Model Results

### Validation

- **Accuracy:** 63.7%
- **ROC-AUC:** 0.668
- **Home-team baseline:** 55.6%

### Untouched Test Set

- **Accuracy:** 59.9%
- **ROC-AUC:** 0.622
- **Home-team baseline:** 56.0%
- **Home-win recall:** 73%
- **Away-win recall:** 44%

The model remained more accurate than simply predicting the home team to win every game, but performance declined from the validation period to the newer test period.

Instead of changing the model after seeing the test results, I treated the decline as a model-risk finding and investigated it further.

## Performance Over Time

| Year | Games | Home Win Rate | Model Accuracy | ROC-AUC |
|---|---:|---:|---:|---:|
| 2021 | 1,625 | 54.6% | 60.5% | 0.635 |
| 2022 | 1,336 | 57.5% | 60.3% | 0.612 |
| 2023 | 768 | 56.1% | 58.1% | 0.612 |

The model remained above the home-team baseline during each test year, but the advantage became smaller over time.

## Model Risk & Validation

After evaluating the final model, I looked beyond accuracy to understand where the model could become unreliable.

### Feature Drift

Several features changed between the training and test periods.

The largest changes were in scoring and assists. Home and away scoring features had KS statistics above **0.71**, showing a large difference between their training and test distributions.

This does not prove that feature drift caused the performance decline, but it shows that newer NBA games were different from much of the data the model learned from.

### Probability Calibration

The model's Brier score increased from:

- **Validation:** 0.2279
- **Test:** 0.2383

Because a lower Brier score is better, the model's predicted probabilities became less reliable on newer data.

The model also showed signs of being overconfident at higher predicted home-win probabilities.

### Error Analysis

The model was correct on:

- **62.1%** of predicted home wins
- **55.7%** of predicted away wins

There were also **307 incorrect predictions** where the model was at least 70% confident. These represented **20.54% of all model errors**.

This showed that a high confidence score did not always mean the prediction was reliable.

## Key Model Risks

The main risks identified during the project were:

- Data leakage
- Performance drift
- Feature drift
- Probability calibration
- High-confidence errors
- Different performance between home and away predictions
- Overfitting
- Historical data becoming less representative of newer NBA games

A monitoring plan was also created to track model accuracy, ROC-AUC, feature drift, calibration, class performance, high-confidence errors, and data quality if the model were deployed.

## Limitations

The model only uses historical team performance. It does not include several factors that could affect the outcome of a game, including:

- Injuries
- Starting lineups
- Player availability
- Rest days
- Travel
- Roster changes
- Betting-market information

The 10-game rolling features also continue across season boundaries, meaning the first few games of a new season can include information from the previous season.

The training data covers many years of NBA history, and the drift analysis showed that the way the game is played has changed over time.

The same validation period was also used for model tuning and threshold selection. A future version could use multiple time-based validation periods.

## Key Takeaway

The biggest lesson from this project was that higher model accuracy does not automatically mean a better model.

The original version appeared to achieve about **85% accuracy**, but that performance was partly caused by data leakage.

After rebuilding the feature pipeline and testing the model on future data, the final model achieved **59.9% accuracy compared with a 56.0% baseline**.

The accuracy is lower, but the evaluation is much more realistic. The project also shows how data leakage, performance drift, feature drift, calibration, and model limitations can affect whether a machine learning model should actually be trusted.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- SciPy
- Google Colab

## Contact

**Christopher Hunt Jr.**

[LinkedIn](https://www.linkedin.com/in/christopher-hunt-jr)
