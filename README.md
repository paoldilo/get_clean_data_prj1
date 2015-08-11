# README.md
Assignment project for Coursera Getting and cleaning data README file

This file explains how the script works and the input/output data required and created by the script.
An explanation of the variables created in the output dataset and their measure scale can be found in the codebook 

## Reading the data
The script assumes you have unzipped the data in the *"UCI HAR Dataset/"* folder in your working directory and that the structure of the original dataset with folders *"UCI HAR Dataset/test"* and *"UCI HAR Dataset/training"* is maintained.

## Transforming the data
The scripts uses temporary variables to store the intermediate results from step 2 to step 4 of the assignment. The intermediate variable's number is minimized to keep memory occupation low.
In details the following transformations have been performed on the data:

- 2. Extracted only the measurements on the mean and standard deviation for each measurement
  -  Variables called *...MeanFreq...* will not be considered as they are "weighted averages" as the codebook says and not means
  - Variables called *angle(...Mean...)* will not be considered as they are angles of means and not means
- 3. Read the descriptive activity from file and applied them to the dataset
- 3a. Added the activity & subject columns to the dataset as factors to obtain a complete dataset
- 4. Appropriately labelled the data set with descriptive variable names.
- 4a. All short format abbreviations we substituted with a descriptive name (eg. "tBodyAcc-mean()-X" transformed in "Time Domain Body Acceleration Mean in Axis-X"
- 5. Created a second, independent tidy data set with the average of each variable for each activity and each subject using data.table summarization.

## Writing the output 
The script performs a final task of writing out the transformed dataset to a text file named **"Tidydataset.txt"**.
This file will be stored in your working directory and will occupy 200Kb on your hard drive.

##Reading back the dataset
If you need to perform further analysis on the dataset you can load it into R with the code:
tidydataset <-read.table("Tidydataset.txt", row.names = FALSE)
as long as "Tidydataset.txt" is in your working directory.