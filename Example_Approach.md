## Approach to Freight Transportation Research

To create a comprehensive approach to freight transportation research that aligns with the given policy goals, the data representation must be structured to incorporate policies, parameters, simulation, and outcome measurements. Here's a detailed plan:

#### Goals
- **Primary Goals:**
  - Make the last mile more efficient.
  - Green the last mile.
- **Specific Objectives:**
  - Reduce congestion in residential neighborhoods.
  - Increase curb space for deliveries.
  - Develop urban consolidation centers.
  - Meet freight vehicle parking demand.
  - Promote sustainable delivery methods and electrify trucks.
  - Shift mode from road to water and rail.

#### Policy Changes
- **Policy Adjustments:**
  - Retiming deliveries.
  - Adjusting truck traffic regulations.
  - Expanding curb space.
  - Implementing urban consolidation centers.
  - Regulating parking supply and demand.
  - Introducing sustainable and electric delivery vehicles.
  - Encouraging alternative transportation modes.

#### Simulation Response to Policy Changes
- **Simulation Setup:**
  - **Input Data:** Vehicle metrics, freight activity types, parking duration, parking demand, parking supply, freight trip dynamics.
  - **Policy Inputs:** Changes in regulations, curb space, consolidation centers, vehicle types, and delivery timings.
  - **Petri-net Parameters:** Variables that define the states and transitions within the Petri-net model.

- **Simulation Process:**
  1. **Initialize:** Start with current policy settings and freight data.
  2. **Policy Application:** Apply policy changes to adjust Petri-net parameters.
  3. **Run Simulation:** Generate freight movement and parking behavior over a defined period.
  4. **Stochastic Elements:** Include variability to reflect real-world conditions.

#### Measuring Outcomes/Goals from Simulation
- **Outcome Metrics:**
  - Average speed of vehicles.
  - Distribution and density of trucks.
  - Parking occupancy rates.
  - Fuel consumption and emissions.
  - Number of deliveries and trip durations.
  - Compliance with delivery and parking regulations.

- **Evaluation Process:**
  - **Data Collection:** Gather simulated data on vehicle metrics, parking dynamics, and freight trips.
  - **Performance Comparison:** Compare simulation results with target values to assess policy effectiveness.
  - **Error/Loss Calculation:** Compute discrepancies between simulated outcomes and policy goals.

#### Data Representation Needs
- **Data Elements:**
  - **Vehicle Metrics:** Type, classification, weight, engine type, load factor, number of deliveries, fuel consumption, speed.
  - **Freight Activity:** Professional activity, establishment type, commodity type.
  - **Parking Duration:** Distance to establishment, delivery and arrival times, parking behavior.
  - **Parking Demand:** Arrival rates, locations, occupancy rates, illegal parking.
  - **Parking Supply:** Space dimensions, locations, types, loading zones.
  - **Freight Trip Dynamics:** Trip origins and destinations, GPS trajectories.

### Comprehensive Approach

1. **Define Policy Goals:**
   - Determine the specific objectives for last-mile efficiency and sustainability.

2. **Identify Policy Parameters:**
   - List all adjustable parameters (e.g., delivery times, vehicle restrictions, curb space).

3. **Data Integration:**
   - Collect and integrate data from various sources (NYC DOT, AVL, ATRI) focusing on vehicle metrics, parking, and freight activities.

4. **Model Setup:**
   - Configure the Petri-net model to include all relevant parameters and data elements.
   - Define the initial state based on current policies and freight data.

5. **Simulation Execution:**
   - Apply policy changes and run the simulation to predict freight movements and parking dynamics.
   - Use stochastic elements to mimic real-world variability.

6. **Outcome Measurement:**
   - Gather simulated data and calculate performance metrics.
   - Compare against policy goals and compute error/loss.

7. **Feedback and Adjustment:**
   - Use the error/loss information to iteratively adjust policy parameters.
   - Optimize policies to achieve desired outcomes.

### Example Flow

1. **Policy Input:** "Retiming deliveries to non-peak hours and increasing curb space by 20%."
2. **Petri-net Parameters:** Adjust delivery time windows and curb space capacity in the model.
3. **Simulation:** Run the simulation to observe changes in average speed, truck distribution, and parking occupancy.
4. **Outcome Measurement:** Measure the average speed, number of deliveries, and occupancy rates.
5. **Error Calculation:** Compare with target metrics (e.g., increase in average speed by 10%, reduction in illegal parking by 15%).
6. **Adjustment:** Fine-tune delivery times and curb space allocation based on simulation results.
7. **Iterate:** Repeat the process to refine policies and achieve optimal results.

This structured approach ensures that policy changes are systematically evaluated and optimized, providing actionable insights for improving freight transportation efficiency and sustainability.




## Research Evaluation from NYC Department of Transportation’s Perspective

#### Goals and Objectives Alignment

**NYC DOT’s Policy Goals:**
- **Make the Last Mile More Efficient:** Improve delivery times, reduce congestion, optimize curb space usage, and enhance overall freight network efficiency.
- **Green the Last Mile:** Promote sustainable delivery methods, reduce emissions by electrifying trucks, and shift freight movement from road to more environmentally friendly modes like water and rail.

