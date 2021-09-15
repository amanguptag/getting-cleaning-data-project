# Code Book
generated 2021-09-15 16:06:12 during sourcing of `run_analysis.R`

## Actions performed on data:
* create data dir `./data`
* downloading zip file: [https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) to `./data`
* extracting zip file: `./data/data.zip` to `./data/UCI HAR Dataset`
* merging all *_test.txt and *_train.txt files into one dataset: `mergedData`
* `mergedData` loaded in memory, dimensions: 10299 x 563
* subsetted `mergedData` into `subSetMergedData` keeping only the key columns and features containing `std` or `mean`, dimensions : 10299 x 68
* merged `./data/UCI HAR Dataset/activity_labels.txt` contents with correct `activity_num` column, effectivly appending `activity_name` to `subSetMergedData`, dimensions : 10299 x 69
