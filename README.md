# EEG-Analyzer

This repository aims to provide an introductory approach to EEG (Electroencephalography) signal processing, analysis, and visualization.

## Data

* Baseline: This part can be used to have negative examples of anything you want to detect. For example, if you want to detect changes when there is "imagination in violet colors," you extract features from that moment and from this one and try to build a classifier.
* Inhaling: Changes in low frequencies, where the movement of the diaphragm for inhaling is emphasized.
* Exhaling: Same as inhaling but emphasizing the movement of the diaphragm for exhaling.
* Taps: There should be some event with a certain peak in the signal. You can try to detect these peaks and see if there is anything.
* Mental Imagery: High frequencies of 20-50 Hz may appear. Increases in the power of these bands between this block and the baseline.
* Eyes Closed: There should be an increase in the specific frequency of 10 Hz relative to the baseline.

## Objetive

The objective is to implement an analysis of these data, exploratory, supervised, or unsupervised, to try to identify what the subject is doing in each block. You can try to separate two blocks from each other, a particular block against the BASELINE (this is the moment when the subject is not doing anything in particular). You can use a part of two blocks for training and then try to predict the other parts.

## Dependencies

- python3.12
- pandas
- jupyter
- matplotlib