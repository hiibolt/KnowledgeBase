## 2x2
\begin{equation}
\frac{1}{ad-bc}\begin{bmatrix}a & b \\ c & d\end{bmatrix}
\end{equation}
- ## 3x3
  For a matrix like:
  \begin{bmatrix}
  a & b & c \\
  d & e & f \\
  g & h & i
  \end{bmatrix}
  
  \begin{cases}
  ax+by+cz=1 \\
  dx+ey+fz = 0 \\
  gx+hy+iz = 0
  \end{cases}
  
  ...and one for each basis vector! Instead, we'll set up a 2D version of Gaussian elimination.
  
  Let's consider that for the $2\cdot2$ version first.
  
  \begin{vmatrix}
  a & b & | & 1 & 0 \\
  c & d & | & 0 & 1
  \end{vmatrix}
  $$\text{or}$$
  
  \begin{vmatrix}
  1 & b/a & | & 1/a & 0 \\
  0 & d - bc/a & | & -c/a & 1
  \end{vmatrix}
  $$\text{or}$$
  
  \begin{vmatrix}
  1 & 0 & | & \frac{1}{a}-\frac{b}{a}(\frac{-c/a}{d-bc/a}) & \frac{-b}{a}(\frac{1}{d-bc/a}) \\
  0 & 1 & | & \frac{-c/a}{d-bc/a} & \frac{1}{d-bc/a}
  \end{vmatrix}$$
  
  \text{or}$$
  \begin{vmatrix}
  1 & 0 & | & \frac{1}{a}-\frac{b}{a}(\frac{-c/a}{d-bc/a}) & \frac{-b}{a}(\frac{1}{d-bc/a}) \\
  0 & 1 & | & \frac{-c/a}{d-bc/a} & \frac{1}{d-bc/a}
  \end{vmatrix}