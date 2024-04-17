## 1. Base Equations
$$\frac{dP}{dt} = (\beta(P)-S(p))P$$
$$\frac{dP}{dt} = (a - (bP + \frac{c}{P}))P$$
$$\text{or}$$
$$-bP^2+aP-c=0$$
$$\text{or}$$
$$bP^2-aP+c=0$$
$$\text{by the quadratic formula...}$$
$$P=\frac{a\pm\sqrt{a^2-4bc}}{2b}$$
$$\text{so}$$
$$M=\frac{a+\sqrt{a^2-4bc}}{2b}$$
$$m=\frac{a-\sqrt{a^2-4bc}}{2b}$$
$$M > m$$
$$\text{so}$$
$$\frac{dP}{dt}=-b(P-M)(P-m)$$
$$\text{so}$$
\begin{cases}
\frac{dP}{dt}=k(M-P)(P-m)\\
P(t_0) = P_0
\end{cases}
- ## 2. Sketching Representative Solutions
  **Equilibrium Solutions**:
  * P(t) = M
  * P(t) = m
  
  **Second Derivative of P**:
  $$\frac{d^2P}{dt^2}=k^2(M-P)(P-m)(m+M-2P)$$
  
  **Graphing**:
  ![image.png](../assets/image_1713367597573_0.png)
  
  *Remember to add the midpoint for the second derivative, and calculate the signs!*