# EEG-Analyzer

This repository aims to provide an introductory approach to EEG (Electroencephalography) signal processing, analysis, and visualization.

## Notebooks:

### Dataset creation

This code performs several data processing tasks using pandas to manipulate a series of EEG (Electroencephalography) data files.

The main characteristics of this code are:

1. **Adjusting Size**: It finds the minimum number of rows among all the DataFrames and trims each DataFrame to that minimum length to ensure they all have the same number of rows.

2. **Dividing DataFrames**: It defines a function `divide_into` that divides a DataFrame into X equal parts and resets the indices of each part. Then, it applies this function to each trimmed DataFrame and stores the parts in a dictionary `divided_dataframes`.

3. **Processing DataFrames**: For each DataFrame in `divided_dataframes`, it applies the transposition function to each of the 10 parts, concatenates the transposed parts into a single DataFrame, and assigns a corresponding target.

4. **Final Combination**: It concatenates all the combined DataFrames with their respective targets into a single final DataFrame `final_combined_dataframe`.

### Exploratory Analysis

**Data Overview**
- First Look at the Data
- Summary Statistics

**To Do:**
- Data Cleaning
- Univariate, Bivariate and Multivariate Analysis
- Insights

## Data

* Baseline: This part can be used to have negative examples of anything you want to detect. For example, if you want to detect changes when there is "imagination in violet colors," you extract features from that moment and from this one and try to build a classifier.
* Inhaling: Changes in low frequencies, where the movement of the diaphragm for inhaling is emphasized.
* Exhaling: Same as inhaling but emphasizing the movement of the diaphragm for exhaling.
* Taps: There should be some event with a certain peak in the signal. You can try to detect these peaks and see if there is anything.
* Mental Imagery: High frequencies of 20-50 Hz may appear. Increases in the power of these bands between this block and the baseline.
* Eyes Closed: There should be an increase in the specific frequency of 10 Hz relative to the baseline.

Created by me:
* Combined dataset X Partitions: Dataset that combines all the columns of the EEG and separates them into an X number of partitions. At the end, the target variable is added to identify which dataset it comes from. For example, if the blinking dataset has 30830 samples, then 10 blinking samples are divided and the data 'blinking' is added to the target column.

## Objetive

The objective is to implement an analysis of these data, exploratory, supervised, or unsupervised, to try to identify what the subject is doing in each block. You can try to separate two blocks from each other, a particular block against the BASELINE (this is the moment when the subject is not doing anything in particular). You can use a part of two blocks for training and then try to predict the other parts.

## Dependencies

- python3.12
- pandas
- jupyter
- matplotlib