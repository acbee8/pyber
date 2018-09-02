# pyber
Using Python Matplotlib and Seaborn libraries to examine and visually represent ride sharing trends in relation to individual cities and their 'Type's {Urban, Suburban, Rural}.

Objectives:
*To build bubble plot showcasing the relationship between four key variables:
- Average Fare ($) Per City
- Total Number of Rides Per City
- Total Number of Drivers Per City
- City Type (Urban, Suburban, Rural)

*To produce summative pie charts showing:
- % of Total Fares by City Type
- % of Total Rides by City Type
- % of Total Drivers by City Type

Process:
1. Established connections to needed libraries [Numpy, Matplotlib, Pandas, & Seaborn].

2. Read in and then merged the two CSVs that tracked number of drivers per city and ride information. This allowed the data to be amassed into a singular dataframe on which I performed initial summary calculations and groupings to inspect the data. 

3. Only using grouped-by' data would not have allowed comparative manipulations needed to produce requested visualizations. So, I broke out individual series to manipulate city-linked data and clean up values (associating individual rides with all others from that city, calculating averages, rounding, dropping unrelated columns/data like ride_ids).

4. Adding all desired series to a final dataframe and renaming columns appropriately set up the ability to cycle through the same dataframe and use .loc for the variables to be plotted.

5. Created a summary table for % of Total Fares Data to inform the three pie charts. Using the original ride_by_city data and dropping the ride_id column produced all the summary data needed. Then summed all the data and saved as it's own row to append to the table [mostly for comparative/further information for the viewer of the pie charts, as the exact 'counts' or 'sums' weren't on the charts].

6.Created a scatter plot with bubbles sized at a 1/2 point for every 20 drivers in that city [driver count as size of bubble], plotted each point per city type using the number of rides for the city [to show which city type had concentrations of number of rides] as the x coordinate on the graph and the fare as the y [to cluster the prices per type possibly showing a trend for ideal ratios between number of drivers, fare cost and rides taken]. Color coded and outlined each plot point: Light Blue = Urban, Light Coral = Suburban & Gold = Rural.

7. The data seems to suggest that Rural fares were the highest per ride, which would make sense likely given geographical distance between locations. Urban riders took more but less expensive trips, again likely reflective of city travel between short distance locations. A suburban outlier with more than 60 rides was left in to warrant further investigation of the possible event or events that triggered the high usage despite above average fare rates when compared to other Suburban data points. 
