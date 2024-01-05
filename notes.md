1) Model 
2) Cost Function
3) Gradient descent
4) Gradient for w
5) Gradient for b

***Linear Regression*** model : $f_{w,b}(x^{(i)})$, where the ***Model Parameters*** are $w$, $b$ 

$$f_{w,b}(x^{(i)}) = wx^{(i)} + b \tag{1}$$
$f_{w,b}(x^{(i)})$ 
$y^{(i)}$. 


The ***Cost Function***: $cost$, $J(w,b)$. calculates the cost for the ***Training Dataset*** where each entry is denoted as $x^{(i)},y^{(i)}$
$$J(w,b) = \frac{1}{2m} \sum\limits_{i = 0}^{m-1} (f_{w,b}(x^{(i)}) - y^{(i)})^2\tag{2}$$ 

***Gradient Descent*** is a process used to identify the lowest cost for parameters $w$, $b$ described as:

$$\begin{align*} \text{repeat}&\text{ until convergence:} \lbrace \newline
 w &= w -  \alpha \frac{\partial J(w,b)}{\partial w} \tag{3}  \newline 
 b &= b -  \alpha \frac{\partial J(w,b)}{\partial b}  \newline \rbrace
\end{align*}$$
where, parameters $w$, $b$ are updated simultaneously.  
The gradient is defined as:
$$

The ***Gradient*** is defined as 

$$
\begin{align}
\frac{\partial J(w,b)}{\partial w}  &= \frac{1}{m} \sum\limits_{i = 0}^{m-1} (f_{w,b}(x^{(i)}) - y^{(i)})x^{(i)} \tag{4}\\
  \frac{\partial J(w,b)}{\partial b}  &= \frac{1}{m} \sum\limits_{i = 0}^{m-1} (f_{w,b}(x^{(i)}) - y^{(i)}) \tag{5}\\
\end{align}
$$
