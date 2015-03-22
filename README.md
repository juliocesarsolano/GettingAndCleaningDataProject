# GettingAndCleaningDataProject
GettingAndCleaningDataProject

Step by Step:

Part 1: Merge the training and the test sets to create one data set.

    Training/Test measurements are read into different variables.
    Merging (making a union) of both sets using rbind.

Part 2: Extracts only the measurements on the mean and standard deviation for 
        each measurement

    Features indices are read into a matrix[idx,featureName]
    Features are filtered using grep containing "mean" or "std"
    DataSet columns are filtered by indices returned in second step
    Training/Test activities are read into different variables
    Merging (making a union) of both sets using rbind
    Training/Test subjects are read into different variables
    Merging (making a union) of both sets using rbind
    Merging measurements,activities,subjects using cbind

Part 3: Uses descriptive activity names to name the activities in the data set

    Activity column is converted into factor
    Activity factor is renamed with descriptive activity names
    Activity column is assigned the descriptive factors

Part 4: Appropriately labels the data set with descriptive activity names.

Part 5: Creates a second, independent tidy data set with the average of each 
        variable for each activity and each subject.

    Data set created above is transformed into a data table.
    Columns are averaged grouping by "Activity" and "subject"
    columns are renamed with a descriptive name: 'mean("measurament")'
    Tidy set is written to a file.
