# ML Powered Taxi Fare Prediction using Docker

Download the New York city map data 'new-york-latest.osm.pbf' from [Geofabrik](https://download.geofabrik.de/north-america/us/new-york.html)

This project implements an ML-based taxi fare prediction system using LightGBM, optimized for accurate fare estimation based on historical data. Docker is used to automate the extraction and processing of travel distance and time from map images, which are then used as inputs for the prediction model.

### Key Features

- **Model Optimization:** Evaluated multiple models, selecting LightGBM for its superior performance.
- **High Prediction Accuracy:** Achieved R² = 83.9%, with optimized error metrics (MAE: 0.01252, RMSE: 0.02279).
- **Automated Data Extraction:** Used Docker to extract and process travel distance and time from map images.

### Model Comparison

To determine the best-performing model for taxi fare prediction, various regression techniques were tested. Below are the results:

| Model                           | MAE    | RMSE   | R²      |
|---------------------------------|--------|--------|---------|
| **Linear Regression**            | 0.01287 | 0.02345 | 0.82992 |
| **2nd Order Polynomial Regression** | 0.01278 | 0.02321 | 0.83339 |
| **3rd Order Polynomial Regression** | 0.01279 | 0.02307 | 0.83540 |
| **XGBoost**                      | 0.01253 | 0.02318 | 0.83374 |
| **LightGBM (Best Model)**         | 0.01252 | 0.02279 | **0.83931** |

### Why LightGBM?
- Best overall performance, achieving the highest R² (0.83931) and lowest error metrics.
- Faster training and better generalization compared to polynomial regression.
- Handles large datasets efficiently, making it ideal for real-time predictions.

This project showcases the integration of machine learning and Docker to streamline taxi fare prediction. By testing multiple models, LightGBM was identified as the best-performing approach, achieving high accuracy and efficiency. The automated data extraction pipeline using Docker enhances preprocessing, ensuring accurate input features for prediction.
