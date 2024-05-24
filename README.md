### Hyperlocal Air Quality Prediction in Dublin

#### Project Overview
This project aims to provide hyperlocal air quality predictions (PM2.5 pollution levels) in Dublin using machine learning models. Accurate, localized air quality data is crucial for informing health, environmental, and urban planning decisions. 

#### Authors
- **Giulia Maria Petrilli** (g.petrilli@students.hertie-school.org)
- **Killian Conyngham** (k.conyngham@students.hertie-school.org)
- **Elena Dreyer** (e.dreyer@students.hertie-school.org)

#### Data Sources
1. **Air Pollution Data**: Collected by Google’s Street View car with Aclima’s mobile air sensing platform (May 2021 - August 2022).
2. **Traffic Volume Data**: Sourced from Dublin’s SCATS traffic management system.
3. **Meteorological Data**: Historical weather data from World Weather Online API.
4. **Official Measurement Stations**: Historical pollutant data from Dublin’s national air quality monitoring network via the Sonitus API.

#### Data Preparation
- **Pollution Clusters**: Measurements were aggregated within 50-meter grids around traffic intersections to manage dataset size and maintain local relevance.
- **Imputation Strategy**: Mean and KNN imputation methods were tested, with KNN performing slightly better.

#### Model Selection and Evaluation
- **Linear Models**: Ridge regression showed the best performance among linear models, but overall had a low R-squared.
- **Tree-based Models**: 
  - **Random Forest**: Performed well with a test RMSE of 5.05.
  - **XGBoost**: Achieved the best test RMSE of 4.93.
- **Neural Networks**: Despite good performance in training, neural networks were less favored due to complexity and lack of explainability.

#### Final Model Choice
The Random Forest model was chosen for its balance between performance and explainability. It had the second-lowest RMSE and allowed for easier feature importance analysis, which is crucial for understanding pollution drivers.

#### Key Findings
- Localized air quality measurements from stationary air pollution stations were highly informative for predicting PM2.5 levels.
