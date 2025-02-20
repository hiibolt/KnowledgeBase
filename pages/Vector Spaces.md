## General Definition
A real *vector space* on a set $V$ on a set of elements for which there are two operations - $\oplus$ and $\odot$ - defined with the following properties, where elements of $V$ are written with arrows worn as hats.

**For all** $\bold{\vec{u}, \vec{v}, \vec{w} \in V}$:
* **(a)** $\vec{u}, \vec{v} \in V \rarr \vec{u}+\vec{v}\in V$ (closed under \oplus, stated concisely as $(V, \oplus)$ is an *abelian group*)
* *(1)* $\vec{u}+\vec{v} = \vec{v} + \vec{u}$ (commutative law)
* *(2)* $\vec{u} + (\vec{u}+\vec{w})=(\vec{u}+\vec{v})+\vec{w}$ (associative law)
* *(3)* There exists an element $\vec{0}\in V$ such that $\vec{u}+\vec{0}=\vec{0}+\vec{u}=\vec{u}$ (there exists an identity)
* *(4)* For each $\vec{u}\in V$, there is an element $-\vec{u}\in V$ such that $\vec{u}+-\vec{u}=-\vec{u}+\vec{u}=\vec{0}$ (inverses exist)
* **(b)** If $\vec{u}\in V$ and $c\in\mathbb{R}$, then $c\vec{u}\in V$. (closed under scalar multiplication, stated as the *abelian group* ($V, \odot$))
* *(1)* $c(\vec{u}+\vec{v}=c\vec{u}+c\vec{v}$. (distributive law 1)
* *(2)* $(c+d)\vec{u} = c\vec{u}+d\vec{u}$. (distributive law 2)
* *(3)* $c(d\vec{u})=(cd)\vec{u}$. (The group ($\mathbb{R}^x,\odot$) where $\mathbb{R}^x$ are non-zero real numbers acts on $V$)
* *(4)* $1\vec{u}=\vec{u}$. (addendum to *3*)
$$\therefore$$
A *vector space* consists of two *abelian groups* $(V, \oplus)$ and $(\mathbb{R}^x,\odot)$ acting on $V$ which respects the two distributive laws.
- ## Abstract Example
  For a set $S = \{\text{:<}, \text{:>}, \text{:3}\}$, then there is the vector space $V$ where:
  $$V:\{f:S\rarr\mathbb{R}\}$$
  Where $+$ is defined by:
  $$a_1e^{b_1x}+a_2e^{b_2x}=a_1a_2e^{(b_1+b_2)x}$$
- ## Determining Whether a Set is a Vector Space
	- ### Example
	  $$V=\{ae^{bx}:a,b\in\mathbb{R}\}$$
	  
	  **Closure under **$\bold{+}$:
- ## Givens of Vector Spaces
  * The elements of a vector space $V$ are called *vectors*.
  * The elements of $\mathbb{R}$ are called *scalars*. 
  * $\oplus$ is called ((67b36c75-7ca6-43fb-af3e-69c8e6518882)).
  * $\odot$ is called ((67b36c75-58bd-41c4-a543-09c3a7461cca)).
  * $\vec{0}$ is called the ((67912a9e-2bd7-4de0-ae70-fea77995ff98)).
  * $-\vec{u}$ is called the *negative of* $\it{\vec{u}}$.
  * If we allow scalars to be ((67b36c72-a64a-48f2-ad2e-9960e1e2830b)), then we obtain a *complex vector space*.
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
	- ### Characteristics Of A Valid Vector Space
	  The linear map of the constraint *must* be **linear**. For example, a ((66fc4beb-e6bb-4622-ba4c-cb9d1938d5c8)) is **linear**, but a ((66e8828d-8b04-4463-b479-f87150ad4c58)) is not.
- ## Common Spaces
	- ### Function Space
	  $$V=\{f:\mathbb{R}\rarr\mathbb{R}:f\text{ is continuous}\}$$
	- ### "$P_n$" space
	  The set of polynomials in the variable $x$ with real coefficients of degree $\le n$.
	  
	  **For example (**$\bf{P_2}$**)**:
	  $$P_2=\{a+bx+cx^2:a,b,c\in\mathbb{R}\}$$
	  $\oplus$ in $P_2$:
	  $(1 + x^2) + (-x + 2x^2) = 1 - x + 3x^2$
	  
	  $\odot$ in $P_2$:
	  $\frac{1}{2}(2x+4x^2)=x+2x^2$
	- ### $\mathbb{R}^n$ and $\mathbb{R}_n$
	- ### $M_{m,n}(\mathbb{R})$
	- #### "$U$" Space
	  $$U=\{u\in M_{2*2} | \text{tr}(u)=0\}$$
	  
	  The common basis vectors are the following three:
	  $$=x\begin{bmatrix}0 & 0\\ 1 & 0\end{bmatrix}+y\begin{bmatrix}0 & 0\\ 1 & 0\end{bmatrix}+z\begin{bmatrix}1 & 0\\ 0 & -1\end{bmatrix}$$
	- #### "$V$" Space
	  $$V=\{v\in M_{2*2}\text{ | }\det(v)=0\}$$
	  
	  **Does it have a zero matrix**:
	  Yes.
	  
	  **We verify that they stay in the space even with scalar multiplication**:
	  $$\det(s\begin{bmatrix}a & b\\ c & d\end{bmatrix})=\det(\begin{bmatrix}sa & sb\\ sc & sd\end{bmatrix})=s^2(ad-bc)$$
	  Yes.
	  
	  **We verify that they stay in the space even with matrix addition**:
	  It does not! There exist examples of matrix addition where two matrices with determinant of zero, when added, do not create a result with a determinant of zero.
	  
	  For example:
	  \begin{equation}
	  \begin{bmatrix}
	  1 & 0 \\
	  0 & 0
	  \end{bmatrix}
	  +
	  \begin{bmatrix}
	  0 & 0 \\
	  0 & 1
	  \end{bmatrix}
	  =
	  \begin{bmatrix}
	  1 & 0 \\
	  0 & 1
	  \end{bmatrix}
	  \end{equation}
	- #### Quadratic Space
	  $$\{a+bx+cx^2\text{ | }\begin{cases}a,b,c\in\mathbb{R}\\ x\in\mathbb{R}\end{cases}\}$$
	  
	  **Does it have a zero matrix**:
	  Yes, $0$.
	  
	  **Does it stay in the space even with scalar multiplication**:
	  Yes.
	  
	  **What are the basis vectors?**
	  $$1,x,x^2$$
- ## ?
  Let's say that we have two vector spaces, $V$ and $W$.
  
  $V$ has the basis $\beta=b_1,\ldots,b_{n}$
  $W$ has the basis $\gamma=c_1,\ldots,c_m$
  
  We have a linear map:
  $$L:V\rightarrow W$$
  $$\left\lbrack L\right\rbrack_{\beta}^{\gamma}$$
  $$\therefore$$
  $$L(b_1)=\alpha_1c_1+\ldots+\alpha_mc_m$$
  
  Our matrix ($M_{m\cdot n}$):
  \begin{equation}
  \begin{bmatrix}
  \alpha_{11} & \ldots & \alpha_{1n} \\
  \ldots & \ldots & \ldots \\
  \alpha_{m1} & \ldots & \alpha_{mn}
  \end{bmatrix}_\beta^\gamma
  \end{equation}