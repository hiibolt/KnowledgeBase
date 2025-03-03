## Definition
The vectors $\vec{v}_1,\dots,\vec{v}_n\in V$ are said to form a basis of $V$ if:
(a) $\vec{v}_1,\dots,\vec{v}_n$ span $V$.
(b) $\vec{v}_1,\dots,\vec{v}_n$ are *linearly independent*.
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