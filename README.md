# MODIS-Land-Surface-Temperature-data
The script extracts nighttime land surface temperature (LST) in Celsius for specific geographic points over a given time range using MODIS data. It handles missing data gracefully and outputs the results to the GEE console and as a downloadable CSV file for further analysis.

Key Features

Dataset:

MODIS/061/MOD11A1 (Terra LST).

Nighttime temperature band: LST_Night_1km.

Filtered to the date range: 2024-01-01 to 2025-01-01 (customizable).

Points of Interest:

Geographical points are defined as a FeatureCollection.

Each point has a name property for identification. In the script, one point is defined:

Point 3: Kolkata, India ([88.3639, 22.5726]).

More points can be added as needed.

Temperature Extraction:

Converts LST from Kelvin to Celsius using the formula:
LST_Celsius = (LST_Night_1km * 0.02) - 273.15.

Handles missing or null values in the data gracefully by assigning null to invalid entries.

Exporting Results:

Outputs valid data to the console.

Exports results as a CSV file to Google Drive for further analysis.
