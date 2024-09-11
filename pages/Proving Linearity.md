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
  L(\begin{bmatrix}x \\ y\end{bmatrix})
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
  \begin{vmatrix}
  a & b & | & e \\
  c & d & | & f
  \end{vmatrix}
  
  * $a=0,c=0,d=0,e\neq 0$: Not invertible
  * $a=0,c=0,e=0,d\neq 0$: Not invertible
  * $a=0,c=0,d\neq 0$: Not invertible
  * $a=0,c=0,b\neq 0$: Not invertible
  
  $$a\neq0$$
  \begin{vmatrix}
  1 & \frac{b}{a} & | & \frac{e}{a} \\
  0 & d - \frac{cdb}{a} & | &