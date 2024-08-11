# RideShare

## Table of Contents
1. [Introduction](#introduction)
2. [Objectives](#objectives)
3. [Dataset Description](#dataset-description)
4. [Data Preprocessing](#data-preprocessing)
5. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
6. [Data Visualization](#data-visualization)
7. [Modeling](#modeling)
8. [Results](#results)
9. [Conclusions](#conclusions)
10. [Future Work](#future-work)
11. [References](#references)

## Introduction
In recent years, ride-sharing services have revolutionised urban transportation by providing a convenient and flexible alternative to traditional taxis and public transit. Uber, in particular, has grown exponentially, offering millions of rides daily across various cities worldwide. Understanding the patterns and dynamics of rides is crucial for several reasons, including improving service efficiency, optimising pricing strategies, and enhancing user experience.

This project aims to analyse the ride share dataset to uncover valuable insights into ride patterns, demand fluctuations, and key factors influencing ride behavior. By exploring this dataset, we can answer questions such as:

- What are the peak hours for Uber rides?
- Which locations have the highest demand for Uber services?
- How do external factors like weather and events impact ride frequency?
- Can we predict the demand for rides based on historical data?

Through comprehensive data preprocessing, exploratory data analysis (EDA), and advanced modeling techniques, this project will provide a detailed understanding of the ride share ecosystem. The findings from this analysis can help Uber and similar ride-sharing companies optimise their operations and better serve their customers.

The dataset used in this project includes information on rides such as date and time, pickup locations, and the affiliated TLC base company codes. By leveraging this data, we will conduct a thorough analysis and develop predictive models to forecast ride demand and identify key trends.

## Objectives
List the main goals and objectives of the project. Examples:
- Analyse the patterns in ride share data.
- Identify peak hours of operation.
- Determine the most popular pickup and drop-off locations.
- Predict the demand for rides.

## Dataset Description
### Source
- The dataset was obtained from [nyc]((https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page).
  
### Features
- `VendorID`: A code indicating the TPEP provider that provided the record.
  -- 1= Creative Mobile Technologies, LLC.
  -- 2= VeriFone Inc.
- `tpep_pickup_datetime`: The date and time when the meter was engaged. 
- `tpep_dropoff_datetime`: The date and time when the meter was disengaged.
- `passenger_count`: The number of passengers in the vehicle (recorded by driver).
- `trip_distance`: The elapsed trip distance in miles (reported by the taximeter).
- `pickup_longitude`: Longitude of the pickup location.
- `pickup_latitude`: Latitude of the pickup location.
- `RatecodeID`: The final rate code in effect at the end of the trip.
  * 1 = Standard rate
  * 2 = JFK
  * 3 = Newark
  * 4 = Nassau or Westchester
  * 5 = Negotiated fare
  * 6 = Group ride
- `store_and_fwd_flag`: This flag indicates whether the trip record was held in vehicle memory before sending to the vendor, aka “store and forward,” because the vehicle did not have a connection to the server.
  * Y = store and forward trip
  * N = not a store and forward trip
- `dropoff_longitude`: Longitude of the drop off location.
- `dropoff_latitude`: Latitude of the drop off location.
- `payment_type`: A numeric code signifying how the passenger paid for the trip.
  * 1 = Credit card
  * 2 = Cash
  * 3 = No charge
  * 4 = Dispute
  * 5 = Unknown
  * 6 = Voided trip
- `fare_amount`: The time-and-distance fare calculated by the meter.
- `extra`: Miscellaneous extras and surcharges. Currently, this only includes the $0.50 and $1 rush hour and overnight charges.
- `mta_tax`: $0.50 MTA tax that is automatically triggered based on the metered rate in use.
- `tip_amount`: Tip amount (automatically populated for credit card tips. Cash tips are not included).
- `tolls_amount`: Total amount of all tolls paid in trip.
- `improvement_surcharge`: $0.30 improvement surcharge assessed trips at the flag drop. The improvement surcharge began being levied in 2015.
- `total_amount`: The total amount charged to passengers. Does not include cash tips.

## Data Preprocessing
### Feature Engineering
- Converted pickup and drop off dateTime front String to dateTime type
- Added a duration column using the difference between pickup and dropoff time

## Exploratory Data Analysis (EDA)
### Univariate Analysis
Examined:
- Distribution of ride times.
- Distribution of pickup locations.

### Bivariate Analysis
Explore relationships between:
- Correlation between time of day and ride frequency.
- Heatmap of pickup locations.

