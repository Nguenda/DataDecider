# DataDecider
Highlights the role of data-driven decision-making in ML projects.

# Machine Learning Project: BikeShare Business Case

## Overview
The problem addressed in this report is optimizing bike and dock allocations at two Bikeshare stations in Washington D.C., specifically '21st & I St NW' and '21st St & Pennsylvania Ave NW'.  Machine learning techniques were used to predict the daily demand for bikes and docks, providing strategic insights and operational recommendations. The analysis utilized historical data of bike usage at the stations and five machine learning models: Linear Regression, Lasso, KNN, Ridge Regression, and Elastic Net. The models were trained and evaluated using cross-validation and the Mean Squared Error (MSE) metric. The goal is to enhance Bikeshare's efficiency by ensuring customers can easily find bikes and available docks.

## Methodology
Historical data from January to April 2022 was collected for both Bikeshare stations, including bike pickups, drop-offs, and weather data such as temperature, humidity, and precipitation. The dataset was obtained from Bikeshare's website []([URL](https://ride.capitalbikeshare.com/system-data)). The collected datasets were cleaned and preprocessed to ensure data quality and consistency. The bike pickups and drop-offs data for both stations were merged, and the weather data was integrated. Missing values in the weather dataset were addressed by removing affected records. 
Several assumptions were made for the analysis:

- Demand and supply are aggregated on a daily basis.
- Bike pickups and drop-offs occur instantaneously and simultaneously.
- The supply of bikes is considered infinite when rebalancing is available.
- Only two locations, '21st & I St NW' and '21st St & Pennsylvania Ave NW', were considered.
- Rebalancing bikes can add a maximum number of bikes up to the available docks at a station.

.
## Exploratory Analysis
![](https://github.com/Nguenda/DataDecider/blob/92892e3fc797d4973d6ed92f93d54374d22af881/Screen%20Shot%202023-05-10%20at%208.04.32%20PM.png)
![](https://github.com/Nguenda/DataDecider/blob/92892e3fc797d4973d6ed92f93d54374d22af881/Screen%20Shot%202023-05-10%20at%208.04.45%20PM.png)


Key Insights from the Exploratory Analysis:
1. Docking Set up:
   - The realtime data from Bikeshare observed distinct differences in the available docks for both '21st and I St' and '21st St & Pennsylvania Ave'. The available docks at '21st and I St' (35 Docks) were higher compared to '21st St & Pennsylvania Ave' (19 Docks), likely due to increased demand at the station.

2. Weather Impact:
   - Temperature: We found a positive correlation between temperature and bike usage, with demand increasing as temperatures rose. However, this trend is disrupted by precipitation.
   - Precipitation: There was a negative correlation between precipitation and bike usage, indicating that rainy or snowy days typically result in lower demand for bikes.

3. Station-specific Patterns:
   - Differences in Demand: Varying levels of demand were observed between the two stations, likely attributable to differences in the surrounding areas, such as the presence of commercial buildings, residential areas, or popular destinations. Generally, '21st and I St' exhibited higher demand with more pickups and drop-offs compared to '21st St & Pennsylvania Ave'.
   - Imbalances in Pickups and Drop-offs: An imbalance between the number of pickups and drop-offs at each station was noted, indicating the need for a proactive approach to redistributing bikes and docks to ensure optimal service levels.

## Model Performance Evaluation
Present the performance evaluation of different models, including MSE comparison and other relevant metrics.
![](https://github.com/Nguenda/DataDecider/blob/fbc6c195db0bd0b861beba3143e51003207c3a80/Screen%20Shot%202023-05-10%20at%208.27.16%20PM.png)

## Model Selection
Explain why a specific model was chosen as the preferred model and highlight its strengths and interpretability.

## Predictive Modeling
Provide the predicted number of bikes for pick-up and drop-off using the selected model.

## Decision-Making
Outline the implications and recommendations for bike and dock allocation based on the model's predictions.

## Insights and Limitations
Summarize the insights gained from the project and acknowledge any limitations or areas for further improvement.

## Conclusion
Conclude the README.md file by summarizing the project's objectives, achievements, and the potential impact of the findings.

## Contributors
List the names and roles of each team member, as well as their contributions to the project.

## Collaboration
Describe how you collaborated on the project, including how you communicated, divided tasks, and resolved conflicts.


