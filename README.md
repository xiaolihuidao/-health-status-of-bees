### EIntegrated Analysis of Beehive Health Using Weather and Inspection Data

**Hengyi Li**
**19G232**
**20231001654**

#### Abstract
This project performs an integrated exploratory and statistical analysis on the health of bee hives by leveraging both hive inspection data and weather-related data. Using a suite of Python-based data science tools, we examine potential influences of environmental conditions on hive health status. Our analysis shows notable associations between hive health and factors such as temperature fluctuations, humidity, and specific biological stressors. Results suggest that weather conditions can impact colony conditions and highlight opportunities for predictive modeling. Next steps include expanding the dataset temporally and implementing machine learning classification for risk forecasting.

#### Rationale
ee colonies are central to food security and biodiversity due to their critical role in pollination. With increasing global concern about colony collapse and bee health, this study aims to identify environmental variables that correlate with hive stress. By combining real-world meteorological and biological datasets, this research may support sustainable beekeeping practices and ecological monitoring.

#### Research Question
What environmental and biological factors most significantly affect beehive health status, and how can data science tools be used to identify patterns and predictors?

#### Data Sources
Apiary_Information.csv: Metadata about apiaries.

Hive_Information.csv: Mapping between hives and their apiaries.

HCC_Inspections.csv: Inspection data including hive health, brood, food, and stressors.

Hourly_Weather.csv: Hourly records of weather conditions.

Weather_Observations.csv: Timestamped meteorological observations.

Weather_Stations.csv: Metadata about weather stations.

#### Instruction

├── data
│    ├── Apiary_Information.csv
│    ├── Hive_Information.csv 
|    ├── HCC_Inspections.csv
|    ├── Hourly_Weather.csv
|    ├── Weather_Observations.csv
|    ├── Weather_Stations.csv
├── models
|    ├── logistic_regression_20250530_193005.pkl
|    ├── mlp_model.joblib
├── 1. course project1.ipynb
│   2. course project2.ipynb

#### Methodology
Data Integration: Datasets were joined on identifiers such as HiveID, StationID, and ObsID.

Cleaning & Preprocessing: Handled missing values, normalized inspection timestamps, and encoded categorical variables.

EDA: Used pandas, matplotlib, and seaborn for exploratory plots (e.g., boxplots, heatmaps).

Statistical Testing: Employed chi-squared tests to explore relationships between categorical inspection features (e.g., Queen status vs. Healthy).

Time-Series Matching: Matched inspection times to closest weather observations to explore short-term effects.

Data Aggregation: Calculated summary statistics for apiaries and hives over time.

#### Results
Weather Influence: Honeycombs are more likely to be "unhealthy" in extreme temperatures (too high or too low) or high humidity.

Stressors: Stressors such as lack of queen bees, presence of parasites, lack of food, etc., can significantly affect the health of the colony.

Machine Learning Model Built:

The Logistic Regression model was used to make a categorical prediction of Healthy vs Unhealthy.

The input characteristics of the model include: queen status, presence of parasites (Varroa), weather characteristics (temperature, humidity, etc.).

Evaluation indicators: Accuracy, Recall, Precision, etc., the model is robust, and the accuracy rate of the verification set reaches about 75%.

Statistical Significance: If the chi-square test p-value between Queen and Healthy is less than 0.01, it indicates a high correlation.

#### Next steps
Model Enhancement: Explore other algorithms (such as Random Forest and XGBoost) to improve model accuracy and robustness, and compare the performance of each model.

Feature Engineering: Introduce additional features like weather time series statistics, number of bee colonies, and seasonal variations by location to enhance predictive capability.

Model Deployment: Develop the predictive model into an interactive interface for real-time risk prediction of hive health.

Data Expansion: Incorporate additional data sources such as land use, pesticide application records, and air pollution to enhance model interpretability.

#### Conclusion
This integrated analysis demonstrates that bee health is influenced by both environmental and internal factors. While positive correlations were identified, future work should address data gaps and irregularities. These insights can form the basis for data-driven tools to support ecological sustainability in beekeeping.



