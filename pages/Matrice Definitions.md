#### Column Vector
A vertical set.

For example, for the set of column vectors with elements of $$\mathbb{R}$$ is $$\mathbb{R}^{n}$$.
- #### Row Vector
  A horizontal set.
  
  For example, for the set of row vectors with elements of $$\mathbb{R}$$ is $$\mathbb{R}_{n}$$.
- #### Diagonal Matrix
  A matrix where all elements $m_{ij} = 0\text{ when }i\ne j$.
	- #### Scalar Diagonal Matrix
	  A diagonal matrix, but all elements are the same number.
	- #### Identity Matrix
	  A diagonal matrix, but all non-zero elements are 1.
- ### Symmetric Matrix
  A matrix where $A=A^T$
	- ### Skew Symmetric Matrix
	  A matrix where $A^T= -A$.
- ### Nonsingular/Invertible Matrix
  id:: 67a25d50-5203-40c8-a7c3-f3e65c7e765d
  A matrix $A$ where there exists a matrix $B$ such that $AB = I_n$.
  
  This matrix $B$ is also called the *inverse* of $A$.
- ### Singular/Noninvertible Matrix
  id:: 67a25d50-6c70-43fd-bfae-9e0e7ebcd07e
  A matrix $A$ where there exists *no* matrix $B$ such that $AB=I_n$.
- ### Triangle Matrix
  id:: 67a6470d-b340-4c59-b950-7d56e59bb513
  A matrix $A$ where all elements above or below the diagonal are $0$.
- ### Zero Vector
  id:: 67912a9e-2bd7-4de0-ae70-fea77995ff98
  $$\vec{0}\in\mathbb{R}^n$$
  $$\vec{0}\in\mathbb{R}_m$$
  Both are column/row vectors respectively with all elements set to 0.
- #### Homogeneous
  An equation $A\vec{x} = \vec{0}$ is called a *homogeneous* equation.
- #### Inhomogeneous
  An equation $A\vec{x} = \vec{b}$, where $\vec{b} \ne \vec{0}$, is called an *inhomogeneous* equation.