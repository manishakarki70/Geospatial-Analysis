# Geospatial-Analysis

This project is designed for geospatial analysis using Python. It focuses on querying geospatial data from Bing Maps, saving the results, and preparing them for analysis.


**Here's a breakdown of its functionality:** 

1. **Imports and Setup:**

   → It imports necessary modules such as formulas (for map_splitter and bing_maps_query), secrets (for BING_MAPS_KEY), and standard libraries 
     like time, requests, pandas, os, and json.

   → The BING_MAPS_KEY is used for authenticating requests to the Bing Maps API.

2. **Reading Input Data:**

   → The notebook reads a CSV file named Square Builder.csv containing geospatial coordinates. This file is expected to be in the current 
     working directory.
   
3. **Defining Geospatial Boundaries:**

   → It extracts coordinates for the four corners of a rectangular area: upper_left, lower_left, upper_right, and lower_right.

4. **Splitting the Map:**

   → The map_splitter function generates a grid of query points within the defined rectangular area.

5. **Querying Bing Maps:**

   → For each query point, the bing_maps_query function is called to fetch geospatial data from Bing Maps. The results are saved as JSON files (e.g., 0.txt, 1.txt, etc.) to ensure data persistence.
   
6. **Processing Results:**

   → The notebook reads one of the saved JSON files (e.g., 7.txt), extracts the results, and converts them into a Pandas DataFrame for further 
     analysis.
   
7. **Output:**

   → The final output is a DataFrame containing the queried geospatial data.
