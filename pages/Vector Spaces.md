#### General Definition
A collection of vectors, where there exists one zero vector. 
Each vector $v$ has a sibling $sv$ (where $s$ is some scalar).
Each vector pair $u,v$ must produce another vector $u+v$.
- ### Basis Vectors
  A choice of n vectors $b_1,b_2,\ldots,b_{n}$. It may be that an arbitrary vector $v$ can be written as $v=s_1,b_1+,\cdots,+s_{n}b_{n}$. In which case, vector **spans** the vector space.
  
  For example, in $\mathbb{R}^2$, with $\left(1,1\right),\left(1,-1\right),\left(-1,1\right)$:
  $$\left(x,y\right)=s_1\left(1,1\right)+s_2\left(1,-1\right)+s_3\left(-1,1\right)$$
  
  In this case, it becomes immediately apparent that it's not going to work.
  For example,
  $$\left(-1,1\right)=a\left(1,1\right)+b\left(1,-1\right)$$
  $$\text{or}$$
  $$\left(-1,1\right)=\left(0\right)\left(1,1\right)+\left(-1\right)\left(1,-1\right)$$
  
  As a result, we derive that a basis is a collection of vectors that **span** the vector space but has **no redundant vectors**.
- ### I have no idea?
  All algebraic laws must be satisfied:
  * $0+v=v$
  * $v+w=w+v$
  * $1v=v$
  * $