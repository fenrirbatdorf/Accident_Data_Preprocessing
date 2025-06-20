This folder holds all versions of the dataset used in this project beyond the base, non preprocessed version.

DATASETS NAMING CONVENTION:

control: A dataset built from the preprocessed, non-feature engineered dataset (dr olsen control preprocess)

feat_eng: A dataset built from the preprocessed, feature engineered dataset (fenrir feature engineer)

class number(s) merge: A dataset version that merges/only contains the classes of the given numbers into one class, without changing any data.

EXAMPLES:
feat_eng_class2_3_merge: this dataset comes from the program fenrir feature engineer, removes classes 1 and 4, and merges classes 2 and 3 under one number. 

control_processed_traffic: Because this dataset does not contain any numbers or the word merge, but DOES contain the word control, it implies that this is the entire dataset based on the code dr olsen control preprocess, without changing/omitting/merging any of the 4 classes.
