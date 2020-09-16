# Support vector machine
In this notebook, the following tasks are accomplished:
1. import and visualize moon data using bonnerlib library
2. train on a noisy data set by tuning soft margin SVM hyperparameters C and Gamma
3. visualize training and testing errors for varying values of C and gamma
4. discuss hyperparameters' effect on underfitting and overfitting

#### Visualize example moon_data. noise = 0
![moon_data_example](https://github.com/yanb514/ML_programming_assignments/blob/master/2_support_vector_machine/images/moon_data_example.png)

#### Visualize svm classifier on moon_data
![moon_data_boundary](https://github.com/yanb514/ML_programming_assignments/blob/master/2_support_vector_machine/images/moon_data_boundary.png)

#### Use grid search to find the best hyperparameters C and γ
![grid_search](https://github.com/yanb514/ML_programming_assignments/blob/master/2_support_vector_machine/images/grid_search.png)

#### Classifier trained on the best parameters
![best_parameters](https://github.com/yanb514/ML_programming_assignments/blob/master/2_support_vector_machine/images/best_parameters.png)

#### Error curve by varying C
![errors_vary_c](https://github.com/yanb514/ML_programming_assignments/blob/master/2_support_vector_machine/images/errors_vary_c.png)

#### Decision boundaries by varying C
![contour_vary_c](https://github.com/yanb514/ML_programming_assignments/blob/master/2_support_vector_machine/images/contour_vary_c.png)

#### Error curve by varying γ
![error_vary_gamma](https://github.com/yanb514/ML_programming_assignments/blob/master/2_support_vector_machine/images/error_vary_gamma.png)

#### Decision boundaries by varying γ
![contour_vary_gamma](https://github.com/yanb514/ML_programming_assignments/blob/master/2_support_vector_machine/images/contour_vary_gamma.png)

Discussion: C is introduced to tradeoff between maximizing margin and minimizing the training error. Clearly as shown in the figures above, the margin decreases as C increases as teh decision boundary is better at seperating training examples correctly. On the other hand, a low C value is shown as a simplier decision boundary, as a cost of underfit. C is a regularization parameter that controls overfitting.

Intuitively, when  γ  is too small, the model becomes over simplified and is not able to capture the complexity of the data set. On the other hand, when  γ  is too large, more samples are selected as the support vectors, and the model becomes too complex and overfits the data.  γ  is the inverse of the radius of support vectors, and can be seen as a way to incorporate more complexity of the model.
