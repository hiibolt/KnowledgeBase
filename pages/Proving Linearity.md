## Steps
$$L\left(x,y\right)=2x+3y$$
* 1.) $L(a(x,y)) = aL(x,y)$ for 
$$\text{or}$$
$$L\left(ax+ay\right)$$
$$\text{or}$$
$$L\left(ax,ay\right)=2\left(ax\right)+3\left(ay\right)$$
$$\text{or}$$
$$=a\left(2x+3y\right)$$
$$=aL\left(x,y\right)$$
* 2.) $L((x, y) + (x'+y'))$
$$F\left(\left(x,y\right)+\left(x^{\prime},y^{\prime}\right)\right)$$
$$=F\left(x+x^{\prime},y+y^{\prime}\right)$$
$$=\left(x+x^{\prime}\right)\left(y+y^{\prime}\right)$$
$$=xy+xy^{\prime}+x^{\prime}y+x^{\prime}y^{\prime}$$
- ## Three Primary Concepts
	- #### Onto
	  id:: 66e1e9fa-12b5-40a3-895a-e427b1ff3aa8
	  Each element in the range is realized $f(x)$ for some $x$
	- #### One-to-one
	  id:: 66e1ea14-8a47-43a0-86ba-4089d9062fe5
	  No pair in the domain goes to the same element in the range
	- #### Invertible
	  The function is both ((66e1e9fa-12b5-40a3-895a-e427b1ff3aa8)) and ((66e1ea14-8a47-43a0-86ba-4089d9062fe5))
- ## Is $\mathbb{R}^2 \rarr \mathbb{R}^2$ Invertible?
  \begin{equation}
  L(
  \begin{bmatrix}
  x \\ y
  \end{bmatrix}
  )
  = 
  \begin{bmatrix}
  a & b \\
  c & d
  \end{bmatrix}
  \begin{bmatrix}
  x \\ y
  \end{bmatrix}
  = 
  \begin{bmatrix}
  ax + by \\
  cx + dy
  \end{bmatrix}
  =
  \begin{bmatrix}
  e \\ f
  \end{bmatrix}
  \end{equation}
  $$\text{or}$$
  
  \begin{bmatrix}
  a & b & | & e \\
  c & d & | & f
  \end{bmatrix}
  
  * $a=0,c=0,d=0,e\neq 0$: Not invertible
  * $a=0,c=0,e=0,d\neq 0$: Not invertible
  * $a=0,c=0,d\neq 0$: Not invertible
  * $a=0,c=0,b\neq 0$: Not invertible
  
  $$a\neq0$$
  \begin{bmatrix}
  1 & \frac{b}{a} & | & \frac{e}{a} \\
  0 & d - \frac{cdb}{a} & | & f - \frac{ce}{a}
  \end{bmatrix}
  $$\text{or}$$
  \begin{bmatrix}
  1 & 0 & | & \frac{e}{a} - \frac{b}{a}(\frac{af-ce}{ad-c}) \\
  0 & 1 & | & \frac{af-ce}{ad-bc}
  \end{bmatrix}
  $$\text{or}$$
  \begin{bmatrix}
  1 & 0 & | & \frac{de-bf}{ad-bc} \\
  0 & 1 & | & \frac{af-ce}{ad-bc}
  \end{bmatrix}
  
  Therefore, we can conclude that, if $ad-bc\neq0$:
  \begin{cases}
  x = \frac{de-bf}{ad-bc} \\
  y = \frac{af-ce}{ad-bc}
  \end{cases}
  $\therefore$ there is a unique solution.
  
  What about when $ad-bc=0$?
  $$L\left(x\begin{bmatrix}1\\ 0\end{bmatrix}+y\begin{bmatrix}0\\ 1\end{bmatrix})\right)$$
  $$\text{or}$$
  $$L\left(x\begin{bmatrix}1\\ 0\end{bmatrix}\right) +L\left(y\begin{bmatrix}0\\ 1\end{bmatrix}\right)$$
  $$\text{or}$$
  $$xL\left(\begin{bmatrix}1\\ 0\end{bmatrix}\right) +yL\left(\begin{bmatrix}0\\ 1\end{bmatrix}\right)$$
  $$\text{and}$$
  $$L\left(\begin{bmatrix}1\\ 0\end{bmatrix}\right)=\begin{bmatrix}a \\ c\end{bmatrix}, 
   L\left(\begin{bmatrix}0\\ 1\end{bmatrix}\right) = \begin{bmatrix}b \\ d\end{bmatrix}$$
  
  $\therefore$ we can assume that the following is the inverse of any given $2x2$ matrix:
  \begin{equation}
  \frac{1}{ad-bc}\begin{bmatrix}d & -b \\ -c & a\end{bmatrix}
  \end{equation}
  
  So, for the functions:
  $$f:A\rightarrow B$$
  $$g:B\rightarrow A$$
  $$\therefore\left(g\circ f)(a)=a\right) \text{ and } (f \circ g)(b) = b$$