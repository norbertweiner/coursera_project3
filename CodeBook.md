##Code Book

This code book will describe the data used in this project.

###Data Set Overview

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. 
Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. 
Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. 
The experiments have been video-recorded to label the data manually. 
The obtained dataset has been randomly partitioned into two sets, 
where 70% of the volunteers was selected for generating the training data and 30% the test data. 

###Explanation of each file

* features.txt: Names of the 561 features.  

* activity_labels.txt: Names and IDs for each of the 6 activities.  

* X_train.txt: 7352 observations of the 561 features, for 21 of the 30 volunteers.  

* subject_train.txt: A vector of 7352 integers, denoting the ID of the volunteer related to each of the observations in X_train.txt.  

* y_train.txt: A vector of 7352 integers, denoting the ID of the activity related to each of the observations in X_train.txt.  

* X_test.txt: 2947 observations of the 561 features, for 9 of the 30 volunteers.  

* subject_test.txt: A vector of 2947 integers, denoting the ID of the volunteer related to each of the observations in X_test.txt.  

* y_test.txt: A vector of 2947 integers, denoting the ID of the activity related to each of the observations in X_test.txt.

###Data that were not used

This analysis was performed using only the files above, and did not use the raw signal data. 
Therefore, the data files in the "Inertial Signals" folders were ignored.

###Script Description 

1. Dataset is automatically downloaded. 
2. Raw data are stored in text files. Text files are read into the memory. 
3. Filter out mean and std data from a big table, then delete the big table to save memory. 
4. Add activity and subject id columns to the test data and train data. 
5. Combine train data and test data.
6. Calcualte mean value for each variable based on subject id and activity
7. Output a tidy.csv file. 
