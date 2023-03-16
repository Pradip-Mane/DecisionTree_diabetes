# DecisionTree_diabetes


- Pima Indians Diabetes Database

- Number of Instances: 768

- Number of Attributes: 8 plus class

### Columns Description:

- Number of times pregnant
- Plasma glucose concentration a 2 hours in an oral glucose tolerance test
- Diastolic blood pressure (mm Hg)
- Triceps skin fold thickness (mm)
- 2-Hour serum insulin (mu U/ml)
- Body mass index (weight in kg/(height in m)^2)
- Diabetes pedigree function
- Age (years)
-Class variable (0 or 1) (class value 1 is interpreted as "tested positive for diabetes")

## Steps

### 1. import Libraries 

### 2. Load Dataset 

### 3. Data Pre-Processing 

### 4. Split the data

### 5. Train The DT Classification Model

### 6. Evaluate the Performance with diffrent Hyperparameter 
- Default Hyperparameter

    - Prediction on test data

                    ****** prediction on test data *******
                    Confusion Matrix
                    [[75 21]
                    [13 45]]
                    ---------------------------------------------------
                    Classification Report
                                precision    recall  f1-score   support

                            0       0.85      0.78      0.82        96
                            1       0.68      0.78      0.73        58

                        accuracy                        0.78       154
                    macro avg       0.77      0.78      0.77       154
                    weighted avg    0.79      0.78      0.78       154


     - prediction on train data

                    ****** prediction on train data *******
                    Confusion Matrix
                    [[404   0]
                    [  0 210]]
                    ---------------------------------------------------
                    Classification Report
                                precision    recall  f1-score   support

                            0       1.00      1.00      1.00       404
                            1       1.00      1.00      1.00       210

                    accuracy                            1.00       614
                    macro avg       1.00      1.00      1.00       614
                    weighted avg    1.00      1.00      1.00       614

* Note: as here model works well on train data but not so well on test data it is a **overfitting** situation
- Plot The Decision Tree

**Note:**

  * Complex model =====> Overfitting
  * in above tree it is clear that tree has more depth, andmore depth means model is complex so there is **Overfitting** occurs
  * to overcome this Overfitting we need set depth of model tree using **max_depth** parameter 
  * but it should not be very less else there is **Underfitting** Problem occurs
  * Therefor the optimal value of max_depth is needed 

- max_depth=5

    - prediction on test data

                        ****** prediction on test data *******
                        Confusion Matrix
                        [[82 14]
                        [19 39]]
                        ---------------------------------------------------
                        Classification Report
                                    precision    recall  f1-score   support

                                0       0.81      0.85      0.83        96
                                1       0.74      0.67      0.70        58

                         accuracy                           0.79       154
                        macro avg       0.77      0.76      0.77       154
                        weighted avg    0.78      0.79      0.78       154

    - prediction on train data

                        ****** prediction on train data *******
                        Confusion Matrix
                        [[362  42]
                        [ 61 149]]
                        ---------------------------------------------------
                        Classification Report
                                    precision    recall  f1-score   support

                                0       0.86      0.90      0.88       404
                                1       0.78      0.71      0.74       210

                         accuracy                           0.83       614
                        macro avg       0.82      0.80      0.81       614
                        weighted avg    0.83      0.83      0.83       614


- max_depth= 4
       - prediction on test data

                        ****** prediction on test data *******
                        Confusion Matrix
                        [[81 15]
                        [20 38]]
                        ---------------------------------------------------
                        Classification Report
                                    precision    recall  f1-score   support

                                0       0.80      0.84      0.82        96
                                1       0.72      0.66      0.68        58

                         accuracy                           0.77       154
                        macro avg       0.76      0.75      0.75       154
                        weighted avg    0.77      0.77      0.77       154



        - prediction on train data

                        ****** prediction on train data *******
                        Confusion Matrix
                        [[345  59]
                        [ 64 146]]
                        ---------------------------------------------------
                        Classification Report
                                    precision    recall  f1-score   support

                                0       0.84      0.85      0.85       404
                                1       0.71      0.70      0.70       210

                         accuracy                           0.80       614
                        macro avg       0.78      0.77      0.78       614
                        weighted avg    0.80      0.80      0.80       614


- max_depth=3

        - prediction on test data

                        ****** prediction on test data *******
                        Confusion Matrix
                        [[90  6]
                        [33 25]]
                        ---------------------------------------------------
                        Classification Report
                                    precision    recall  f1-score   support

                                0       0.73      0.94      0.82        96
                                1       0.81      0.43      0.56        58

                         accuracy                           0.75       154
                        macro avg       0.77      0.68      0.69       154
                        weighted avg    0.76      0.75      0.72       154




        - prediction on train data

                        ****** prediction on train data *******
                        Confusion Matrix
                        [[369  35]
                        [111  99]]
                        ---------------------------------------------------
                        Classification Report
                                    precision    recall  f1-score   support

                                0       0.77      0.91      0.83       404
                                1       0.74      0.47      0.58       210

                        accuracy                            0.76       614
                        macro avg       0.75      0.69      0.71       614
                        weighted avg    0.76      0.76      0.75       614


- Out of all max_depth=5 gives a optimal model so we will use that model for deployment

### 7. Pickling of Model
 
### 8. Model Deployment on render
1. README file
2. requirements.txt
3. app.py
4. style.css
5. main.html
6. Dockerfile
7. main.yaml

### 9. Deploy on Render