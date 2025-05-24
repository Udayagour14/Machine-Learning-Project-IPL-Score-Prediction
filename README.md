# Machine-Learning-Project-IPL-Score-Prediction
### 1.Project overview
This project aims to predict the total score of a cricket team at the end of their innings during an IPL (Indian Premier League) match. The model is built using historical data from IPL seasons 1 to 9 (2008-2016) and tested on data from season 10 (2017). The model uses various machine learning algorithms to predict the score based on input features such as the batting and bowling teams, overs, runs, wickets, and other match statistics.


### 2. Data Understanding


**2.1 Data Collection**

The dataset used for this project is an IPL dataset (ipl.csv) containing match statistics for each ball bowled in a match. The dataset includes:
●Batting team
●Bowling team
●Overs (current over in the match)
●Runs scored in that over
●Wickets taken in that over
●Runs in last 5 overs
●Wickets in last 5 overs
●Total score of the batting team at the end of the innings
●Date of the match

**2.2 Upload & Preprocess Dataset**
✔ Load IPL match data containing features like team names, overs, runs, wickets, and past performance.

**2.3 Data Exploration**

●The dataset contains multiple columns such as match ID, venue, batsman, bowler, striker, non-striker, etc.
●We perform basic data exploration, such as checking the shape of the dataset, data types, and the first few records, to understand the structure of the data.

✔ Handle missing values by using techniques like median imputation for numerical features.

**3. Encoding**

✔ One-hot encode categorical features (batting team, bowling team) to convert team names into numerical format.
✔ Scale numerical features using StandardScaler to ensure consistent input values.

**4.Train & Evaluate Models**
✔ Train multiple regression models using dataset:
- Linear Regression (Baseline model)
- Decision Tree Regression (Handles nonlinear relationships)
- Random Forest Regression (More stability and generalization)
- AdaBoost Regressor (Boosts weak learners for better accuracy)

  **5.Evaluate models using error metrics**
- Mean Absolute Error (MAE) – Measures average prediction error.
- Mean Squared Error (MSE) – Penalizes large mistakes in predictions.
- Root Mean Squared Error (RMSE) – Converts MSE back to original units for better interpretation.
- 
  **6.Make Predictions**
✔ Use trained models to predict total scores for matches.
✔ Ensure feature alignment between input data (X_test) and model (X_train).
✔ Run predictions dynamically for different IPL matches, ensuring expected output format.
✔ Check prediction accuracy by comparing results with real match scores.

 **7. Model Comparison**
| Model | MAE (Lower is better) | MSE (Lower is better) | RMSE (Lower is better) | 
| Linear Regression | 0.4569 (Best) | 0.3899 (Best) | 0.6245 (Best) | 
| Decision Tree | 0.6131 (Worst) | 0.7080 (Worst) | 0.8415 (Worst) | 
| Random Forest | 0.5043 (2nd Best) | 0.4580 (2nd Best) | 0.6768 (2nd Best) | 
| AdaBoost with LR | 0.5226 (3rd Best) | 0.4271 (3rd Best) | 0.6535 (3rd Best) | 


/**Linear Regression performed best, but Random Forest & AdaBoost were strong alternatives.
Decision Tree had the highest error, possibly due to overfitting.**/
