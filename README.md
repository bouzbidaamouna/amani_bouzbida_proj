ashrae-energy-prediction

**Variable Desicription


-Train

building_id - Foreign key for the building metadata.

meter - The meter id code. Read as {0: electricity, 1: chilledwater, 2: steam, 3: hotwater}. Not every building has all meter types.

timestamp - When the measurement was taken

meter_reading - The target variable. Energy consumption in kWh (or equivalent). Note that this is real data with measurement error, which we expect will impose a baseline level of modeling error.

-building_meta

site_id - Foreign key for the weather files.

building_id - Foreign key for training.csv

primary_use - Indicator of the primary category of activities for the building based on EnergyStar property type definitions

square_feet - Gross floor area of the building

year_built - Year building was opened

floor_count - Number of floors of the building

-weather_[train/test]

Weather data from a meteorological station as close as possible to the site.

air_temperature - Degrees Celsius

cloud_coverage - Portion of the sky covered in clouds, in oktas

dew_temperature - Degrees Celsius

precip_depth_1_hr - Millimeters

sea_level_pressure - Millibar/hectopascals

wind_direction - Compass direction (0-360)

wind_speed - Meters per second


1/ Importing Packages and Collecting Data

2/Variable Description and Identification

3/Feature Engineering:

       Engineered features include:
       
          Month of the year
          
          Day of the week of the timestamp
          
          Hour of the day
          
       Imputing Missing variable
       
       Encoding Categorical Variable
       
 4/ Modeling LSTM       
