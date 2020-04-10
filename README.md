# Data from Google Popular Times & photos taken from Huayi's roof

## Data
- curpop_df: live popularity score. 
	- On a scale of 0-100. 
	- Collected every 10 min
	- binned to 15 min time binns. The bins are 05-20, 20-35, 35-50, 50-1:05. 
- weekpop_df: static popularity provided by Google.
	- On a scale of 0-100. 
	- Monday-Sunday, each day has 24 hours
- image_label: safety level labelled based on photos taken from the roof every hour
	- 0: safe, 1: unsafe, 2: not sure. 
	- binned to the time bin closest to the time that these photos are taken
	- Thoughts:
		- can look into how to interpolate this data to other nearby time bins. 
		- Or maybe impute it somehow based on weather data and the live popularity data for nearby time bins. 