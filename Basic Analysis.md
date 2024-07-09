## Task 1: Truck Volume Analysis - To evaluate the traffic volume

**Metrics: Difference in Truck Volume from Non-peak to Peak Hours**
- Compared the Segment ID's with open source NYC DCP's open source data to get the latest active Segment ID's.
- Created a new dataframe containing the data for only those latest Segment ID's and calculated the difference in truck volume for Non-peak to Peak hours per time period. (WD Evening, WD Mid-Day, WD Morning, WE Saturday)
- Unique Segment ID's after filtering = 11118.
- Plotted a Stacked Bar Graph to visualize the difference in truck volume per time period for first 20 Segments.
- Positive values indicate the volume of trucks at the Peak hours whereas the negative values indicate the volume of trucks at the Off-Peak hours.
- Out of the sample of 20 segments, the SegmentID 9008369 which corresponds to Street 'SEDGWICK AVENUE' has the count of around 1000 trucks using the road segment on Weekday Peak morning hours and around 500 trucks using the road segment on Weekday Midday Peak hours. It indicates that this segment experiences heavy truck traffic during that time.
- Comparing usage with other segments where truck traffic is lower provides a context for understanding the relative importance and demand for "SEDGWICK AVENUE" among other road segments.
- This information highlights "SEDGWICK AVENUE" as a significant thoroughfare for truck transportation, experiencing notable traffic volumes during peak hours, which is crucial for transportation planning, infrastructure management, and understanding local traffic dynamics.

![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/620c7861-d60a-44d9-9a60-2cbd5a6ef121)


**Metrics: Volume of Trucks by Time Categories**
- Created a grouped bar chart (bar1 for positive counts and bar2 for negative counts) to visualize the truck volume differences across segments and time categories.
- It calculates and visualizes how many segments have positive or negative truck volume differences, providing insights into when and where truck traffic peaks or dips relative to each time category. 
- Calculated the sum of the above displayed difference in truck volumes (WD Evening, WD Mid-Day, WD Morning, WE Saturday) grouping by SegmentID.
- Result shows the Weekday Morning counts high volume during the peak hours.

![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/2cc0b726-c966-42ed-b56f-c2dca0f89c52)


## Task 2: Truck Origin-Destination Analysis - To analyse truck trip mobility

**Metrics: Number of trucks trips origin per spatial area and time period, Number of trucks trips destination per spatial area and time period**
- Graph helps visualize the number of truck trips originating from and concluding in the top 20 sub-geographies.
- Grouped by origin and destination to get the total number of trips per origin and destination and then displayed the top 20 Origins and Destinations.
- By comparing the two plots, we can identify sub-geographies that are both major origins and destinations, suggesting areas that are both significant sources and sinks for truck traffic.
- These insights are valuable for urban planners and logistics companies to optimize routes, manage traffic congestion, and improve supply chain efficiency. Areas with high trip counts might need better infrastructure or traffic management solutions.

![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/fa804318-0203-4770-98c8-89b6b79e45c7)


- Bar plot to visualize the number of truck trips for three specific analyses (TAZ, NTA, IBZ) across different time periods (timeBin).
- Grouped by analysis and timeBin and calculated the sum of thr truck trips.
- High Truck Activity: The high volume of truck activity during the morning peak hours indicates a need for improved traffic management strategies to reduce congestion during this time.

![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/57ecb963-cc28-4fa4-b4a4-730246b4b960)


**Understand the volume of trips between different pairs of sub-geographies, making it easier to analyze traffic patterns and relationship**
- Grouped by both origin and destination to get the sum of trip counts.
- The heatmap highlights the pairs of origin and destination sub-geographies with the highest volumes of truck trips. These high-volume routes can be crucial for logistics planning and infrastructure development.
- This helps in understanding which areas are major sources and destinations of truck traffic.
- This heatmap serves as a visual representation to make informed decisions on managing and optimizing truck traffic in urban settings.

![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/a7851c54-7fb2-4149-a764-fd0be79b2a52)
