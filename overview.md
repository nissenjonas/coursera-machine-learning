# Overview

* Choose model 
  * Linear Regression
  * Polynomial Regression  
* Identify Cost Function
  * Loss value is the cost for the individual training inputs (x1, ... xi)
  * Cost value is the avearage loss value for an entire training set (total cost)
* Gradient decent (to fit model)
  * Identify learning rate
  * Feature scaling
  * Feature Engineering (Adding features based on other features)
  * Until convergence
  
<figure>
    <img src="./slides/2_function_terms.png" style="width:1000px;" >
</figure>

Fit the linear regression parameters $(w,b)$ to your dataset.
- The model function for linear regression, which is a function that maps from `x` (city population) to `y` (your restaurant's monthly profit for that city) is represented as 
    $$f_{w,b}(x) = wx + b$$
    

- To train a linear regression model, you want to find the best $(w,b)$ parameters that fit your dataset.  

    - To compare how one choice of $(w,b)$ is better or worse than another choice, you can evaluate it with a cost function $J(w,b)$
      - $J$ is a function of $(w,b)$. That is, the value of the cost $J(w,b)$ depends on the value of $(w,b)$.
  
    - The choice of $(w,b)$ that fits your data the best is the one that has the smallest cost $J(w,b)$.


- To find the values $(w,b)$ that gets the smallest possible cost $J(w,b)$, you can use a method called **gradient descent**. 
  - With each step of gradient descent, your parameters $(w,b)$ come closer to the optimal values that will achieve the lowest cost $J(w,b)$.
  

- The trained linear regression model can then take the input feature $x$ (city population) and output a prediction $f_{w,b}(x)$ (predicted monthly profit for a restaurant in that city).