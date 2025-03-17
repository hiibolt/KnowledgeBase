## Definition
The vectors $\vec{v}_1,\dots,\vec{v}_n\in V$ are said to form a basis of $V$ if:
(a) $\vec{v}_1,\dots,\vec{v}_n$ span $V$.
(b) $\vec{v}_1,\dots,\vec{v}_n$ are *linearly independent*.

A *vector space* $V$ is *finite dimensional* if there is a finite subset of $V$ that is a basis of $V$. Otherwise $V$ is called *infinite dimensional*.

If you have a vector basis of $V$ called $S$, then every vector in $V$ can be written in one and only one way as a linear combination of elements of $S$.

The dimension of a non-zero vector space $V$ is the number of vectors in a basis for $V$. We write $\text{dim }V$ for the dimension of $V$. We define the dimension of the trivial vector space $\{\vec{0}\}$ to be 0.
- ## Theorems
	- ### 1
	  Let $S=\{\vec{v}_1,\dots,\vec{v}_n\}$ be a set of non-zero vectors in a vector space $V$ and let $W=\text{span }S$. Then some subset of $S$ is a basis for $W$.
	- ### 2 "Bob Theorem"
	  If $S=\{\vec{v}_1,\dots,\vec{v}_n\}$ is a basis of a vector space $V$ and $T=\{\vec{w}_1,\dots,\vec{w}_r\}$ is a linearly independent set of vectors in $V$. Then $r\le n$.
	  
	  **Corollary 1**:
	  If $S=\{\vec{v}_1,\dots,\vec{v}_n\}$ and $T=\{\vec{w}_1,\dots,\vec{w}_m\}$ are bases for a vector space $V$, then $n = m$.
	  
	  In other words, *all basis have the same number of elements*.
	  
	  **Corollary 2**:
	  If the vector space $V$ has dimension $n$, then maximally independent subsets of $V$ contain $n$ vectors.
	- ### 3
	  Let $S$ be a set of vectors in a vector space $V$.
	  A subset $T\subseteq S$ is called a *maximally independent subset* of $S$ if $T$ is linearly independent and is not properly contained in any other linearly independent subset of $S.$
	- ### 4
	  Let $S=\{\vec{v}_1,\dots,\vec{v}_n\}$ be a set of non-zero vectors in a vector space $V$. Let $W = \text{span }S$. Then some subset of $S$ is a basis for $W$.
- ## Examples
	- ### Example 1
	  Check that $S=\{t^2+1,t-1,2t+2\}$ spans $P_2 (at^2+bt+c\in P_2)$.
	  In other words, find $a_1,a_2,a_3$ such that $a_1(t^2+1)+a_2(t-1)+a_3(2t+2)$.
	  
	  \begin{cases}
	  a_1=a \\
	  a_2 + 2a_3 = b \\
	  a_1-a_2+2a_3 = c
	  \end{cases}
	  $$\text{or}$$
	  \begin{cases}
	  a_1 = a\\
	  a_2=\frac{a+b-c}{2} \\
	  a_3=\frac{c+b-a}{2}
	  \end{cases}
	  
	  Next, we need to show the vectors are linearly independent.
	  To do so, set $a_1(t^2+1)+a_2(t-1)+a_3(2t+2)=0*1+0*t+0*t^2=\vec{0}$.
	  Solve, then set $a_1 = a_2 = a_3 = 0$.
	- ### Example 2
	  Find a basis for the subspace $V$ of $P_2$ consisting of all vectors of the form $at^2+bt+c$ where $c=a-b$.
	  
	  $$at+bt+(a-b)=a(t^2+1)+b(t-1)$$
	  $\therefore$ the subspace has basis $t_2+1, t-1$.