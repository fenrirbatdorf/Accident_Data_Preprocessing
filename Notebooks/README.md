# Accident_Data_Preprocessing
Steps taken to preprocess car accident data for research.

This repo is for Fenrir Badorf's 2025 NIST SURF summer project, examining if CFD is a useful tool for feature engineering and dimensionality reduction.

The source file for this project can be found at: https://smoosavi.org/datasets/us_accidents. A subset of this data containing only Maryland accidents is included in this repo, in the folder Data_Raw -> full_data.

FILES:

Data_Initial_Split: The file that serves as the initial train test split of the data, to prevent information from the test data to affect the training data.

Dr_Olsen_Control_Preprocess: The file written by Dr. Olsen to take the MD traffic subset, and preprocess the data for machine learning without feature engineering. This serves as the control version of the datasets for the experiment.

Fenrir_Feature_Engineer: The file needed to preprocess the full traffic dataset down to only MD, and then to create the feature engineer version of the dataset.

Files beginning with OLD: Previous drafts of programs to use that are not in use for the current version of the experiment.

PCA_Process: A hands-on learning file to get used to PCA in Python.

Pipeline: An as-of-yet unfinished and unused pipeline for the model, to train on the various versions of the reduced dataset.

PROCESS: An ongoing to-do of versions of the dataset that have been or will be created, as well as any steps needed to do each part of the experiment.


NOTE: There are 3 main data processing files used to begin the process: Data_Initial_Split, Dr_Olsen_Control_Preprocess, and Fenrir_Feature_Engineer_Repair (From now on referred to as split, dr olsen and fenrir).

The split notebook is simply a dedicated instance of Scikit-Learn's train_test_split function, to divide the MD subset of data into a training set and a testing set before cleaning. These training and testing sets are then saved to: Data_Raw -> test_set, and Data_Raw -> train_data.


The dr olsen notebook takes the training/testing datasets from the folder Data_Raw, and cleans each without significantly changing the contents of the dataset. 

NOTE 1: The dataset linked above is much larger than the dataset taken by this program, which only takes the subset of all data which occurred in Maryland.

NOTE 2: Both dr olsen notebook and fenrir notebook have the capacity to take train sets or test sets as inputs, which use different arguments. It is VERY important that the user confirm they have input the correct function arguments at the beginning and end of the notebooks in order for the data to be processed and output with the correct names and information.


The fenrir notebook takes the MD subset dataset located in the repo, cleans and preprocesses the data in a slightly different manner, and then adds feature engineered columns. This is meant to be a comparison dataset to the dr olsen preprocessed data result, and both serve as jumping off points for differences in dimensionality reduction. 

After cleaning the data in either notebook, the data is saved to:
Data_Cleaned -> test_data
and
Data_Cleaned -> train_data

If the user is also exporting one vs many variations of the training data, these data variations will be saved to: 
Data_Cleaned -> control_datasets_unbin -> Control_Class_Merge

