Two data sets were downloaded containing information regarding school identifications and ACT/SAT values.

Since we are trying to determine the relationship between schools’ ACT/SAT averages and socioeconomic values, we needed to join the data sets. 
We did so as a left join on the school ID using the EDGap_data as the template. Before this, we removed unnecessary values from our edu_raw dataset that were not necessary for our interpretation. 
Next, we removed all NaN values from ACT/SAT values to avoid skew. Then, using an iterative imputer, we trained and fit the imputer to fill all remaining NaN values.

However, during data preparation, specifically during the edu_raw upload and during the join, there were issues that impeded our process.

First, during the upload of edu_raw, there were fewer columns than specified by the course; after further investigation, the downloaded file was missing many columns, most importantly “CHARTER_TEXT.”

Second, during the left join procedure, the process created entire columns of NaNs for values like State, Zip Code, etc.

Therefore, no clean CSV has been created at this time. Further work will be done ASAP.
