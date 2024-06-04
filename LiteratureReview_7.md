## Unraveling intra-urban freight parking patterns: A data-driven geospatial study of shared logistics sector in Hong Kong 

***Citation:***
Zidong Yu, Haotian Wang, Xintao Liu, Unraveling intra-urban freight parking patterns: A data-driven geospatial study of shared logistics sector in Hong Kong, Journal of Transport Geography,
Volume 117, 2024, 103900, ISSN 0966-6923, https://doi.org/10.1016/j.jtrangeo.2024.103900. (https://www.sciencedirect.com/science/article/pii/S0966692324001091)

***Summary:***

**Data Collection**
-  GPS Trajectory Data: The study used GPS trajectory data from GoGoX, recording the movements of registered vehicles from July 1 to August 1, 2017.
    - This data is used to identify parking events by detecting periods where vehicles remain stationary for a specified duration.
    
  ![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/dcdebb4c-5279-4515-8f7c-e546af75e3e6)

- POIs (Points of Interest) Data: Collected 319,799 Points of Interest (POIs) from the AutoNavi API, reclassified into eight categories to represent various urban functions.
  - This data helps to understand the relationship between parking behaviors and urban functions.
  - The density of POIs in different categories is used as features in the Random Forest regression analysis to determine their impact on parking patterns.

    ![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/1f9361a7-2758-4ba5-8076-d4926a83690e)

- NSR (No Stopping Restriction) Data and Traffic Signs: Integrated No Stopping Restriction (NSR) data and traffic signs to identify roads where parking is prohibited.
  - This data is used to identify and analyze illegal parking events.
    
    ![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/08fd7248-0ec5-4feb-aeff-10c0e7450e19)

**Data Preprocessing**

1. GPS data preprocessing
     Parking Event Detection: Identified potential parking events by looking for continuous time records where vehicles remained in the same location. Only instances with durations between 3 minutes and 24 hours were considered valid parking events.

2. POIs Data Preprocessing
     Density Calculation: Calculated the density of each POI category in different regions to understand their impact on parking behaviors.

3. Integration of NSR and Traffic Signs
     Mapping Prohibitions: Mapped No Stopping Restriction (NSR) zones and traffic signs indicating parking prohibitions to the GPS data to identify illegal parking events.

**Feature Engineering**

1. Parking Event Features:

- Duration: Calculated the duration of each parking event.
  Example: If a vehicle remains parked at the same spot from 08:00 to 08:30, the duration of this parking event is 30 minutes.
  
- Frequency: Computed the frequency of parking events in different regions.
  Example: If a region has 100 parking events recorded in one week, the weekly frequency of parking events for that region is 100.
  
- Illegal Parking Index: Developed an index combining the number of illegal parking incidents and their average duration to evaluate the intensity of illegal parking.
    Example: If a road segment has 10 illegal parking incidents, each with an average duration of 20 minutes, the Illegal Parking Index for that segment is 10×20=200.

2. Spatial Features:

- Rank-Size Distribution: Used to exhibit the spatial heterogeneity of parking events.
  Example: If the top-ranked region has 1000 parking events and the second-ranked has 800, the rank-size distribution helps visualize the drop-off in parking events as rank increases.
  
- Log-Odds Ratio: Calculated to compare the relative differences in parking events between weekdays and weekends, as well as between short-term and long-term parking.

3. Urban Function Features:

- POI Density: Computed the density of various POI categories to serve as indicators of urban functions.
  Example: If a region has 50 dining POIs in an area of 2 km², the density of dining POIs is 50/2 =25 POIs per km².

- Random Forest Regression Features: Utilized POI densities and other spatial attributes as input features for the Random Forest regression model to explore correlations with parking behaviors.

**Methods Used**

1. Rank-Size Distribution and Log-Odds Ratio:

    - Analyzed the spatial concentration and temporal heterogeneity of parking events using these statistical methods.

2. Random Forest Regression:

    - Employed to model the relationship between parking behaviors and urban functions. This method helps to capture nonlinear relationships and assess the importance of different features.

3. SHapley Additive exPlanations (SHAP):

    - Used to interpret the Random Forest model results. SHAP values indicate the contribution of each feature to the model’s predictions, providing insights into which urban functions most influence parking behaviors.

**Results and Visualization**

- Spatial and Temporal Patterns: Mapped and analyzed the distribution of parking events, highlighting high-demand areas and illegal parking hotspots.
- Impact Analysis: Assessed how different urban functions (e.g., industrial, dining) affect parking behaviors using Random Forest and SHAP.

