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
  Result:
  \begin{cases}
  a = a\\
  b = -a - c\\
  c = c\\
  d = -2a - c\\
  e=-3a-c
  \end{cases}
  \begin{equation}
  \begin{bmatrix}
  a\\
  b\
  \end{equation}