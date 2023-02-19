# new
Project data source: https://www.kaggle.com/datasets/dhruvildave/ookla-internet-speed-dataset
Introduction
This dataset provides global fixed broadband and mobile (cellular) network performance metrics in zoom level 16 web mercator tiles (approximately 610.8 meters by 610.8 meters at the equator). Data is provided in both Shapefile format as well as Apache Parquet with geometries represented in Well Known Text (WKT) projected in EPSG:4326. Download speed, upload speed, and latency are collected via the Speedtest by Ookla applications for Android and iOS and averaged for each tile. Measurements are filtered to results containing GPS-quality location accuracy.

Content
Field Name	Type	Description
avg_d_kbps	Integer	The average download speed of all tests performed in the tile, represented in kilobits per second.
avg_u_kbps	Integer	The average upload speed of all tests performed in the tile, represented in kilobits per second.
avg_lat_ms	Integer	The average latency of all tests performed in the tile, represented in milliseconds.
tests	Integer	The number of tests taken in the tile.
devices	Integer	The number of unique devices contributing tests in the tile.
quadkey	Text	The quadkey representing the tile.
tile	Text	Well Known Text (WKT) representation of the tile geometry.
Quadkeys can act as a unique identifier for the tile. This can be useful for joining data spatially from multiple periods (quarters), creating coarser spatial aggregations without using geospatial functions, spatial indexing, partitioning, and an alternative for storing and deriving the tile geometry.

Two layers are distributed as separate sets of files:

mobile - Tiles containing tests taken from mobile devices with GPS-quality location and a cellular connection type (e.g. 4G LTE, 5G NR).
fixed - Tiles containing tests taken from mobile devices with GPS-quality location and a non-cellular connection type (e.g. WiFi, Ethernet).
Quarter 1 refers to data from January to March. Quarter 2 refers to data from April to June. Quarter 3 refers to data from July to September. Quarter 4 refers to data from October to December. All the data is from the year 2020.

Citation
Speedtest® by Ookla® Global Fixed and Mobile Network Performance Maps. Based on analysis by Ookla of Speedtest Intelligence® data for 2020. Provided by Ookla and accessed February 15, 2021. Ookla trademarks used under license and reprinted with permission.

Image Credits: Unsplash - umby