**Research Goals:**
- Assess and optimize policy impacts on freight transportation.
- Model and simulate freight dynamics and parking behavior.
- Measure outcomes to inform policy decisions.

### Benefits to NYC DOT

1. **Informed Decision-Making:**
   - **Data-Driven Insights:** Provides empirical evidence on how policy changes affect freight transportation, helping NYC DOT make informed decisions.
   - **Predictive Modeling:** Simulates various scenarios, predicting outcomes of policy implementations before they are enacted.

2. **Efficiency Improvements:**
   - **Last Mile Optimization:** Helps identify the most effective strategies for reducing congestion and improving delivery efficiency.
   - **Resource Allocation:** Optimizes curb space and parking resources, ensuring better utilization and reducing illegal parking incidents.

3. **Environmental Impact:**
   - **Sustainability:** Supports policies aimed at reducing greenhouse gas emissions by evaluating the impact of electrification and mode shifts.
   - **Green Initiatives:** Measures the effectiveness of sustainable delivery methods, guiding the transition to greener freight systems.

4. **Policy Customization:**
   - **Tailored Solutions:** Customizes policies to specific areas and times, addressing unique challenges of different neighborhoods and business districts.
   - **Dynamic Adjustments:** Allows for iterative policy adjustments based on real-time data and simulation outcomes.

5. **Comprehensive Analysis:**
   - **Holistic Approach:** Considers various metrics such as vehicle speed, fuel consumption, parking occupancy, and trip duration.
   - **Interconnected Metrics:** Analyzes the complexity and interconnectivity of freight data elements, providing a comprehensive understanding of the freight ecosystem.

### Key Components of the Research

1. **Policy Simulation Model:**
   - **Petri-net Parameters:** Adjusts parameters to simulate different policy scenarios.
   - **Stochastic Elements:** Incorporates randomness to reflect real-world variability, ensuring robust and realistic simulations.

2. **Outcome Measurement:**
   - **Performance Metrics:** Evaluates key performance indicators such as average speed, distribution of trucks, parking occupancy rates, and emissions.
   - **Error/Loss Calculation:** Measures discrepancies between simulated outcomes and policy goals, providing feedback for policy refinement.

3. **Iterative Process:**
   - **Feedback Loop:** Continuously refines policies based on simulation results and outcome measurements, ensuring policies are effectively meeting goals.
   - **Optimization:** Identifies optimal policy settings for maximum efficiency and sustainability benefits.

### Practical Applications

1. **Retiming Deliveries:**
   - Simulates the impact of off-peak deliveries on traffic congestion and delivery efficiency.
   - Measures how changing delivery windows affects average speed and parking demand.

2. **Curb Space Management:**
   - Assesses the effects of increasing curb space for deliveries on parking occupancy and illegal parking rates.
   - Evaluates the balance between parking supply and demand under different policy scenarios.

3. **Sustainable Delivery Methods:**
   - Models the adoption of electric trucks and other sustainable methods.
   - Measures the reduction in fuel consumption and emissions.

4. **Urban Consolidation Centers:**
   - Simulates the establishment of consolidation centers and their impact on freight efficiency and traffic patterns.
   - Evaluates the benefits of reducing the number of individual delivery trips.

### Conclusion

From NYC DOT’s perspective, this research offers substantial value by providing a systematic and data-driven approach to policy evaluation and optimization. By aligning with NYC DOT’s policy goals of efficiency and sustainability, the research supports informed decision-making, resource optimization, and environmental stewardship. The iterative simulation process ensures that policies can be continuously refined to adapt to changing conditions and emerging challenges, ultimately contributing to a more efficient and sustainable urban freight system.

##
To achieve the goals described by Professor Grossberg using the provided datasets, follow these steps to determine which dataset aligns best with your research objectives. Each dataset offers unique insights, so understanding their attributes and limitations will help in making an informed choice.

### Steps to Achieve Research Goals

1. **Identify Key Metrics and Objectives:**
   - Determine the primary metrics you want to measure, such as average speed, distribution of trucks, parking occupancy, and emissions.
   - Identify the policy impacts you aim to simulate (e.g., retiming deliveries, reducing truck traffic).

2. **Evaluate Datasets Based on Research Needs:**
   - Analyze each dataset's metrics, geographical and temporal precision, vehicle type, dataset size, accuracy, and gaps.
   - Determine which dataset provides the most relevant information for your objectives.

3. **Data Preparation:**
   - Clean and preprocess the data to handle missing values, inaccuracies, and ensure temporal and spatial alignment.
   - Transform data into the required representation (e.g., TAZ-level data for spatial analysis).

4. **Model Selection and Simulation:**
   - Choose an appropriate model based on data representation and research goals (e.g., Petri-Net, Neural Network, GAN, or Diffusion Model).
   - Implement and run simulations to generate outputs.

5. **Output Measurement and Loss Calculation:**
   - Measure the outputs from simulations and compare them with target values.
   - Calculate errors/losses to assess the accuracy of the simulations.

