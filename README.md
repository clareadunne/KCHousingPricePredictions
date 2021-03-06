# King County Housing Bake-off

This repo contains the materials used to predict house prices in King County, WA. Ultimately, a model was developed with a root mean square error of ~$128,000 for the training data. 

The repo contains: 

- a jupyter notebook detailing EDA and inference process: `Three Things to Tell Outside Investors.ipynb`.
- a jupyter notebook for feature engineering and model development: `Bakeoff_modeling_process.ipynb`.
- a jupyter notebook to predict on holdout data: `Predict_holdout.ipynb`.
- folder containing pickled items.
- folder containing CSVs.
- a inference presentation: `Phase2KingCounty.pdf`.
 

## Inference

- **Exploratory Data Analysis (EDA):** Generated four visualizations. Box plots to identify outliers, scatter plots to determine shape of relationship (linear or otherwise), histograms to see distribution shape, and heatmap to compare correlations at a glance.   

- **Feature Engineering:** Generated dummy variables for zip, as well as binning certain categorical features to smooth distribution. Created zip indexes for mean sales price, median sales price, and public school score. Performed non_linear transforms where necessary. 

- **Statistical Tests:** T_test for independence between houses with a recent renovation and those without (P < 0.05). ANOVA testing on mean price for view rating (P = 0). OLS between price and longitude multiplied by square footage (R_squared = 0.495) 

- **Linear Regression Model:** All features: RMSE of $188,967. Test-train split: Test RMSE $.44% smaller than train RMSE  - the model is not overfit. Add degree_2 polynomial features for top 50 features by Pearson Corr Coeff - this causes model to overfit (~1300 features). Utilised SelectKBest to reduce features to 140 - achieved test RMSE of ~$130,000. Assessed largest residuals to iterate back through engineered features and adjust. Additionally increased number of features passed to poly_2 to 70. Eventually achieved test RMSE of ~$126,000.   

## Holdout predictions

Pickled model and other pertinent data (including SelectKBest columns), engineered matching features for holdout data (`kc_house_data_holdout_features.csv`), generated 4322 predictions for house prices in King County. Test distribution, mean and median of these prices against train data to avoid glaring errors. 



