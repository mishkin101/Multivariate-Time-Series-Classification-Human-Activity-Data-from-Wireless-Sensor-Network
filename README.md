# Multivariate-Time-Series-Classification-Human-Activity-Data-from-Wireless-Sensor-Network

This project tackles multivariate time-series classification using the [UCI AReM](https://archive.ics.uci.edu/dataset/366/activity+recognition+system+based+on+multisensor+data+fusion+arem) human-activity dataset collected from a wireless sensor network (six synchronized signals per instance, 480 samples each).

### Worflow
1. organize time series data into train/test folders
2. engineer time-domain features per signal—min, max, mean, median, quartiles, standard deviation, zero-crossings, cross-correlation, peak/trough counts;
3. segment each instance into ℓ equal chunks and extract the same features within each segment to capture within-instance dynamics;
4. build and compare classifiers for both a binary task (bending vs. non-bending) and multiclass activity recognition.

### Binary Classification Comparison: 
- a p-value-guided RFE + logistic regression pipeline
- 1-penalized logistic regression that performs embedded feature selection.
 
### Multiclass Classification Comparison:
- evaluate multinomial logistic regression (L1) and Naive Bayes variants, including a Gaussian NB + PCA reduction to mitigate feature correlation. 

### Comparison
Model selection uses nested/outer cross-validation and test-set evaluation with ROC/AUC, accuracy, and confusion matrices.
