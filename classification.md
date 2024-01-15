# Classification

Classification is creating a model that will make a prediction given specific inputs.

Binary classification (true/false or 1 or 0) examples:

* Detecting spam email
* Fraudulent credit card transaction
* Is a tumor malignant

## Logistic Regression Model
Used for classification problems



  $$f_{\mathbf{w},b}(\mathbf{x}^{(i)}) = g(\mathbf{w} \cdot \mathbf{x}^{(i)} + b)$$

  where $g(z)$ is known as the ***sigmoid function*** and it **maps all input values to values between 0 and 1**:

  $$g(z) = \frac{1}{1+e^{-z}}$$
  and $\mathbf{w} \cdot \mathbf{x}$ is the vector dot product:
    
  $$\mathbf{w} \cdot \mathbf{x} = w_0 x_0 + w_1 x_1$$

We interpret the output of the model ($f_{\mathbf{w},b}(x)$) as the probability that $y=1$ given $\mathbf{x}$ and parameterized by $\mathbf{w}$ and $b$.

Therefore, to get a final prediction ($y=0$ or $y=1$) from the logistic regression model, we can use the following heuristic -

  if $f_{\mathbf{w},b}(x) >= 0.5$, predict $y=1$
  
  if $f_{\mathbf{w},b}(x) < 0.5$, predict $y=0$

### Cost function
***Squared error loss*** is not appropriate for logistic regression.

Using the ***logistic loss function***

>**Loss** is a measure of the difference of a single example to its target value while the  
**Cost** is a measure of the losses over the training set

$loss(f_{\mathbf{w},b}(\mathbf{x}^{(i)}), y^{(i)})$ is the cost for a single data point, which is:

$$ J(\mathbf{w},b) = \frac{1}{m} \sum_{i=0}^{m-1} \left[ loss(f_{\mathbf{w},b}(\mathbf{x}^{(i)}), y^{(i)}) \right]$$

### Sigmoid function
When z is a large positive number in the context of the sigmoid function, $\sigma(z)$, the function tends to approach its asymptotic value of 1. The sigmoid function, commonly denoted as $\sigma(z) = \frac{1}{1 + e^{-z}}$, is characterized by an "S"-shaped curve.

As the value of z becomes increasingly positive, the exponential term $e^{-z}$ in the denominator of the sigmoid function becomes very small, approaching zero. This makes the denominator of the function very close to 1, and thus $\sigma(z)$ itself becomes close to $$\frac{1}{1 + 0} = 1$$

Therefore, for large positive values of z, $\sigma(z)$ will be very close to 1, although it never actually reaches 1. This is a key property of the sigmoid function, making it useful for applications where a smooth transition between two states (0 and 1) is desirable, such as in logistic regression in machine learning.

## Decision Boundary
Is the border that defines what outcome the prediction will have

Simple exmple for logistic regression model

![Decision boundary](/slides/decision_boundary.png)

