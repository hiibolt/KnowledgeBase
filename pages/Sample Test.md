## 1 - Extinction Problem
\begin{cases}
P(t), t \geq 0\\
\beta(P) = 0.2P^{\frac{1}{2}}\\
\delta(P) = 0.1P^{\frac{1}{2}}\\
\end{cases}

\begin{cases}
\frac{dP}{dt} = (\beta(P)-\delta(P))P\\
P(0) = 100
\end{cases}

We are aiming to find **Doomsday** (when the population approaches infinity).

$$\frac{dP}{dt}=0.1P^{\frac{3}{2}}$$
$$\text{or}$$
$$P^{\frac{-1}{2}}=\frac{1}{-20}t+C$$
$$C=\frac{1}{10}$$
$$\text{so}$$
$$P=(\frac{-20}{-t+2})^2=\frac{400}{(2-t)^2}$$

We can see that a value approaching $$t = 2$$ from the left is our $$T$$, or Doomsday.
- ## 2 - Dimensional Analysis
  \begin{cases}
  P - ML^2T^{-3}\\
  \rho - ML^{-3}\\
  \mu - ML^{-1}T^{-1}\\
  D - L\\
  v - LT^{-1}
  \end{cases}
  We want to find power ($P$) in terms of the other variables.
  $$P^a\rho^b\mu^cD^dv^e=M^0L^0T^0$$
  
  \begin{cases}
  a+b+c = 0\\
  2a-3b-c+d+e = 0\\
  -3a-c-e = 0\\
  \end{cases}
  **Resulting basis vectors**:
  \begin{cases}
  a = a\\
  b = -a - c\\
  c = c\\
  d = -2a - c\\
  e=-3a-c
  \end{cases}
  \begin{equation}\begin{bmatrix}a\\b\\c\\d\\e\end{bmatrix} = a\begin{bmatrix}1\\-1\\0\\-2\\-3\end{bmatrix} + b\begin{bmatrix}0\\-1\\1\\-1\\-1\end{bmatrix}\end{equation}
  **Our complete set of dimensionless products**:
  $$\Pi_1=\frac{P}{\delta D^2V^3}$$
  $$\Pi_2=\frac{\mu}{\delta D v}$$
  By the Buckingham Theorem, there exists a function $$f$$ such that $$f(\Pi_1, \Pi_2) = 0$$.
  
  Then, by the Implicit Function Theorem, there is another function $$h$$ such that $$\Pi_1 = h(\Pi_2)$$.
  
  **Final solution**:
  $$P=\delta D^2v^3h(\frac{\mu}{\delta Dv})$$
- ## 3 - Graphical Solutions
  \begin{cases}
  \frac{dP}{dt} = (1-P)(P-3)\\
  P(0) = P_0 \geq 0
  \end{cases}
  
  **Equilibrium Solutions**:
  $$\frac{dP}{dt} = 0\text{ when }P = 1, 3$$
  
  We must find $$\frac{d^2P}{dt^2}$$ now.
  $$\frac{d^2P}{dt^2} = $$