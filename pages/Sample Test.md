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
  P\\
  d\\
  \rho, \mu