## 1. Summary of Changes

- Tested Random Forest model.    
- Metrics and models are logged in /Artifacts/.      

## 2. Results

| Version | Model            | RMSE ↓ | Main Parameters                                                        |  
|-------|------------------|--------|------------------------------------------------------------------------|  
| v0.1  | LinearRegression | 53.85  | StandardScaler + LinearRegression                                      |  
| v0.2  | RandomForest     | 53.19  | max_depth = 5, n_estimators = 500, min_samples_leaf=5, random_state=42 | 

## 3. Discussion

- The results indicate that the Random Forest model (v0.2) slightly outperforms the Linear Regression model (v0.1) in terms of RMSE, achieving 53.19 compared to 53.85. While the improvement is modest, it demonstrates that introducing a non-linear model can better capture the underlying patterns in the data.
- Despite the improvement, the RMSE values indicate that there is still considerable prediction error.  
- 
## 4. Reproducibility

- Fixed seed = 42
- Environment: Written in requirements.txt.  
- Artifacts: Trained models, evaluation metrics, and experiment logs are saved in the /Artifacts/ directory.  

