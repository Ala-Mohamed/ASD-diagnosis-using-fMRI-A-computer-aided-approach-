# ASD-diagnosis-using-fMRI-A-computer-aided-approach-

This project aims to address the challenges of diagnosing the Autism Spectrum Disorder (ASD) 
accurately, which is a neurodevelopmental disorder that affects social activity, communication, and 
repetitive behaviour. The current diagnosis depends on the subjective behavioural assessment, and there 
is no established medical test. Misdiagnosis can raise significant issues and make the patient more 
susceptible to depression, self-harm, and eating disorders. Recent studies suggest that ASD is associated 
with changes in brain organization and neural connectivity, revealing a potential diagnosis using brain 
image data such as functional magnetic resonance imaging (fMRI). This project suggests that using 
Machine learning (ML) and Deep learning (DL) to analyze this functional brain network imaging data 
can be a promising method to distinguish between typical developing (TD) controls and ASD persons. 
This study proposes an automated diagnostic method utilizing the time series data for regions of interest 
identified by Bootstrap Analysis of Stable Cluster (BASC) atlas for 340 subjects, including 170 subjects 
diagnosed. The methodology implies constructing a connectivity pairwise matrix using Spearman 
correlation and Transfer entropy matrices. The Spearman correlation matrix for each subject will be used 
with ML models. For the DL, Transfer entropy (TE) matrices will be used as a connectivity matrix, then 
the sliding window technique to analyze functional brain dynamics and long short-term memory will be 
used for classification. The results show .72 and .75 accuracy for the support vector machine and logistic 
regression, respectively. SHAP value analysis indicating key brain regions contributing to classification, 
such as Left-Fusiform-Left-PrimMotor. The LSTM model and sliding window technique require higher 
computational complexity to proceed.  This project investigated the potential use of ML and DL for ASD 
diagnosis, and indicated the brain regions contributing to this disorder, while highlighting the need for 
further refinement of DL approaches to capture dynamic brain interactions effectively.  

Initially appeared on
[gist](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2). But the page cannot open anymore so that is why I have moved it here.

### Prerequisites
**numpy**: Essential for numerical operations, especially with arrays and matrices, which are fundamental to machine learning and data processing.
**scipy**: Provides scientific computing tools, including spearmanr for correlation analysis.
**scikit-learn**: The primary machine learning library for:
**model_selection**: train_test_split, GridSearchCV
**svm**: SVC (Support Vector Classifier)
**linear_model**: LogisticRegression
**metrics**: accuracy_score, roc_auc_score, precision_score, recall_score, confusion_matrix, roc_curve
**preprocessing**: StandardScaler
**pipeline**: Pipeline
**impute**: SimpleImputer
**matplotlib**: Used for creating static, interactive, and animated visualizations, specifically plt for plotting ROC curves, SHAP plots, etc.
**TensorFlow**: The core deep learning framework, specifically:
tensorflow.keras.models: Sequential
tensorflow.keras.layers: LSTM, Dense, Dropout
**pyinform**: A Python package for information-theoretic measures, specifically transfer_entropy.
**shap**: SHapley Additive exPlanations, a library for explaining the output of machine learning models.
## Data and Running 
The time series matrices were obtained from https://www.nature.com/articles/s41598-023-34650-6#Sec18 supplementary material 

## License

This project is licensed under the [CC0 1.0 Universal](LICENSE.md)
Creative Commons License - see the [LICENSE.md](LICENSE.md) file for
details




