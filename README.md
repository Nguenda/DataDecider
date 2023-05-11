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
![]([image.jpg](https://github.com/Nguenda/DataDecider/blob/main/Screen%20Shot%202023-05-10%20at%208.04.32%20PM.png))
![]([image.jpg](https://github.com/Nguenda/DataDecider/blob/main/Screen%20Shot%202023-05-10%20at%208.04.45%20PM.png))


Highlight key insights gained from the exploratory analysis, such as docking setup, weather impact, and station-specific patterns.


## Results
![Alt Text](image.jpg)
![Alt Text](image.jpg)
![Alt Text](image.jpg)
![Alt Text](image.jpg)


Summarize the results of your analysis, including any metrics or visualizations that demonstrate the performance of your model.

## Contributors
List the names and roles of each team member, as well as their contributions to the project.

## Collaboration
Describe how you collaborated on the project, including how you communicated, divided tasks, and resolved conflicts.


## Model Performance Evaluation
Present the performance evaluation of different models, including MSE comparison and other relevant metrics.

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

