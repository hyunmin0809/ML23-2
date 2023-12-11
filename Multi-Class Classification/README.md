# ML23-2

Machine Learning 2023-2

## Experiment setting

The experimental setup replicates the default environment provided by Colab.

- RAM: 12.7GB
- Disk: 107.7GB

Size of Data:

- 19,000 samples for monitored data
- 10,000 samples for unmonitored data

## Before execute code in google colab, file below should be prepared under 'content/drive/MyDrive/'

1. unmon_standard10.pkl
2. mon_satdard.pkl
3. feature/
   - data_arrays_1.npz
   - data_arrays_2.npz
   - data_arrays_3.npz
   - data_arrays_4.npz
   - unmon_data_1.npz
   - unmon_data_2.npz

- data_arrays file link:
  https://drive.google.com/drive/folders/18uhgWOfsojF_kvNgYs0DaaLXEtpzyuf7?usp=sharing
- npz files consists of features.

## multimodel

The result presents the outcome of training a model using seven features for binary classification. As the performance was unsatisfactory, we have decided to re-adjust the features in the secondary analysis of the multimodel approach.

## multimodel 2차

### 1. Load features from monitored & unmonitored data:

- load data_arrays_1npz to data_arrays_4.npz. File and unmon_data.npz File consists of features(X1, X3, X5, X6, X7, X8, X9, X11, X12, X14, X15, X16, X17) that have already preprocessed.

### 2. Create a total dataset by merging monitored and unmonitored data.

### 3. Utilize the functionalities provided by Random Forest to determine feature importance:

- Use both Gini impurity and Entropy methods.
- Calculate the average importance values from each method and exclude features that yield values averaging below 0.05.

### 4. Return to step 2 and reconstruct the dataset, excluding features with low importance.

### 5. Model training & testing(with model evaluation for each model, and hyperparameter tuning for each model)

- Logistic Regression (sampled data, pca, batch training)
- Decision Tree
- Random Forest
- KNN
- SVM (RBF, Linear)

## Conclusion

| Model               | Reason for Selection                                                    | Outcome                                                                                                                                                            |
| ------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Logistic Regression | Initially chosen due to high performance in binary classification       | Poor results. It struggled with imbalanced data and is presumed to be unsuitable for complex non-linear structures in the data.                                    |
| Decision Tree       | Considered for its ability to handle multiclass classification          | Limited effectiveness, possibly due to data imbalance. Additionally, the complexity of the data may exceed the model's capabilities.                               |
| Random Forest       | Selected for its feature importance and efficiency in handling features | Demonstrated good performance, but drawback includes longer processing time. Notably, it showed less sensitivity to parameter values.                              |
| KNN                 | Inspired by the mention of using KNN for fingerprinting hacking         | Poor performance, possibly attributed to data imbalance. In practical fingerprinting scenarios, the model might require weighted class handling to be appropriate. |
| SVM (RBF Kernel)    | Similar to logistic regression, chosen for promising results            | Successful operation, but tuning is crucial due to sensitivity to parameter values.                                                                                |
| SVM (Linear Kernel) | Selected for its feature importance and efficiency in handling features | Unimpressive results, akin to logistic regression. The low performance is attributed to the non-linear nature of the data.                                         |


## Note 
If you don't proceed in the correct order, you may encounter an error message like 

- "'DataFrame' object has no attribute 'ravel'." 

In such cases, you can resolve this by adding 'values.' before 'ravel'.


