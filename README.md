# Accident_Data_Preprocessing
Steps taken to preprocess car accident data for research.

This repo is for Fenrir Badorf's 2025 NIST SURF summer project, examining if CFD is a useful tool for feature engineering and dimensionality reduction.

The source file for this project can be found at: https://smoosavi.org/datasets/us_accidents

NOTE: There are 2 main data processing files used to begin the process: Dr_Olsen_Control_Preprocess, and Fenrir_Feature_Engineer (From now on referred to as dr olsen and fenrir).

The dr olsen notebook takes the dataset in the folder data_raw, and cleans it without significantly changing the contents of the dataset. NOTE: The dataset linked above is much larger than the dataset taken by this program, which only takes the subset of all data which occurred in Maryland.

The fenrir notebook takes the full dataset located at the above link, cleans and preprocesses the data in a slightly different manner, and then adds feature engineered columns. This is meant to be a comparison dataset to the dr olsen preprocessed data result, and both serve as jumping off points for differences in dimensionality reduction.

The initial, Maryland only raw version of the dataset is saved in the Data_Raw folder, and all variations of the datasets needed are saved in the Data_Cleaned folder.


FILES:

Fenrir_Feature_Engineer: The file needed to preprocess the full traffic dataset down to only MD, and then to create the feature engineer version of the dataset.

Dr_Olsen_Control_Preprocess: The file written by Dr. Olsen to take the MD traffic subset, and preprocess the data for machine learning without feature engineering. This serves as the control version of the datasets for the experiment.

Files beginning with OLD: Previous drafts of programs to use that are not in use for the current version of the experiment.

PROCESS: An ongoing to-do of versions of the dataset that have been or will be created, as well as any steps needed to do each part of the experiment.