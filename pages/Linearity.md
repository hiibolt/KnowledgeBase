### Linearity
For a function $$L$$, it must satisfy:
$$L(x+y)=L(x) + L(y)$$
$$L(cX) = cL(x)$$

For example, the derivative operation is linear:
$$\int(f+g) = \int{f} + \int{g}$$
$$\int(cf) = c\int{f}$$
- ## Linear Dependence
  Vector $\vec{v}_1,\dots\vec{v}_k\in V$ are said to be *linearly dependent* (LD) is there exist constants $a_1,\dots,a_k\in\mathbb{R}$, not all equal to $0$, such that:
  $$a_1\vec{v}_1+\dots+a_2\vec{v}_k=\vec{0}$$
	- ### Example 1
	  $(1,1)^T\text{ and }(1,2)^T$ are linearly independent.
	  
	  **Proof**:
	  $$c_1(1, 1)^T+c_2(1,2)^T=(0,0)^T$$
	  By RREF, we get $c_1=c_2=0$.
	- ### Example 3
	  $$\vec{v}_1=(1,2,3)^T,\vec{v}_2=(2,0,2)^T,\vec{v}_3(9,2,7)^T,\vec{v}_4=(-2,2,1)^T$$
	  
	  Since assigning $a_n$ as a coefficient to each vector $\vec{v}_n$ creates a system with more unknowns than equations, they are not linearly independent - they are *linearly dependent*.
	- ## Theorems
		- ### 1 
		  Let $S_1$ and $S_2$ be finite subsets of a vector space and assume $S_1\subseteq S_2$. Then:
		  * (a) IF $S_1$ is linearly dependent then so is $S_2$
		  * (b) If $S_2$ is linearly independent, then so is $S_1$
		- ### 2
		  If the nonzero vectors $\vec{v}_1,\dots\vec{v}_n$ in a vector space $V$ are linearly dependent, then one of the vectors, say $\vec{v}_j (j\ge 2)$ is a linear combination of the preceeding vectors.
		- ### 3
		  Non-zero vectors $\vec{v}_1,\dots,\vec{v}_n\in V$ are *linearly dependent* if and only if $\exists j \ge z$ such that $\vec{v}_j$ is a linear combination of $\vec{v}_i,\dots,\vec{v}_{j-1}$.