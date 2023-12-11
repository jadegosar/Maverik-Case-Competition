# Maverik-Case-Competition

This project was completed as a part of the Masters of Science in Business Analytics program at the University of Utah in the final Capstone course. Maverik was the sponsor of the case competition in which we were tasked with providing accurate forecasts for a new store's first year of sales in four major product categories.

## Business Problem and Project Objective

Maverik is a leading convenience and fuel store company known for providing excellent customer experience and a specialized food selection for every "Adventure's First Stop". Maverik, founded in 1928, has grown to 8000 employees and 400 locations and is expanding with their recent acquisition of the gas station company "Kum & Go". Opening 30 stores each year, Maverik faces the unique challenge of forecasting and evaluating the performance expectations for each new location over its first year. Complex sales predictors, varying seasonality influences, and market fluctuations complicate the modeling process and impact the accuracy of sales projections, leading to the deliverable being a model that produces a daily level forecast that considers seasonality. The benefit of the solution is that an accurate forecasting model will enable Maverik to improve financial planning and create more accurate initial ROI documentation.

The objective of the project was to create a time series model that can accurately forecast multiple sales categories for a new store over its first year of being open. Using store-level data provided by Maverik and features engineered to represent seasonality trends, models were built to forecast four different product categories; merchandise, food, gasoline, and diesel. Our groups solution to this business problem was to create a Lasso model with lagged sales terms included, a vector autoregression (VAR) model, and an autoregressive integrated moving averages (ARIMA) model that allowed for multivariate analysis, with all models having the ability to forecast both individual and aggregate time intervals.

## Individual Contributions

Throughout the EDA process, my contributions were performing the initial feature engineering by creating the column to track days since the store opened, the indicators for whether a given holiday was major or general, and the visualizations relating to sales trends over time. In the modeling phase, I worked on creating a lasso model with lagged terms from day 1 to 365 and implementing the ARIMA modeling approach, which included creating a workflow that started with a univariate version of an ARIMA model that was built upon to include external regressors while optimizing the ideal combination of parameters. Lastly, I created many of the data visualizations that accompanied our results and formatted them for the final presentation.

## Business Value Added
The final models were the VAR and ARIMA models that were benchmarked against the current model that Maverik uses, with each model outperforming at least one of the benchmarks. O

## Difficulties and Challenges

One of the main challenges that we faced in this project was that the dataset we were building our model on only contained one year of data on each of the 37 stores. Due to this limitation of the dataset, creating a singular ARIMA model on all the available information was not possible as each store had to be treated as a singular time series object. Even when we tried to create a standardized value for tracking time series days, we were not able to create a time series model based on all of the data available which meant we had to create an ARIMA model for each site individually. This approach came with additional limitations in that different combinations of parameters optimize the model for each store, meaning to test the accuracy of the model on the holdout set we had to apply the majority combination from the train set which was not the optimal combination of parameters for each store in the test set. The short horizon of data available for each store also made it difficult to implement traidtional time series models as many of the models, such as the ARIMA, are the most accurate at determining seasonality trends when given at least two consecutive years of data to learn from which we did not have available in the dataset.

## Takeaways


