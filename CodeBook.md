# CodeBook.md
## Original signals
The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

## Transformed signals
The tidy dataset comes from a statistical transformation of the original dataset to obtain only the variables measurement of the original dataset regarding the mean and standard deviation of the measurement by Subject and Activity.
**The variables related to columns containig "meanFreq()" where not included because as the Codebook states they are weighted averages and not means **
So each row has the mean of all the measurement of a single subject in a single activity. (E.g. Time Domain Body Acceleration Mean in Axis-X for subject 1 in WALKING, contains the mean of the body acceleration for subject 1 while walking)
Being the average and standard deviation of the original signals they mantains the same dimensional units of the original signals.


## Subject variables
The subject names are in the first column of the dataset and they are named 
- Subject XX : XX ranges from 1 to 30

## Activity variables
The subject names are in the second column of the dataset and they are named:
- WALKING
- WALKING_UPSTAIRS
- WALKING_DOWNSTAIRS
- SITTING
- STANDING
- LAYING

##Time Domain Variables

- Time Domain Body Acceleration Mean in Axis-(XYZ)  - 3 variables on the 3 axis (X,Y,Z) - measure is the mean of the corresponding time series (tBodyAcc-XYZ) by Subject and by activity
- Time Domain Body Acceleration Std. Dev. in Axis-(XYZ)  - 3 variables on the 3 axis (X,Y,Z) - measure is the standard deviation of the previous mean by Subject and by activity
- Time Domain Gravity Acceleration Mean in Axis-(XYZ) - 3 variables on the 3 axis (X,Y,Z) - measure is the mean of the corresponding time series (tGravityAcc-XYZ) by Subject and by activity 
- Time Domain Gravity Acceleration Std. Dev. in Axis-(XYZ) - 3 variables on the 3 axis (X,Y,Z) - measure is the standard deviation of the previous mean by Subject and by activity
- Time Domain Body Acceleration Jerk Mean in Axis-(XYZ)- 3 variables on the 3 axis (X,Y,Z) - measure is the mean of the corresponding time series (tBodyAccJerk-XYZ) by Subject and by Activity 
- Time Domain Body Acceleration Jerk Std. Dev. in Axis-(XYZ) - 3 variables on the 3 axis (X,Y,Z) - measure is the standard deviation of the previous mean by Subject and by activity
- Time Domain Body Gyroscopical Mean in Axis-(XYZ)- 3 variables on the 3 axis (X,Y,Z) - measure is the mean of the corresponding time series (tBodyGyro-XYZ) by Subject and by Activity
- Time Domain Body Gyroscopical Std. Dev. in Axis-(XYZ) - 3 variables on the 3 axis (X,Y,Z) - measure is the standard deviation of the previous mean by Subject and by activity
- Time Domain Body Gyroscopical Jerk Mean in Axis-(XYZ)- 3 variables on the 3 axis (X,Y,Z) - measure is the mean of the corresponding time series (tBodyGyroJerk-XYZ) by Subject and by Activity
- Time Domain Body Gyroscopical Jerk Std. Dev. in Axis-(XYZ) - 3 variables on the 3 axis (X,Y,Z) - measure is the standard deviation of the previous mean by Subject and by activity
- Time Domain Body Acceleration Magnitude Mean - 1 variable - measure is the mean of the corresponding time series (tBodyAccMag) by Subject and by Activity
- Time Domain Body Acceleration Magnitude Std. Dev. - 1 variable - measure is the standard deviation of the corresponding time series (tBodyAccMag) by Subject and by Activity
- Time Domain Gravity Acceleration Magnitude Mean - 1 variable - measure is the mean of the corresponding time series (tGravityAccMag) by Subject and by Activity
- Time Domain Gravity Acceleration Magnitude Std. Dev. - 1 variable - measure is the standard deviation of the corresponding time series (tGravityAccMag) by Subject and by Activity
- Time Domain Body Acceleration Jerk Magnitude Mean - 1 variable - measure is the mean of the corresponding time series (tBodyAccJerkMag) by Subject and by Activity
- Time Domain Body Acceleration Jerk Magnitude Std. Dev. - 1 variable - measure is the standard deviation of the corresponding time series (tBodyAccJerkMag) by Subject and by Activity
- Time Domain Body Gyroscopical Magnitude Mean - 1 variable - measure is the mean of the corresponding time series (tBodyGyroMag) by Subject and by Activity
- Time Domain Body Gyroscopical Magnitude Std. Dev. - 1 variable - measure is the standard deviation of the corresponding time series (tBodyGyroMag) by Subject and by Activity
- Time Domain Body Gyroscopical Jerk Magnitude Mean - 1 variable - measure is the mean of the corresponding time series (tBodyGyroJerkMag) by Subject and by Activity
- Time Domain Body Gyroscopical Jerk Magnitude Std. Dev. - 1 variable - measure is the standard deviation of the corresponding time series (tBodyGyroJerkMag) by Subject and by Activity

