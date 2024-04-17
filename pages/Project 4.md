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
- ## 3. Initial Value Problem
  \begin{cases}
  \frac{dP}{dt} = k(M-P)(P-m) \text{, (solve the IVP, as the DE is seperable)}\\
  P(t_0) = P_0
  \end{cases}
  
  **Solving**:
  $$\int\frac{dP}{(M-P)(P-m)}dP=\int kdt = kt+C$$
  $$\text{or (partial fractions)}$$
  $$A=B=\frac{1}{M-m}$$
  $$\frac{1}{M-m}(-\ln|M-P|+\ln|P-m|)$$
  $$\text{or}$$
  $$\ln|\frac{P-m}{M-P}|=(M-m)kt+C$$
  $$C=\ln|\frac{P_0-m}{M-P_0}|-(M-m)kt_0$$
  $$\text{so}$$
  $$\ln|\frac{P-m}{M-P}|=(M-m)kt+\ln|\frac{P_0-m}{M-P_0}|-(M-m)kt_0$$
  $$\text{or}$$
  $$\frac{P-m}{M-P}=\frac{P_0-m}{M-P_0}e^{k(M-m)(t-t_0)}$$
  $$\text{(solve for P, let the right side equal A(t))}$$
- ## 4. 
  $$P(t) = \frac{M(P_0-m) + m(M-B)e^{-k(M-m)(t-t_0)}}{P_0-m+(M-P_0)e^{-k(M-m)(t-t_0)}}$$
  
  We must now find the value of $t$ where $P(t) = 0$ (aka $t^{*}$)
  
  Solve the following way for t:
  $$M(P_0-m)+m(M-P_0)e^{-k(M-m)(t-t_0)}=0$$
  $$\text{or}$$
  $$-$$