<h2> <b> Objective:<br></h2>
The main objective of the project is to identify the employees leaving the organization<br>
The primarily identifying the factors influencing the leaving the organisation<br>
**Midterm Project**

**dataset** - employee_departure_dataset https://drive.google.com/file/d/1XoEt8xC_HCOxofrmFC0Mu_W2oHnfOt9z/view?usp=drive_link

***Steps to be followed:***
1. EDA
2. Feature Engineering
3. Create multiple models
4. Perform cross validation
5. Create pipelines
6. Evaluate models
7. Hyperparameter selection/tuning

## Choosing the Right Metric
- Recall: Indicates how well the model identifies employees who are actually leaving.
- Precision: Shows how accurately the model flags employees as leaving when they are actually staying.

<b>Between the two, we prioritize recall over precision due to the business impact of incorrectly predicting an employee as staying when they are actually planning to leave.</b>

## Models Used:
KNN Model<br>
Random Forest <br>
Decision Tree <br>

### Inference:
#### The model demonstrates a strong balance between precision and recall, with especially high recall for identifying employees likely to leave.

### Best Model ?

##### Among the three models tested (Random Forest, Decision Tree, and KNN), the Decision Tree model (with parameters 'criterion': 'entropy', 'max_depth': 10, 'min_samples_leaf': 1, 'min_samples_split': 2) performs the best based on:

##### - Highest Recall (94.6%): This model effectively captures nearly all employees who are actually leaving, which is crucial for our objective.
##### - Balanced Performance: It maintains a reasonable precision (74.6%) and F1-score for the "leaving" class, making it reliable without too many false alarms.
##### - Consistent Accuracy: With a mean accuracy of 88.4%, it performs consistently well across different folds in K-Fold Cross-Validation, indicating good generalization.

##### Overall, the Decision Tree model’s high recall and balanced metrics make it the most suitable model for predicting employee turnover, aligning well with the business goal of identifying potential leavers accurately.
