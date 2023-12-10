# ML23-2
Machine Learning 2023-2

## binary_classification.ipynb
### Before execute code in google colab, file below should be prepared under 'content/drive/MyDrive/' 
1. unmon_standard10.pkl
2. data_arrays_1.npz
3. data_arrays_2.npz
4. data_arrays_3.npz
5. data_arrays_4.npz
- data_arrays file link:
https://drive.google.com/drive/folders/1uKioGkU617hFeS1FDfxffH8nPRjaOSek?usp=sharing
- npz files consists of features.

## Steps
### 1.	Prepare features from unmonitored data: 
- directly extract features from unmon_standard10.pkl

### 2.	Load monitored data & transform to Dataframe: 
- load data_arrays_1npz to data_arrays_4.npz. File consists of features(X1, X5, X6, X7, X9, X12, X14) that have already been preprocessed. 

### 3.	Transform unmonitored data(at 1) to Dataframe.

### 4.	Make total data set: unmonitored data + monitored data

### 5.	Model training & testing(with model evaluation for each model, and hyperparameter tuning for each model except Naïve Bayes)
- Split dataset
-	Logistic Regression
-	Linear SVM
-	SVM with RBF
-	Naïve Bayes
-	Decision Tree
-	Overall model evaluation

### 6.	Classify unmonitored dataset with 5 models

# Conclusion
|Model|Reason for Selection|Outcome|
|------|---|---|
|Logistic Regression, Linear SVM|Effective if the dataset is linear|The completed tuning results indicate that a high C value leads to fitting excessively, causing overfitting, revealing that our data is non-linear. The accuracy was not bad.|
|SVM|Can improve generalization through hyperparameter tuning(C, gamma)|Result showed the second highest accuracy. Better than linear SVM.|
|Naive Bayes|Effective if the dataset satisfies assumption|The lowest accuracy.This reveals the data is nonlinear, with interactions or dependencies among features.|
|Decision Tree|Effective for multiple features|The best performance. The highest f1-score. Tuning was performed appropriately, avoiding overfitting.|
