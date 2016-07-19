### Model and Cost Function

* Supervised Learning: A model whereby you are given the "right answer" for each example in the training data.

* There are two types of supervised learning problem: regression and classification.

* In a regression problem, you want to predict a real-valued output.

* The other type of supervised learning model is called classification, where the aim is to predict discrete-valued output.

* In regression, the hypothesis refers to when you are mapping x features to y predictions.

* A linear regression model with one variable *(x)* is also know as a **univariate linear regression**.

* Cost function let's the machine figure out how to fit the possible line through our data. What values of the parameters gives the minimum error.

* The squared error cost function is one of the most commonly used cost functions for regression problems. There are other ways to calculate the objective cost function as well. 

* Contour plots are great to visualize the cost function since using the original hypothesis and it's parameters will generate a bow shape 3D figure that is difficult to read. 


### Parameter Learning

* Gradient Descent is used for minimizing the cost function and it is not only used in regression but also in other different types of machine learning techniques. 

* The derivative calculation on the Gradient descent algorithm is in charge of deciding what is the next value of the parameters to try to head towards the minimum. The derivative value is basically deciding in which direction we are going on the Cost function curve so as to decide what are the next values of the parameters. If the derivative produces a positive slope then direction to choose parameter value is towards the negative side, meaning a lower value of a parameter. Conversely, if the derivative has a negative slope, then the direction is to the right hand side, meaning a higher value of the parameter. 

* In the gradient descent algorithm if the alpha is too small, then the process will take baby steps towards the minimum, resulting in a slow algorithm. Conversely, if the alpha is big then gradient descent can overshoot the minimum (it may fail to converge or even diverge).

* Gradient descent for linear regression will have a bow shape and only has a global optima. 

* Batch gradient descent if when each step of gradient descent uses all the training examples. 

### Multivariate Linear Regression

* Feature scaling is the idea of making sure that the features are on a similar scale. This allows for the gradient descent algorithm to converge much faster as the contours take a more round shape. The idea is to have the values of the feature scaled in a way that they are in a closer range of numbers rather than a skewed range of values. For instance, have all features range from 0 to 1. 

* For sufficiently small learning rate, the cost function should decrease on very iteration. But if learning is too small, gradient descent can be very slow to converge. Similarity, if the learning rate is too big it will overshoot and more than likely fail to converge. 

* Feature scaling becomes even more important when wanting to fit a cubic or quadratic function through the points. 

### Computing parameters analytically

* Another option to minimize the cost function is to use normal equation, which uses straightforward derivatives to calculate for the values of parameters. 

* No feature scaling needed when using normal equation.

* Gradient Descent vs Normal Equation: Normal equation doesn't need to iterate and there is no need to choose a learning rate. Gradient descent works well when the number of features is large but normal equation is very slow when number of features is very large. So we can choose what algorithm to use based on the number of features in the training data set. 


* Feature scaling allows the gradient descent to make less iterations as the shape is less skewed. 

### Regularization

* In logistic regression, there are three ways that an algorithm might try to fit the data. Two of these fits are undesired (Underfitting and Overfitting). 

* **Underfitting** is when a straight line fitted on the data causing the model to have **high bias**, unable to fit the training set well. 

* **Overfitting:** If we have too many features, the learned hypothesis may fit the training set very well, but fail to generalize to new examples or the test data. This is also referred to as a model with **high variance**. This can sometimes can occur when we have too many features in the training dataset.

* Addressing overfitting:
  - Reduce number of features (manually and automatically)
  - Regularization (keep all features but reduce value of parameters; this works well with datasets that have a lot features that are all contributing to predict the labels.)

* Smaller values to the parameters produces smoother and simpler hypothesis curve, which is desired when having high-order degree polynomial hypothesis. This enable for less over-fitting. 

* If regularization parameter is too large, the algorithm results in under-fitting (fails to fit even the training dataset). This happens because the first parameters are also being penalized which produces a hypothesis to be equal or close to the first parameter, which renders an arbitrary straight line through the data. In other words, the model has a preconception that the hypothesis relies heavily on the first parameter. 

* In the normal equation, regularization also takes care of the non-invertible issue when there may be more features than examples in a training dataset.

* Simple logistic regression is only able to find a linear decision boundary. For such cases where the data needs a non-linear hypothesis curve, one way to solve this is to use higher order polynomial features with regularization. 

* It is important to note that when implementing regularization, the first parameter is left untouched as modifying introduce some problem when creating the decision boundary.




