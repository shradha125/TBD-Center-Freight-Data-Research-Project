## Using Machine Learning to Predict Freight Vehicles’ Demand for Loading Zones in Urban Environments

***Citation:*** Ludowieg, A. R., Sanchez-Diaz, I., & Kalahasthi, L. K. (2023). Using Machine Learning to Predict Freight Vehicles’ Demand for Loading Zones in Urban Environments. Transportation Research Record, 2677(1), 829-842. https://doi-org.ccny-proxy1.libr.ccny.cuny.edu/10.1177/03611981221101893

***Summary***:

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
        For instance, if we are predicting the demand at 10:00 AM, short-term lags might include the number of vehicles parked at 9:55 AM, 9:56 AM, 9:57 AM, 9:58 AM, and 9:59 AM.
    -   Long-term Lags: Lagged values for one to four weeks to account for weekly and monthly variations, such as those caused by holidays or other special dates.
        For example, the number of vehicles parked at the same time on previous days or weeks (e.g., 10:00 AM one day ago, one week ago, etc.).
-  **Target Variable:** The target variable is a continuous variable representing the time (in seconds) until no spots are available. This is calculated for different prediction horizons: 1 minute, 5 minutes, 15 minutes, and 60 minutes into the future.
      Example: Current Time: 10:00 AM, prediction Horizon: 15 minutes (until 10:15 AM). Time until no spots are available: 810 seconds (if the last spot is occupied at 10:13:30 AM)


***Modeling***
- **Baseline Model: Linear regression**. Performed well for short-term predictions (e.g., 1 minute ahead) where the time series data exhibited more linear patterns.
- **Neural Networks:** To capture more complex patterns in the data.
     - Multilayer Perceptron (MLP): Captured complex non-linear relationships in the data.
     - Long Short-Term Memory (LSTM): Particularly used for longer prediction horizons (e.g., 15 minutes and 60 minutes ahead).
     - Combination Models: A combination of LSTM and MLP layers is also tested to leverage both short-term and long-term temporal patterns.
     - Probabilistic Neural Networks: Effective in capturing the variability in loading zone demand.

***Evaluation Matrics***
Mean Absolute Error (MAE), Root Mean Square Error (RMSE).

#### Given Data
Timestamp,Time of Day,Day of Week,Date,Weather,Traffic Condition,Special Event,
#### Calculated Data
Occupancy 2 mins ago,Occupancy 3 mins ago,Occupancy 4 mins ago,Occupancy 5 mins ago,Occupancy same time yesterday,Occupancy same time last week,Current Occupancy,Avg Occupancy Last 15 mins,Avg Occupancy Last Hour,Occupancy Rate (last 15 mins),
#### Target Variable (Calculated)
Target Variable (Seconds until no spots)



## Modeling Truck Parking Demand at Commercial and Industrial Establishments

***Citation:*** Guerrero, S. E., Pulikanti, S., Wieghart, B., Bryan, J. G., & Strow, T. (2023). Modeling Truck Parking Demand at Commercial and Industrial Establishments. Transportation Research Record, 2677(1), 1157-1168. https://doi.org/10.1177/03611981221103597

***Summary:***

Study aims to address the mismatch between truck parking needs and the availability of spaces, which often results in unsafe, disruptive, and illegal parking practices. The research combines GPS data with land use and employment data to quantify parking requirements and improve land use and development decision-making.

***Data Collection***
- ATRI data from Phoenix, AZ.
- **GPS Data** (Latitude, longitude, timestamp, speed, truck ID): Capture the location, movement, and unique identification of trucks, helping to identify stops and parking events.
- **Traffic Data** (Average speed, traffic volume, number of lanes on adjacent roadways): Provides contextual information on traffic conditions that can affect parking behavior.
- **Rest Area Characteristics**: Details about the facilities available at rest areas which can influence where truck drivers choose to park.
- **Weather Data** (Hourly precipitation): Weather conditions can impact driving and parking patterns.
- **Land Use Data** (land use types (residential, industrial, commercial, etc.)): Helps in understanding the type of area where parking occurs and its suitability for truck parking.

***Data Preprocessing***
1. **Cleaning GPS Data:**
    - Stop Identification: Defined by truck speed (≤2 mph) and distance criteria (DX ≤ 40 ft and DXmax ≤ 100 ft). A duration longer than 10 minutes ensures that the identified stops are meaningful in terms of parking behavior.
    - Filtering Errors: Removing GPS points with unrealistic locations due to signal bouncing or loss.
      
