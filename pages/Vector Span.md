## Definition
If $$S=\{\vec{v}_1,\dots,\vec{v}_k\}$$ is a set of vectors in a vector space $V$, then the *set* of all linear combinations of the vectors in $S$ is called the *span* of $S$.

Notated as:
$$\text{span }S$$
$$\text{span }\{\vec{v_1},\dots,\vec{v}_k\}$$

*Note*: When checking if something is in a span, if after RREF the system is inconsistent, then the given vector $\vec{v}$ is *not* in the span.
- ## Examples
	- ### Example 1
	  \begin{equation}
	  \text{span }
	  \{
	  \begin{bmatrix}
	  0 & 0 \\
	  1 & 0 \\
	  0 & 0
	  \end{bmatrix},
	  \begin{bmatrix}
	  0 & 1 \\ 
	  0 & 0 \\
	  0 & 0
	  \end{bmatrix},
	  \begin{bmatrix}
	  0 & 0 \\
	  0 & 0 \\
	  0 & 1
	  \end{bmatrix}
	  \}
	  \end{equation}
	  \begin{equation}
	  \{
	  \begin{bmatrix}
	  0 & a_2 \\
	  a_1 & 0 \\
	  0 & a_3
	  \end{bmatrix}
	  : a_1, a_2, a_3 \in \mathbb{R}
	  \}
	  \end{equation}
	- ### Example 2
	  For $\vec{e}_1=(1,0,0)^T,\vec{e}_2=(0,1,0)^T,\text{ and }\vec{e}_3=(0,0,1)^T$, these span the entirety of $\mathbb{R}^3$.
	- ### Example 3
	  In $P_2$, prove that $\vec{v}_1=t^2-4t+1$ and $\vec{v}_2=t^2-2$ does not span $P_2$.
	  
	  **Proof**:
	  $$v=at^2+bt+c$$
	  ...and no $a_1$ and $a_2$ $a_1\vec{v}_1+a_2\vec{v}_2=\vec{v}$.