## Frequency Domain variables
- Frequency Domain Body Acceleration Mean in Axis-(XYZ)  - 3 variables on the 3 axis (X,Y,Z) - measure is the mean of the corresponding frequency series (fBodyAcc-XYZ) by Subject and by activity
- Frequency Domain Body Acceleration Std. Dev. in Axis-(XYZ) - 3 variables on the 3 axis (X,Y,Z) - measure is the standard deviation of the corresponding frequency series (fBodyAcc-XYZ) by Subject and by activity
- Frequency Domain Body Acceleration Jerk Mean in Axis-(XYZ)  - 3 variables on the 3 axis (X,Y,Z) - measure is the mean of the corresponding frequency series (fBodyAccJerk-XYZ) by Subject and by activity
- Frequency Domain Body Acceleration Jerk Std. Dev. in Axis-(XYZ) - 3 variables on the 3 axis (X,Y,Z) - measure is the standard deviation of the corresponding frequency series (fBodyAccJerk-XYZ) by Subject and by activity
- Frequency Domain Body Gyroscopical Mean in Axis-(XYZ)  - 3 variables on the 3 axis (X,Y,Z) - measure is the mean of the corresponding frequency series (fBodyGyro-XYZ) by Subject and by activity
- Frequency Domain Body Gyroscopical Std. Dev. in Axis-(XYZ) - 3 variables on the 3 axis (X,Y,Z) - measure is the standard deviation of the corresponding frequency series (fBodyGyro-XYZ) by Subject and by activity
- Frequency Domain Body Acceleration Magnitude Mean - 1 variable - measure is the mean of the corresponding frequency series (fBodyAccMag) by Subject and by Activity
- Frequency Domain Body Acceleration Magnitude Std. Dev. - 1 variable - measure is the standard deviation of the corresponding time series (fBodyAccMag) by Subject and by Activity
- Frequency Domain Body Body Acceleration Jerk Magnitude Mean - 1 variable - measure is the mean of the corresponding frequency series (fBodyAccJerkMag) by Subject and by Activity
- Frequency Domain Body Body Acceleration Jerk Magnitude Std. Dev. - 1 variable - measure is the standard deviation of the corresponding time series (fBodyAccJerkMag) by Subject and by Activity
- Frequency Domain Body Body Gyroscopical Magnitude Mean - 1 variable - measure is the mean of the corresponding frequency series (fBodyGyroMag) by Subject and by Activity
- Frequency Domain Body Body Gyroscopical Magnitude Std. Dev. - 1 variable - measure is the standard deviation of the corresponding time series (fBodyGyroMag) by Subject and by Activity
- Frequency Domain Body Body Gyroscopical Jerk Magnitude Mean - 1 variable - measure is the mean of the corresponding frequency series (fBodyGyroJerkMag) by Subject and by Activity
- Frequency Domain Body Body Gyroscopical Jerk Magnitude Std. Dev. - 1 variable - measure is the standard deviation of the corresponding frequency series (fBodyGyroJerkMag) by Subject and by Activity
