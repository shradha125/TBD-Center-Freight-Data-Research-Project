## Using Machine Learning to Predict Freight Vehicles’ Demand for Loading Zones in Urban Environments

***Citation:*** Ludowieg, A. R., Sanchez-Diaz, I., & Kalahasthi, L. K. (2023). Using Machine Learning to Predict Freight Vehicles’ Demand for Loading Zones in Urban Environments. Transportation Research Record, 2677(1), 829-842. https://doi-org.ccny-proxy1.libr.ccny.cuny.edu/10.1177/03611981221101893

The goal was to predict the demand for loading zones at various future time horizons, helping to optimize urban freight operations. 

***Data Collection***
- The parking data used in this study was collected from the city of Vic in Spain using the Parkunload® app. This app records the use of public loading zones by freight vehicles.
- **Time-stamped Records:** Each record includes the start and end time of parking events, allowing the creation of a minute-by-minute time-series dataset.
- **Loading Zone Identifiers:** Each record is tagged with the specific loading zone where the parking event occurred.
- **Vehicle Information:** Details about the vehicles using the loading zones are included.
- The dataset covers a six-month period, focusing on the second semester of 2018.

***Data Processing***
-  **Transformation:** The raw data is transformed into a time-series format. This involves creating a temporal index that records the number of vehicles parked in each loading zone at every minute during the observation period.
-  **Occupancy Calculation:** For each timestamp, the occupancy of a loading zone is calculated as the total number of parking spots minus the number of vehicles parked.
-  **Feature Vectors:** Feature vectors are created for each loading zone. These vectors include lagged values of the target variable (the time until there are no available spots). These lags help capture both short-term and long-term temporal patterns.
    -   Short-term Lags: Lagged values of the target variable for 2 to 5 minutes to capture immediate past patterns.
    -   Long-term Lags: Lagged values for one to four weeks to account for weekly and monthly variations, such as those caused by holidays or other special dates
-  **Target Variable:** The target variable is a continuous variable representing the time (in seconds) until no spots are available. This is calculated for different prediction horizons: 1 minute, 5 minutes, 15 minutes, and 60 minutes into the future.

***Modeling***
- **Baseline Model: Linear regression**. Performed well for short-term predictions (e.g., 1 minute ahead) where the time series data exhibited more linear patterns.
- **Neural Networks:** To capture more complex patterns in the data.
     - Multilayer Perceptron (MLP): Captured complex non-linear relationships in the data.
     - Long Short-Term Memory (LSTM): Particularly used for longer prediction horizons (e.g., 15 minutes and 60 minutes ahead).
     - Combination Models: A combination of LSTM and MLP layers is also tested to leverage both short-term and long-term temporal patterns.
     - Probabilistic Neural Networks: Effective in capturing the variability in loading zone demand.

***Evaluation Matrics***
Mean Absolute Error (MAE), Root Mean Square Error (RMSE).


  
