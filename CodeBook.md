The run_analysis.R script follows the 5 steps required as described in the course project’s definition.

0. Download the dataset
Dataset downloaded and extracted under the folder called UCI HAR Dataset.

1. Assign each data to variables

  * features <- features.txt 
  * activities <- activity_labels.txt
  * subject_test <- test/subject_test.txt
  * x_test <- test/X_test.txt
  * y_test <- test/y_test.txt
  * subject_train <- test/subject_train.txt
  * x_train <- test/X_train.txt
  * y_train <- test/y_train.txt

2. Merges the training and the test sets to create one data set

x_data and y_data are created using the rbind() function as well as subject_data and merged_data are created with rbind() and cbind() respectively.

3. Extracts only the measurements on the mean and standard deviation for each measurement
tidy_data is created subsetting merged_data and selecting only columns: subject, code and the measurements on the mean and standard deviation (std) for each measurement

4. Uses descriptive activity names to name the activities in the data set
Numbers in code column are replaced with it's activity taken from second column of the activities variable

5. Appropriately labels the data set with descriptive variable names
I have replaced in name column:
* Acc -> Accelerometer
* Gyro -> Gyroscope
* BodyBody -> Body
* Mag -> Magnitude
* f -> Frequency
* t -> Time

6. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject
FinalData is created using the summarise_all() function applied to tidy_data.
Export FinalData into FinalData.txt file.


README
Peer-graded Assignment: Getting and Cleaning Data Course Project
This repository is a Nunno Nugroho submission for Getting and Cleaning Data course project. It has the instructions on how to run analysis on Human Activity recognition dataset.

Dataset
Human Activity Recognition Using Smartphones

Files
CodeBook.md a code book that describes the variables, the data, and any transformations or work that I performed to clean up the data

run_analysis.R performs the data preparation and then followed by the 5 steps required as described in the course project’s definition:
Merges the training and the test sets to create one data set.
Extracts only the measurements on the mean and standard deviation for each measurement.
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive variable names.
From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
FinalData.txt is the exported final data after going through all the sequences described above.
