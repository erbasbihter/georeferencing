# Georeferencing
This file contains the information about how to conduct data harmonization and georeferencing using GPS coordinates.

Each folder contains:
 - analysis: Codes that are used to georeference schools
 - cleaning: CENI and SIGE school names harmonization codes.
 - maps: Shape files or coordinates to create visuals
 - output: any cleaned data or georeferenced data.
 - raw: Raw data or data that are used as inputs.

Step 1: Harmonize school names by running the code in the 'cleaning' folder. The cleaned data is stored in the output folder with names
"cenischools_clean_v3.xlsx" and "sigeschools.xlsx" respectively. In addition to harmonizing school names, I'm removing duplicate school names which are
less than 1km close to each other in SIGE data as well.

Step 2: Start georeferencing by running Georeference_Kinshasa in the 'analysis' folder. The final output is stored in the 'output' folder.

Step 3: Move on with georeferencing by running Georeference_Others and Georeference_villes in 'analysis' folder. The final outputs are stored in the
'output' folder.

Step 4: Run the Georeference_Village_School code in the 'analysis' folder. This code does the matching for schools whose name is the village name. 
I'm removing the schools which are very close to each other here.


Step 5: Finally in Georeference_Buffer code, buffers for each admin variables are created and those finals are also stored in the 'output' folder. The very final result is  'matching_buffers4_40km'.
I'm also producing some tables/graphs here to compare matched and unmatched observations. The pdf version of this code can be also found in the same folder ('analysis') where the code is.
