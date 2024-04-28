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
  $$\frac{P-m}{M-P}=\frac{P_0-m}{M-P_0}e^{k(M-m)(t-t_0)}=A(t)$$
  $$\text{or}$$
  $$P+PA(t)=m+MA(t)$$
  $$\text{or}$$
  $$P=\frac{m+MA(t)}{1+A(t)}=\frac{m+M(\frac{P_0-m}{M-P_0}e^{k(M-m)(t-t_0)})}{1+\frac{P_0-m}{M-P_0}e^{k(M-m)(t-t_0)}}=\frac{M(P_0-m)+m(M-P_0)e^{-(M-m)k(t-t_0)}}{(P_0-m)+(M-P_0)e^{-(M-m)k(t-t_0)}}$$
- ## 4. 
  $$P(t) = \frac{M(P_0-m) + m(M-P_0)e^{-k(M-m)(t-t_0)}}{P_0-m+(M-P_0)e^{-k(M-m)(t-t_0)}}$$
  
  We must now find the value of $t$ where $P(t) = 0$ (aka $t^{*}$)
  
  Solve the following way for t:
  $$M(P_0-m)+m(M-P_0)e^{-k(M-m)(t-t_0)}=0$$
  $$\text{or}$$
  $$-k(M-m)(t-t_0)=\ln\frac{M(m-P_0)}{m(M-P_0)}$$
  $$\text{or}$$
  $$t^{*}=\frac{1}{-k(M-m)}\ln(\frac{M(m-P_0)}{m(M-P_0)})+t_0$$
  
  Next, lets determine the behavior of $P(t)$ as $t \rarr \infty$:
  $$P(t) = \frac{M(P_0-m) + m(M-P_0)e^{-k(M-m)(t-t_0)}}{P_0-m+(M-P_0)e^{-k(M-m)(t-t_0)}}$$
  $$\text{so}$$
  $$\lim_{t \rarr \infty}P(t) = \frac{M(P_0-m)}{P_0-m} = M$$
  
  Verifying our equilibrium solutions:
  $$\text{When }P(t) = m, \lim_{t \rarr \infty}P(t) = \frac{M(m-m) + m(M-m)e^{-k(M-m)(t-t_0)}}{m-m+(M-m)e^{-k(M-m)(t-t_0)}}$$
  $$\text{so (lots of cancellations)}$$
  $$= m$$
  $$\text{When }P(t) = M, \lim_{t \rarr \infty}P(t) = \frac{M(M-m) + m(M-M)e^{-k(M-m)(t-t_0)}}{M-m+(M-M)e^{-k(M-m)(t-t_0)}}$$
  
  
  $$\text{so (lots of cancellations)}$$
  $$= M$$
- ## 5.
  $$P(t)\geq \frac{m+M}{2}, t \geq t_0$$
  
  Substitute $$P_0=\frac{m+M}{2}$$ into the equation from 4 and simplify!
  
  **Why is** $$P(t)\geq P_0=\frac{m+M}{2}$$ **for all** $$t \geq t_0$$?
  Refer to #2 and the graph, and also recall that $$P'(t) > 0\text{ if }P_0=\frac{m+M}{2}$$
  @ $$\frac{m+M}{2}, P(t) > P_0$$
  
  $$P(t) = \frac{M(P_0-m) + m(M-P_0)e^{-k(M-m)(t-t_0)}}{P_0-m+(M-P_0)e^{-k(M-m)(t-t_0)}}$$
  $$\text{or}$$
  $$P(t) = \frac{M(\frac{m+M}{2}-m) + m(M-\frac{m+M}{2})e^{-k(M-m)(t-t_0)}}{\frac{m+M}{2}-m+(M-\frac{m+M}{2})e^{-k(M-m)(t-t_0)}}$$
  $$\text{or}$$
  $$P(t) = \frac{M(\frac{M-m}{2}) + m(\frac{M-m}{2})e^{-k(M-m)(t-t_0)}}{\frac{M-m}{2}+(\frac{M-m}{2})e^{-k(M-m)(t-t_0)}}$$
  $$\text{or}$$
  $$P(t) = \frac{M+me^{-k(M-m)(t-t_0)}}{1+e^{-k(M-m)(t-t_0)}}$$
- ## 6.
  There exists a table with P, \beta(P), and P\delta(P).
  
  We must use [[3.3 LSM]] to estimate \beta(P) and P\delta(P).
  
  $\beta(P) = a \rarr$  find the average of the values of \beta(P)
  $\delta(P)=bP+\frac{C}{P}\rarr P\delta(P)=bP^2+C$, find *b* and *c* using the values of the table
  
  Take the partial derivative of S 
  $S(b,c)\sum_{i=1}^{b}[(P\delta)_i-bP_i^2-c]^2$ - Use excel or a calculator
  
  **Final Values**:
  * $$a = \frac{\sum_{i=1}^n\beta(P)_i}{n}=0.4983R$$
  * $$b = 2x10^{-5}$$
  * $$c = 2,000$$
  
  **Finding m, M if we know a, b, c**:
  (plug in the equations form m, M from #1)
  
  **Results**:
  * m=5028.81205
  * M=19889.8929
- ## 7.
  $$P_0=4000$$
  We must decide if $$P_0$$ if within (0, m), (m, M), or (M, \infty). (based on problem #2, fish will die, survive, die)
  
  Because this initial value is lower than $$m$$, the population will die. This requires 8460 fish to stay alive.
- ## 8.
  If $$P_0 = 4000 < m < \frac{m+M}{2}$$, how many fish does the local government need to get to the safety level?
  
  $$\frac{m+M}{2}-4000 > 0$$
  
  **Maximum Fishing Per Year**:
  If the fishing is allowed once a year, $$P(1) - \frac{m+M}{2}$$
  If the fishing is allowed twice a year, $$(P(\frac{1}{2}) - \frac{m+M}{2})2$$
  If the fishing is allowed montly, $$(P(\frac{1}{12}) - \frac{m+M}{2})12$$
  
  **Final Values**:
  * 1 Year - 1096
  * 1 Month - 1112
  * 1 Day - 1340