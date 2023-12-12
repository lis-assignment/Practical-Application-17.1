# Practical Application Assignment17.1   
#### Comparing Classifiers   

### Link to the notebook   
[Practical Application Assignment notebook](https://github.com/lis-assignment/Practical-Application-17.1/blob/main/prompt_III.ipynb)   

**In this project, I use a dataset from a Protugese banking institution and is a collection of the result of multiple marketing campains**

#### Goal
to compare the performance of the classifiers we encountered in this section, namely K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines.  We will utilize a dataset related to marketing bank products over the telephone.

#### Model for comparision
* KNN 
* LogisticRegressions
* Decision Trees
* Support Vector Machine

#### Valuable column for model training
* age: the customer's age, int
* job: type of job, object
* marital: marital status of the customer, object
* education: education levels of the customer, object
* default: has creadit in default, object
* housing: has house loan, object
* loan: has personal loan, object

#### Steps:
1. convert object datatype to 1 and 0 using get_dummy from pandas library
2. Scale the data using Standard Scaler because the age has more weight than the other columns
3. Setting up a baseline at 50% to compare the models
4. Testing 4 different classification models in their default stage
5. Get the accuracy score for both training dataset and testing dataset
6. Using `GridSearchCV` to find the best hyper parameters
7. Using the hyperparameter to enhance the accuracy of the models

#### Findings
| Model | Train Time | Train Accuracy | Test Accuracy |
| ----- | ---------- | -------------  | -----------   |
| LR    |0.056    |.887     |.885     |
| knn    |0.020    |.879     |.815     |
| DTree    |0.112    |.917     |.862     |
| SVM    |24.35    |.888     |.885     |   

* SVM takes much more time to train while KNN is the fastest Model to fit
* Decision Tree has the highest Train accuracy
* Both SVM and Logistic Regression has the highest Test accuracy
* Logistic Regression seems to be the best Model for this particular dataset because this dataset has only two classes
* Most of the classific model performs better than expectations

#### Enhance the model
* by using `GridSearchCV`, maching realize the best K number for KNN is 50
* Changing `n_neighbors` hyperparameter the confusion matrix get better result

#### Future work
* `GridSearchCV` takes too long to run, I tried to iterate through from 1 to the `len` of the dataset but I failed, it takes more than 2 hours to run the model and the CPU rate goes to 797%.
* I will enhance my skill to understand more about `GridSearchCV` and create a better dataset for the next training

#### Contact
liulujunjin@gmail.com

## Thank you 