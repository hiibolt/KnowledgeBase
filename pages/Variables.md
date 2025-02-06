### Random Variable
A function whose domain is the sample space S, and whose range is the set of real numbers
- ## Discrete Random Variable
  Uppercase $X$ is the *name* of the variable.
  Lowercase $x$ is the *possible numeric values* of $X$.
  
  The probability distribution is called the probability mass function, $pmf$, and has the following properties:
  $p(x)=P(X=x)=P(\text{all }s\in S:X(x)=x)$ for every $x\in\mathbb{R}$.
  
  To be a valid probability mass function, the following two properties must hold:
  * $\sum_xp(x)=1.00$
  * $p(x)\ge0$ for all values of $x$.
	- ### Example 1
	  Suppose that we toss a fair coin 3 times and observe the number of heads that appear. Let $x =$ the number of heads that appears in three tosses of a fair coin. Find the probability mass function of $X$.
	  
	  **Solution**:
	  $x =$ the # of heads observed in three tosses of a fair coin.
	  As such, the possible values of $x \rarr \{3,2,1,0\}$
	  
	  To find the probability mass function ($pmf$) of $x$, we need to list all possible values of $X$ and their corresponding probabilities.
	  
	  $$S=\{HHH,HHT,HTT,TTT,TTH,THH, HTH, THT\}$$
	  ..., since $x$ is a $rv$ whose domain is the sample space $S$.
	  
	  The probability of each possible flip sequence are:
	  $$P(0) = \frac{1}{8}=0.1250$$
	  $$P(1) = \frac{3}{8}=0.3750$$
	  $$P(2) = \frac{3}{8}=0.3750$$
	  $$P(3) = \frac{1}{8}=0.1250$$
	  
	  The $pmf$ of $x$ is given by:
	  \begin{equation}
	  p(x)=P(X=x)=
	  \begin{cases}
	  0.1250 \text{ for } x = 0 \\
	  0.3750 \text{ for } x = 1 \\
	  0.3750 \text{ for } x = 2 \\
	  0.1250 \text{ for } x = 3 \\
	  0 \text{ otherwise }
	  \end{cases}
	  \end{equation}
	  So:
	  |x|0|1|2|3|otherwise (o/w)|
	  |p(x)|0.1250|0.3750|0.3750|0.1250|0|
	  ...and this is a valid pmf because:
	  * $p(x) \ge 0 \forall x$
	  * $\sum_xp(x) = 1$
- ## Cumulative Distribution Function
  The cumulative distribution function, *CDF*, $F(x)$ of discrete random variable, *rv*, $X$ with pmf $p(x)$ is defined for every number $x$ with:
  $$F(x)=P(X\le x)=\sum_{y:y\le x}p(y)$$
	- ### Example 1
	  Considering the above example for coinflips:
	  $$F(0)=P(x\le 0)=0.125$$
	  $$F(1)=P(x\le 1)=0.500$$
	  $$F(2)=P(x\le 2)=0.8750$$
	  $$F(3)=P(x\le 3)=1.000$$
	  \begin{equation}
	  F(x) = 
	  \begin{cases}
	  0 \text{ if }x< 0\\
	  0.125 \text{ if }0\le x<1\\
	  0.500 \text{ if }1\le x<2\\
	  0.870 \text{ if }2\le x<3\\
	  1.000 \text{ if }3\le x
	  \end{cases}
	  \end{equation}
	  \begin{equation}
	  p(x) = 
	  \begin{cases}
	  0.125\text{ if }x=0\\
	  0.375\text{ if }x=1\\
	  0.375\text{ if }x=2\\
	  0.125\text{ if }x=3\\
	  0\text{ ow}
	  \end{cases}
	  \end{equation}
	- ### Example 2
	  |X|13.5|15.9|19.1|ow|
	  |p(x)|0.2|0.5|0.3|0|
	  
	  **Find the expected value of X**:
	  $$E(x) = \mu = \text{mean} = \sum xp(x)$$
	  $$\text{or}$$
	  $$=13.5(0.2)+15.9(0.5)+19.1(0.3)$$
	  $$E(x) = \mu = 16.380\text{ft}^3$$
	  
	  **Find** $E(X^2)$:
	  $$E(X^2)=\sum x^2p(x)$$
	  $$\text{or}$$
	  $$=(13.5)^2(0.2)+(15.9)^2(0.5)+(19.1)^2(0.3)=\dots$$ 
	  
	  **Find the variance and standard deviation of** $X$:
	  $$V(X)=E(X^2)-E(X)^2 =3.9936(\text{ft}^3)^2$$
	  $$\sigma = \sqrt{V(x)} = 1.9984\text{ft}^3$$
	  
	  **If the price of a freezer having capacity $X$ cubic feet is $25X - 8.5$, find the expected price paid by the next customer to buy a freezer**:
	  $$E(\text{price}) = E(25X-8.5) = 25E(X) - 8.5$$
	  $$\text{or}$$
	  $$=401.00$$
	  
	  **Find the variance and standard deviation of the price paid by the next customer**:
	  $$V(p) = V(25X-8.5)=25^2V(X)=\$^22496.00$$
	  $$\sigma_p=\sqrt{V(p)} = \$49.96$$
- ## Variance and Standard Deviation
  $$Var(X) = \sigma^2 = E(X^2)-E(X)^2$$