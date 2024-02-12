# Project-1

## Sea Level Rise Comparison Tool

## Collaborators

* Dr. Dick Davis II
* Jana Avery
* Jay Requarth
* John Andrews
* Mathew Nicholas
* Nee Buntoum
* Yeongjin Nam
  
  https://github.com/GuyInFreezer/project-1/assets/101156624/9dbab4d4-eefc-41a5-a259-cd7e63757956

## Overview

 This program provides a comparison of sea level rise between two cities. It visualizes historical sea level data, projects future trends, and highlights potential impacts on coastal communities.

 This program was originally designed to help New Hanover County allocate funds to mediate the effect of sea level rise. All data is average monthly in the format yyyy-mm-01. All data is assumed to
 be on the 1st of the month. However, the program is written to compare any 2 locations in the world where sea level data is available. city1 = location 1. This sea level rise data is compared to northern hemisphere temperature. A correlation between sea level rise to northern hemisphere temperature rise
 city2 = location 2. The sea level rise from location 1 and location 2 are plotted, and a correlation is determined.
 The PSMSL.org data is used because, at some sites, sea level data is available for more than 80 years.Add information from the PDF article about PSMSL.org. Why are they considered a valid source? How much data is available? etc. Wilmington is such a site. Data is available since 1935. Only 17 data points is missing. The reference point was set in 1970 at -7000 mm. Thus, on that day, the mean sea level was +7000.Missing data is denoted by -9999 and was cleaned.

## Features

* Data Visualization: Utilizes interactive graphs and maps to illustrate sea level rise trends over time.
  
* City Comparison: Allows users to compare sea level rise between two selected cities.
  
* Future Projections: Provides projections of future sea level rise based on climate change models.
  
* Impact Assessment: Identifies areas at risk of flooding and potential impacts on infrastructure and communities.

## Installation

1. Clone this repository to your local machine.
2. Download the data from the PSMSL.org website. Go to Home page:

   <img src="images/psmsl_home.jpg"
        alt="PSMS home" 
        width="250" 
        height="150" 
        style="display: block; margin: 0 auto; align: center;" />
3. Click on "Data" link, then“Obtaining Tide Gauge Data:” link.

    <img src="images/TideGaugeData.jpg" 
        alt="Tide Gauge Data" 
        width="250" 
        height="150" 
        style="display: block; margin: 0 auto; align: center;" />
4. Select the Station Name or Station ID. Click on the Station ID link.

   <img src="images/stationID_link.jpg" 
        alt="station id" 
        width="250" 
        height="150" 
        style="display: block; margin: 0 auto; align: center;" />

5. Look at “Time span of data:” and “Completeness (%)” to see if the data is of interest. If yes, click on “Download monthly mean sea level data.” hyperlink located to
the right of the sea level graph.
The data will download. Make sure Xcode is available on your computer.
To convert the data to a .csv format, open the data using the Xcode application.
You should see data that looks something like this: yyyy.mmmm; nnnn; 0;0000
yyyy = year. mmmm is a decimal format for month: mmmm=(M−0.5)/12
With M = the integer for the month. For example, April = 04. nnnn is millimeters above the reference (which was set at -7000 mm in 1970)
6. The rlrdata looks like this:

   <img src="images/rlrdata.jpg" 
        alt="rlr data" 
        width="250" 
        height="150" 
        style="display: block; margin: 0 auto; align: center;" />
7. Copy and paste the data into an Excel spreadsheet. Save as “Wilmington.csv” file.

   <img src="images/Wilmingtondotcsv.jpg"
        alt="wilmington" 
        width="250" 
        height="150" 
        style="display: block; margin: 0 auto; align: center;" />

8. Add the Wilmington.csv file to the Resource folder. Do the same for the second city, and the third, and so on. Just before running the program, change the csv file name to city1.csv and city2.csv. Run program. When the program asks you to select the file to upload, open the Resource folder and click on city1.csv.
9. The northern hemisphere temperature data will be loaded with the “https://_______ hyperlink” imbedded in the program. This data is in the classic csv format with each row being a different year (yyyy) and each column a different month. An imbedded for-loop is used to create a 2 column dataframe with a date time in the yyyy-mm-01 format. All data is assumed to be entered for the month on the 1st of the month.When the program asks you to select the file to upload, open the Resource folder and click on the city2.csv.df = city_1.cvs df[‘date’ , ‘height’]
height variable is in mm. drop a height <= 5000, because na = -9999. The date variable was an object and it had hidden alpha-numerics: ‘\xa0  1942.5417’Remove the alpha-numerics and spaces. The first 4 digits before the decimal point is the year (yyyy). The 4 digits after the decimal point are the month. (M-0.5)/12, with M = the numerical month (April = 04). The month is determined using this
equation.new_df = a new dataframe with an index, datetime variable, and height variable. Prophet is used to predict future data.
ds: x-axis (independent variable) in datetime format: yyyy-mm-dd
y:  y-axis  (dependent variable) in an integer format.
temps from the https:// hyperlink
test_df is the new dataframe – index, ds (datetime), y (y-axis)
combined_df – inner merge of new_df file and test_df on datetime plot sea level for city1 vs Temperature rise.
Do a correlation. Upload city2 so that we can compare the 2 cities. cities_df – merge new_df and city_2_df on ds(datetime). Plot the sea level rise for the 2 cities on different y-axes and datetime on the x-axis. Check the correlation.

Download README in pdf here:

[README for Project1.pdf](https://github.com/GuyInFreezer/project-1/files/14230952/README.for.Project1.pdf)

## Works Cited

1. PSMSL Data 
Permanent Service for Mean Sea Level (PSMSL). (n.d.). Data retrieved from PSMSL.org, Fortran IV datafile accessed via MatLab program in Xcode, manipulated and analyzed using Pandas in Python.

2. NASA Northern Hemisphere Temperature Data NASA Goddard Institute for Space Studies. (n.d.). Northern Hemisphere Temperature Anomalies. Retrieved from https://data.giss.nasa.gov/gistemp/tabledata_v4/NH.Ts+dSST.csv

3. Energy Units Basics,
U.S. Energy Information Administration. (n.d.).  Energy Units Basics.
Retrieved from: https://www.eia.gov/kids/what-is-energy/energy-units-basics.php

4. Climate Change Indicators: Arctic Sea Ice 
United States Environmental Protection Agency. (n.d.). Climate Change Indicators: Arctic Sea Ice. Retrieved from https://www.epa.gov/climate-indicators/climate-change-indicators-arctic-sea-ice

Download works cited in pdf here:

[worksCited.pdf](https://github.com/GuyInFreezer/project-1/files/14234906/worksCited.pdf)


