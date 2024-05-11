**Title: Using Truck Fleet Data in Combination with Other Data Sources for Freight Modeling and Planning**

***Citation:*** Creator(s) : Pinjari, Abdul R.;Zanjani, Akbar Bakhshi;Thakur, Aayush;Irmania, Anissa;Kamali, Mohammadreza;Short, Jeffrey;Pierce, Dave;Park, Lisa;
Corporate Creator(s) : University of South Florida. Dept. of Civil and Environmental Engineering;American Transportation Research Institute;
Published Date : 2014-07-01
Report Number : BDK84-977-20
***URL :*** https://rosap.ntl.bts.gov/view/dot/27807

***Description:***
ATRI’s truck GPS data in Florida were used to measure average speeds on each mile of Florida’s SIS highway network for different time periods of the day. Three months of data in the year 2010 were used to generate the speeds.

1. Develop algorithms to convert large streams of ATRI’s truck GPS data into a more useable truck trip format.
2. Analyze truck trip characteristics in Florida using ATRI’s truck GPS data. - 4 months of ATRI’s truck GPS data
3. Assess ATRI’s truck GPS data in terms of its coverage of truck traffic flows in Florida.

The raw GPS data streams from ATRI need to be converted into a truck trip format to realize the full potential of the data for freight planning applications. The project resulted in algorithms to convert the raw GPS data into a database of truck trips. The results from the algorithms were
subjected to different validations to confirm that the algorithms can be used to extract accurate trip information from raw GPS data provided by ATRI.

These algorithms were then applied to four months of raw GPS data from ATRI, comprising a total of 145 million raw GPS data records, to develop a large database of truck trips traveling within, into, and out of the state. The resulting database comprised more than 1.2
million truck trips traveling within, into, and out of the state. 

The truck travel characteristics analyzed include trip duration, trip length, trip speed, time-of-day profiles, and Origin Destination (OD) flows. 

Four months of ATRI’s GPS data -->  OD tables at the TAZ-level spatial resolution.

Convert the raw GPS data into a data base of truck trips. 
Development of such a truck trip database involved the determination of truck starting and ending instances and locations, trip distance, total trip duration, and duration of intermediate stops (e.g., at traffic signals and rest stops) in the trip.

Each record within the database contained the following information:
1. Unit Information: A unique identifier for the transponder/truck.
2. Geographic Information: The latitude and longitude data that identify where a truck
position record was recorded.
3. Temporal Information: The time at which a truck position record was recorded, in the following format – MM-DD-YYYY HH:MM:SS.
![image](https://github.com/shradha125/TBD-Center-Freight-Data-Research-Project/assets/69496783/fd267b92-2456-4f5f-b498-05d9a281173d)

Unique Truck ID -> Confidential

Narrowed down to include specific segments that fall along Florida’s SIS road network (in this case).

 With the network divided into segments and the truck GPS data assigned a unique segment ID, the data for each segment were aggregated and sorted into the
following five time bins:
 AM Peak: 6:00 a.m. – 9:59 a.m.
 Mid-day: 10:00 a.m. – 2:59 p.m.
 PM Peak: 3:00 p.m. – 6:59 p.m.
 Off-peak: 7:00 p.m. – 5:59 a.m.
 Average of all hours: 12 a.m. – 11:59 p.m

Average speeds were calculated for each segment during each time period.
