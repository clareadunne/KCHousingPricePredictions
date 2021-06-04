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

- **Exploratory Data Analysis (EDA):** You must create **at least 4 data visualizations** that help to explain the data. These visualizations should help someone unfamiliar with the data understand the target variable and the features that help explain that target variable.

- **Feature Engineering:** You must create **at least 3 new features** that you think will are related to the price of a house. In the notebook you you need to explain the features you engineer and your thought process behind why you created them.  

- **Statistical Tests:** Your notebook must show **at least 3 statistical tests** that you preformed on your data set. Think of these as being part of your EDA process; for example, if you think houses with a view cost more than those without a view, then perform a two-sample T-test. These willpreliminary evidence that a feature will be important in your model.  

- **Linear Regression Model:** One of the benefits of a linear regression model is that you can **interpret the coefficients** of the model **to derive insights**. For example, which feature has the biggest impact on the price of the house? Was there a feature that you thought would be significant but was not once other features were considered?  Models for inference are typically simpler so they are more straight forward to interpret, so you probably won't include all of your features in this model. 

*Reminder -  **Check Model Assumptions:** While you will have one final model from which you will draw insights, you will probably build multiple models to get there. Your first modeling attempt will probably violated one of the 4 assumptions of a linear regression model, and invesitgating those violations can help you to make a better model. For example, your errors might not be homoscedastic. This could mean that a non-linear transformation of the target variable could improve your model. It is not always possible to perfectly meet those assumptions, so that should not be your goal but, you must make at least one attemmpt to improve your model in order to meet the assumptions.* 

## Holdout predictions

You will go through a process to develop a model using `kc_house_data_train.csv`. The model that you develop for the predictions should be different from the one you used to make inferences. For your predictive model, you want it to be as accurate as possible and won't worry about making inferences from it. Therefore your model can be more complex. 

Once you develop your most accurate model using the `kc_house_data_train.csv`, you will use that model/process to predict on the `kc_house_data_holdout_features.csv`. You will submit those predictions as a `.csv` file to the instructional staff and we will score the submitted predictions using the RMSE of those predictions.

***Important note #1***: If you create a new feature with your training data, you will need to do the same thing with the test data before using the model to predict on the holdout data.  

***Important note #2***: While we will score and rank each submission, your class rank will **not** have any direct impact on passing Phase 2. *The goal is to make sure you can actually produce predictions*.


## GitHub Repository

A GitHub repo is a good way to keep track of your work, but also to display the work you did to future employers. Your GitHub should contain the following:

- A `README.md` that briefly describes the project and the files within the repo.
- Your cleaned and annotated notebooks showing your work.
- A folder with all of your 'working' notebooks where you played around with your data and the modeling process.

## Data Set Information

This data set contains information about houses that were sold in the Seattle area during the last decade. Below is a description of the column names, to help you understand what the data represents. As with most real world data sets, the column names are not perfectly described, so you'll have to do some research or use your best judgment if you have questions relating to what the data means. 

Like every data set, there are some irregularities and quirks. Trust me, there wasn't a house sold with 33 bedrooms, even though the data says there was. *You have to decide how you want to handle that example*. Also, some houses were sold more than once within the time frame of this dataset. Think about how that can be useful information in predicting the selling price.

As you go through this modeling process, think about what determines how much someone will pay for a house.  For example, the larger the house is, the more people will pay for it. If you understand why certain houses cost more than others and represent that in your model, it will be a more accurate model.  

Have fun!

# Column Names and descriptions for Kings County Data Set
* **id** - unique ID for a house
* **date** - Date day house was sold
* **price** - Price is prediction target
* **bedrooms** - Number of bedrooms
* **bathrooms** - Number of bathrooms
* **sqft_living** - square footage of the home
* **sqft_lot** - square footage of the lot
* **floors** - Total floors (levels) in house
* **waterfront** - Whether house has a view to a waterfront
* **view** - Number of times house has been viewed
* **condition** - How good the condition is (overall)
* **grade** - overall grade given to the housing unit, based on King County grading system
* **sqft_above** - square footage of house (apart from basement)
* **sqft_basement** - square footage of the basement
* **yr_built** - Year when house was built
* **yr_renovated** - Year when house was renovated
* **zipcode** - zip code in which house is located
* **lat** - Latitude coordinate
* **long** - Longitude coordinate
* **sqft_living15** - The square footage of interior housing living space for the nearest 15 neighbors
* **sqft_lot15** - The square footage of the land lots of the nearest 15 neighbors
