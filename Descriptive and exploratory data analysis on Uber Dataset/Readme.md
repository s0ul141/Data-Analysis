# Uber Rides Analysis in New York City (April-September 2014)

## Table of Contents
1. [Introduction](#introduction)
2. [Data Preparation](#data-preparation)
3. [Temporal Analysis](#temporal-analysis)
   3.1 [Hourly Analysis](#hourly-analysis)
   3.2 [Daily Analysis](#daily-analysis)
   3.3 [Monthly Analysis](#monthly-analysis)
   3.4 [Day of Week Analysis](#day-of-week-analysis)
4. [Base Analysis](#base-analysis)
5. [Heat Map Visualizations](#heat-map-visualizations)
6. [Geospatial Analysis](#geospatial-analysis)
7. [Conclusion](#conclusion)

## 1. Introduction <a name="introduction"></a>

This report presents an in-depth analysis of Uber ride data in New York City from April to September 2014. The analysis explores various temporal and spatial patterns in ride frequency, providing insights into usage trends across different time scales and geographical areas. Understanding these patterns can help optimize service delivery, inform marketing strategies, and improve overall user experience.

## 2. Data Preparation <a name="data-preparation"></a>

The analysis began with loading and preprocessing data from six CSV files, each representing a month from April to September 2014. Key steps included:

- Combining monthly data into a single dataset (`data_2014`)
- Parsing and formatting date and time information using `lubridate` functions
- Creating new columns for day, month, year, day of the week, hour, minute, and second
- Ensuring proper data types for each column to facilitate analysis

This preparatory step was crucial for enabling the subsequent detailed temporal and spatial analyses.

## 3. Temporal Analysis <a name="temporal-analysis"></a>

### 3.1 Hourly Analysis <a name="hourly-analysis"></a>

We analyzed the distribution of rides across different hours of the day.
![Trips Every Hour](https://github.com/user-attachments/assets/1a60ed39-10f4-45d7-8815-aa122dd288ca)

*Figure 1: Distribution of trips across 24 hours*
This bar chart shows the number of Uber trips taken during each hour of the day. The x-axis represents the 24 hours of a day, while the y-axis shows the total number of trips. Key observations:

- Peak hours are clearly visible, with the highest number of trips occurring around 6 PM (18:00).
- There's another significant peak in the morning, around 8 AM (08:00).
- The lowest number of trips occurs in the early morning hours, between 3 AM and 5 AM.
- Trip volume gradually increases from early morning, peaks in the evening, and then declines into the night.

We also examined how hourly patterns changed across different months.

![Trips by Hour and Month]()

*Figure 2: Hourly trip distribution by month*

Observations:
- The general pattern of peak hours remains consistent across months.
- Summer months (June-August) show higher ride volumes, especially during evening hours.
- April and May have lower overall ride volumes, possibly due to milder weather encouraging alternative transportation.

### 3.2 Daily Analysis <a name="daily-analysis"></a>

We investigated how ride frequency varied across days of the month and across different months.

![Trips Every Day]()

*Figure 3: Trip frequency by day of the month*

![Trips by Day and Month]()

*Figure 4: Daily trip patterns across months*

Observations:
- There's no strong pattern associated with specific days of the month.
- Weekends (visible as regular spikes every 7 days) generally show higher ride volumes.
- Certain days show unexpected spikes or dips, possibly due to events or holidays.
- The overall trend shows increasing ride volumes from April to September.

### 3.3 Monthly Analysis <a name="monthly-analysis"></a>

We examined the overall trend in ride volume across the six months.

![Trips by Month]()

*Figure 5: Monthly distribution of trips*

Observations:
- There's a clear upward trend in ride volume from April to September.
- The largest increase appears to be between May and June.
- September has the highest number of rides, possibly due to a combination of good weather and increased business activity after summer vacations.

### 3.4 Day of Week Analysis <a name="day-of-week-analysis"></a>

We analyzed how ride patterns differed across days of the week and how these patterns changed from month to month.

![Trips by Day and Month]()

*Figure 6: Trip patterns by day of week and month*

Observations:
- Fridays and Saturdays consistently show the highest ride volumes across all months.
- Sundays and Mondays tend to have the lowest ride volumes.
- The difference between weekday and weekend ride volumes becomes more pronounced in the summer months.

## 4. Base Analysis <a name="base-analysis"></a>

We investigated the distribution of rides across different Uber bases and how base usage varied over time.

![Trips by Bases]()

*Figure 7: Distribution of trips across Uber bases*

![Trips by Bases and Month]()

*Figure 8: Base usage patterns by month*

![Trips by Bases and DayofWeek]()

*Figure 9: Base usage patterns by day of week*

Observations:
- Base B02617 handles the highest number of rides, followed by B02598.
- The relative usage of bases remains fairly consistent across months, with all bases showing the general upward trend from April to September.
- Some bases show more pronounced weekend spikes than others, suggesting they might be located closer to entertainment districts.

## 5. Heat Map Visualizations <a name="heat-map-visualizations"></a>

We created several heat maps to visualize complex patterns in the data:

![Heat Map by Hour and Day]()

*Figure 10: Heat map of trips by hour and day*

![Heat Map by Month and Day]()

*Figure 11: Heat map of trips by month and day*

![Heat Map by Month and Day of Week]()

*Figure 12: Heat map of trips by month and day of week*

![Heat Map by Month and Bases]()

*Figure 13: Heat map of trips by month and base*

![Heat Map by Bases and Day of Week]()

*Figure 14: Heat map of trips by base and day of week*

Observations:
- The hour-day heat map clearly shows the daily rush hour patterns.
- The month-day heat map reveals an overall increase in intensity (ride volume) as months progress.
- The month-day of week heat map shows that Friday and Saturday intensities increase more dramatically in summer months.
- The month-base heat map confirms that all bases see increased activity in later months.
- The base-day of week heat map shows that some bases have more pronounced day-of-week patterns than others.

## 6. Geospatial Analysis <a name="geospatial-analysis"></a>

We mapped the geographical distribution of Uber rides in NYC.

![NYC MAP BASED ON UBER RIDES DURING 2014 (APR-SEP)]()

*Figure 15: Geographical distribution of all Uber rides*

![NYC MAP BASED ON UBER RIDES DURING 2014 (APR-SEP) by BASE]()

*Figure 16: Geographical distribution of Uber rides by base*

Observations:
- Ride density is highest in Manhattan, particularly in Midtown and Lower Manhattan.
- There are also high concentrations of rides in parts of Brooklyn and Queens, likely in popular commercial or residential areas.
- Each base seems to have a primary area of operation, though there is significant overlap.
- Some bases appear to specialize in airport rides, as indicated by concentrations near JFK and LaGuardia airports.

## 7. Conclusion <a name="conclusion"></a>

This analysis of Uber ride data in New York City from April to September 2014 reveals several key insights:

1. Temporal Patterns: Clear daily patterns with morning and evening rush hour peaks, weekly patterns with higher weekend usage, and a monthly trend of increasing ride volumes from spring to late summer.

2. Seasonal Effects: Summer months see higher ride volumes, particularly in evening hours and weekends, likely due to increased tourism and outdoor activities.

3. Base Operations: While some bases handle significantly more rides than others, all follow similar temporal patterns and saw growth over the analyzed period.

4. Geographical Concentrations: Rides are heavily concentrated in Manhattan, with secondary hotspots in parts of Brooklyn, Queens, and around airports.

These findings can inform strategic decisions such as:
- Adjusting driver availability to match hourly and weekly demand patterns
- Tailoring marketing efforts to capitalize on seasonal trends
- Optimizing base operations and coverage areas
- Focusing expansion efforts on high-demand areas and times

Future analyses could benefit from incorporating additional data such as weather conditions, local events, and broader transportation trends to provide even deeper insights into ride-sharing patterns in New York City.