2. **Combining Datasets:**
   - Integrate GPS stops data with land use, traffic, and weather data to create a comprehensive dataset for analysis.
     
3. **Handling Missing Values**
   - Imputation

***Feature Engineering***

1. **Creating New Features:**
    - Time-Based Features: Time of day, day of the week, which can influence parking patterns.
    - Spatial Features: Distance to nearest rest area, proximity to urban centers.

2. **Interaction Terms:**
    - Capture combined effects of multiple factors, such as interaction between traffic volume and weather conditions on parking demand.

3. **Parking Metrics:**
    - Number of Stops per Weekday: Total parking events per establishment.
    - Cumulative Stop Duration: Total time trucks are parked per establishment.
    - Peak Occupancy: Maximum number of trucks parked at the same time.

***Modeling***
- Statistical Models used: Linear Models, Negative Binomial Models, and Log-Linear Models.

***Evaluation***
- R-Squared (R²)
- Log-Likelihood
- Bayesian Information Criterion (BIC)

Study confirms the initial hypothesis of a mismatch, providing specific insights into where parking demand is highest and thus where interventions are most needed.


## Improving delivery conditions by dynamically managing the urban parking system: Parking availability prediction

***Citation:*** 
H. Errousso, J. el Ouadi, S. Benhadou, H. Medromi and N. Malhene, "Improving delivery conditions by dynamically managing the urban parking system: Parking availability prediction," 2020 IEEE 13th International Colloquium of Logistics and Supply Chain Management (LOGISTIQUA), Fez, Morocco, 2020, pp. 1-6, doi: 10.1109/LOGISTIQUA49782.2020.9353890. keywords: {Supply chain management;Roads;Urban areas;Switches;Tools;Real-time systems;Task analysis;freight parking;parking availability;prediction;regression;ensemble methods},

***Summary:***

Study presents an approach to managing urban parking systems by predicting parking availability dynamically. The aim is to improve delivery conditions, reduce urban traffic, and enhance living conditions in cities.

The solution consists of two main modules:
- Prediction Module: Forecasts parking space availability using historical data.
- Assignment Module: Allocates parking spaces based on predictions and real-time conditions.
    - Dynamically allocate parking spaces based on real-time conditions and forecasted availability. Adjust the designation of parking spaces (e.g., from general parking to delivery bays) as needed.    

**Data Collection:**
- Data Source: The study uses parking data from the City of Melbourne, Australia, which includes information from 4300 sensors across 303 avenue sections within 35 areas.
- Attributes: Data includes entry and exit times, park event length, zone and street names, and device IDs.
- https://data.melbourne.vic.gov.au/explore/dataset/on-street-parking-bay-sensors/table/

These datasets are crucial for accurately predicting parking availability and dynamically managing parking space allocation to improve urban delivery

**Data Preprocessing:**
- Remove Inconsistencies: Eliminate records with very brief or negative parking durations and unnecessary columns.
- Assign Unique Identifiers: Assign unique integers to area names.
- Time Segmentation: Model the timeline into 15-minute intervals, assigning an integer to each interval.
- Fill Missing Data: Fill in missing entry or exit times using data from previous periods or similar times on previous days.
- Calculate Metrics: Determine the parking capacity, number of incoming and outgoing vehicles, and the number of available spaces.

**Machine Learning Models:**

The study explores several ensemble regression methods to predict parking availability:
- Bagging Methods: Random Forest, Bagging Regressor, Extra Trees.
- Boosting Methods: Adaboost, XGBoost, Gradient Boosting Machine (GBM), LightGBM, CatBoost.
- Stacking Models: Various combinations of bagging and boosting methods with meta-learners like Decision Tree, Random Forest, and LightGBM.

**Evaluation:**

The models are evaluated using:
- Coefficient of Determination (R²)
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

**Results:**
- Performance Comparison: LightGBM outperforms other boosting methods, while Random Forest is the best among bagging methods. Stacking methods show that the choice of meta-learner significantly impacts prediction accuracy.
- Efficiency: Stacking does not significantly enhance predictive precision compared to using the best individual models, but it can help balance accuracy and computational cost.

Others:

https://ieeexplore-ieee-org.ccny-proxy1.libr.ccny.cuny.edu/stamp/stamp.jsp?tp=&arnumber=9582619

  
