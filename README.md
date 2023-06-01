# DataDecider
Highlights the role of data-driven decision-making in ML projects.

This portfolio provides the following content for the project:

1. Four CSV files that were used as datasets to build the models and perform the analysis.
2. [Team Final Report](https://github.com/Nguenda/DataDecider/blob/05e61f5b5a12ff57103f8e57ad90662d6a8823c1/Machine%20learning%201_project_BikeShare.pdf): This PDF file is a detailed report on the project, containing text and images to illustrate the content.
3. [CapitalBikeshare_21st_&_I_St_NW.ipynb](https://github.com/Nguenda/DataDecider/blob/main/CapitalBikeshare_21st_%26_I_St_NW.ipynb): This file is the code file for the project related to 21st_&_I_St_NW. Users can view and run the code through Jupyter Notebook.
4. [CapitalBikeshare_21st_St_&_Pennsylvania_Ave_NW.ipynb](https://github.com/Nguenda/DataDecider/blob/main/CapitalBikeshare_21st_St_%26_Pennsylvania_Ave_NW.ipynb): This file is the code file for the project related to 21st_St_&_Pennsylvania. Users can view and run the code through Jupyter Notebook.
5. The portfolio includes images that were used to visually illustrate and enhance the explanatory analysis conducted in the project.


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
LASSO model was chosen as the preferred model. Our analysis revealed that LASSO outperformed the other models when evaluated by the Mean Squared Error(MSE) as shown in table 1 above. 3 out 4 MSEs from the LASSO model were found to be the lowest of the 5 models which were used and yielded the best performance on the validation set. Furthermore, LASSO had the least number of features after hyper parameter tuning, which reduces the cost of running the model. It’s interpretability was considered to be 
more difficult than linear regression but still understandable.

## Predictive Modeling
Provide the predicted number of bikes for pick-up and drop-off using the selected model.
![](https://github.com/Nguenda/DataDecider/blob/9fb3e71d58562282635da526758561d1a869fab2/Screen%20Shot%202023-05-10%20at%208.37.55%20PM.png)

After analyzing a set of features from the test dataset, the Lasso Regression model predicted the number of 
pickups and drop-offs for the two stations, as displayed in Table 2.

## Decision-Making
Based on the model's predictions, the decision-making process for bike and dock allocation involves monitoring pickups and drop-offs at the stations. Surplus bikes at the '21st & I St NW' station and the need for additional docks at '21st St & Pennsylvania Ave NW' station are identified. Recommendations include automated allocation based on real-time predictions, regular model updates, planning maintenance during low-demand periods, major rebalancing during busy months, evaluating station performance, and using app data for accurate demand prediction.

## Insights and Limitations
The insights gained from the project include the effectiveness of the chosen model in predicting bike demand, the significant impact of weather conditions on demand, and the potential for optimizing resource allocation based on the model's predictions.

However, there are several limitations and areas for further improvement. The model's performance is dependent on the quality and quantity of available data, and the analysis was limited to daily pickups, which may not capture the full picture of bikeshare operations throughout the day. Unforeseen events and external factors are not accounted for in the model, which may affect bike demand. Regular retraining of the model may be necessary to adapt to changing patterns and trends.

## Conclusion
This study demonstrates the potential of machine learning models in optimizing Bikeshare's operations by 
predicting bike demand at specific stations. After comparing the performance of various machine learning 
models, we found that Lasso Regression yielded the most accurate and reliable predictions for bike demand 
at the two stations: '21st & I St NW' and '21st St & Pennsylvania Ave NW'. In this report, we outlined some 
dynamic and impactful decision recommendations based on the insights gained from the Lasso Regression 
model to optimize bike and dock allocation for Bikeshare's operations. By leveraging data and the selected 
model, Bikeshare can make data-driven decisions to allocate resources more efficiently and improve its 
overall service quality

## Contributors
Team members: **Agnes Nguenda, Emmanuel Asong, Nigel Nyajeka, Meakin Marange**

As a team of MSBA students, each member brought their unique skills and knowledge to the project. They worked collaboratively to tackle various aspects of the project, including project management, data preprocessing, model development, research, and data analysis. The team's combined efforts resulted in the successful completion of the project and the achievement of its objectives.

## Collaboration
During the project, we fostered a collaborative environment and utilized effective communication channels to ensure smooth collaboration. We primarily communicated through regular team meetings, both in-person and online, where we discussed project progress, shared updates, and addressed any issues or concerns. Additionally, we maintained open communication channels through instant messaging platforms and email for day-to-day interactions.

To divide tasks, we initially assessed each team member's strengths, interests, and areas of expertise. Based on this assessment, we allocated tasks accordingly, considering the individual's skills and workload balance. We aimed for a fair distribution of responsibilities and ensured that each team member had the opportunity to contribute and develop their skills.

In terms of conflict resolution, we encouraged open and respectful discussions when disagreements arose. We actively listened to each other's perspectives, sought common ground, and worked towards finding mutually agreeable solutions. In case of significant conflicts, we sought the guidance of our project advisor or faculty member to help mediate and provide guidance for resolution.

Overall, our collaborative approach, effective communication, task allocation, and conflict resolution strategies allowed us to work efficiently as a team, leverage our collective strengths, and successfully complete the project.






