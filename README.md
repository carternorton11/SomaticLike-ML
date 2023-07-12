# SomaticLike-ML

### Introduction
This was a project to produce a machine-learning model to identify somatic cell contamination in sperm methylation data. 
This final model is hosted here: https://github.com/jenkins-lab-byu/Somatic_Cell_QC_Pipeline/tree/main/Somatic_Cell_ML_Pipeline

### Feature Identification
~1000 differentially methylated were selected from a USEQ sliding window analysis on our training set. I generated mean beta values at each of these regions for each sample, 
and plotted them on a clustermap.

![SLSFig4 2](https://github.com/carternorton11/SomaticLike-ML/assets/99043737/d78570df-92e8-4dbe-8024-365ba164a26f)

### Binarization
I established a cutoff for hyper/hypomethylation using mean methylation values from sperm samples in our training set. All samples were then assigned a "0" or "1" at each region,
depending on methylation value. 

### Model Training
I selected 521 blood and 521 semen samples as a training set. Recursive feature elimination using a logistic regression model selected the 250 most informative regions between the two sample groups. 
I then used Sample data at selected features to train a Random Forest, Logistic Regression, SVM, KNN, Neural Network, and GBC models. 

### Model Validation
I selected 100 normal sperm samples and 100 contaminated sperm samples as a validation set. sensitivity and specificity values were generated using all 6 machine learning models. Hyperparameters, including thresholds and model size, were tuned using these data.

### Model Testing
I used 4 pure and 12 contaminated samples (these were samples we processed and manually contaminated) as a testing set. All models were tested on these data. 

### Model Selection
All models showed excellent sensitivity or specificity, but the Logistic Regression model performed the best in validation and testing. This model is now published on the Jenkins' Lab GitHub. 