6. **Policy Adjustment and Iteration:**
   - Adjust policy parameters based on error/loss analysis.
   - Re-simulate with updated parameters and iterate until optimal results are achieved.


## Dataset Evaluation

#### **Dataset A: Truck Volume and Speed**
- **Metrics:** Mean Truck Speed, Truck Volume
- **Geographical Area:** NYC
- **Temporal Precision:** Peak and Off-peak periods in weekdays vs. weekend
- **Spatial Precision:** Roadway Segment (25 feet)
- **Vehicle Type and Dataset Size:** Semi-trailers, private data purchased by NYC DOT from ATRI
- **Accuracy and Gaps:** Lack of off-peak hour granularity, missing data for certain periods
- **Performance Metrics and Applicable Models:** Speed infraction rate, truck traffic flow analysis, impact on last mile operations
- **Interpretation for Policy-Makers:** Truck speed regulation, roadway network optimization

#### **Dataset B.1: Truck Trip Origin and Destination**
- **Metrics:** Truck Origin Number
- **Geographical Area:** NYC
- **Temporal Precision:** Day
- **Spatial Precision:** TAZ, IBZ, NTA
- **Accuracy and Gaps:** Lack of off-peak temporal granularity, low spatial-level precision
- **Performance Metrics and Applicable Models:** Freight trip generation, parking metrics (arrival rate at TAZ level)
- **Interpretation for Policy-Makers:** Hot spots of truck trip generations, urban consolidation center location, evaluation of parking management strategies

#### **Dataset B.2: Matrix of Truck Trip Origin and Destination Combinations**
- **Metrics:** Number of Trucks for Each Origin and Destination Combination
- **Geographical Area:** NYC, some NJ counties, catchment zones
- **Temporal Precision:** Peak and off-peak periods in weekdays vs. weekend
- **Spatial Precision:** TAZ, IBZ, NTA in NYC, municipalities in surrounding counties, catchment zones
- **Accuracy and Gaps:** Heterogeneous level of moderate spatial precision, missing data for certain origin-destination combinations
- **Performance Metrics and Applicable Models:** Freight trip generation, parking metrics (arrival rate)
- **Interpretation for Policy-Makers:** Truck traffic flow regulations, parking demand evaluation and prediction, evaluation of parking management strategies

#### **Dataset C: Truck Parking Duration**
- **Metrics:** Truck Parking Duration (average, median, maximum, minimum)
- **Geographical Area:** NYC
- **Temporal Precision:** Second
- **Spatial Precision:** TAZ
- **Accuracy and Gaps:** Missing data for certain TAZ, dwell time only is captured
- **Performance Metrics and Applicable Models:** Parking metrics (parking duration)
- **Interpretation for Policy-Makers:** Curbside management, parking demand evaluation and prediction, evaluation of parking management strategies

#### **Dataset D: GPS Data**
- **Metrics:** Truck Location, Instantaneous Truck Speed
- **Geographical Area:** NYC (service and industrial zones)
- **Temporal Precision:** Second
- **Spatial Precision:** GPS coordinates (latitude-longitude pairs, 50 feet)
- **Vehicle Type and Dataset Size:** 500 hybrid diesel and compressed natural gas trucks, AVL technology-equipped
- **Accuracy and Gaps:** Temporally and spatially very precise, heterogeneous granularity in temporal data distribution, some GPS inaccuracies
- **Performance Metrics and Applicable Models:** Freight trip generation, illegal driver behavior, parking metrics (number of stops, arrival time/rate, occupancy rate, illegal parking rate)
- **Interpretation for Policy-Makers:** Truck traffic flow regulations, roadway network optimization, curbside management, parking demand evaluation and prediction

### Dataset Alignment with Research Goals

**Dataset D: GPS Data** aligns the most with your research goals due to:
- High temporal and spatial precision, which is crucial for accurate simulations.
- Detailed metrics on truck location, speed, trip trajectories, and parking behavior.
- Applicability to multiple performance metrics and models, allowing for comprehensive analysis and simulation.

### Achieving the Goal

1. **Data Preparation:**
   - Clean and preprocess Dataset D for missing values and GPS inaccuracies.
   - Aggregate data into the required format (e.g., TAZ-level).

2. **Model Selection:**
   - Implement a Neural Network Model or Petri-Net Model for high temporal and spatial precision.
   - Ensure the model can simulate truck movements, speed, parking, and policy impacts.

3. **Simulation Execution:**
   - Run simulations using the prepared data and selected model.
   - Implement policy changes and observe their effects on outputs.

4. **Output Measurement and Loss Calculation:**
   - Measure outputs such as average speed, truck distribution, parking occupancy, and emissions.
   - Calculate errors/losses by comparing simulated outputs with targets.

5. **Policy Adjustment and Iteration:**
   - Adjust policy parameters based on the error/loss analysis.
   - Re-simulate with updated parameters and iterate until optimal results are achieved.

By following these steps and utilizing Dataset D, you can achieve the goals outlined for your research while ensuring accurate and meaningful policy simulations.