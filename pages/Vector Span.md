## Definition
If $$S=\{\vec{v}_1,\dots,\vec{v}_k\}$$ is a set of vectors in a vector space $V$, then the *set* of all linear combinations of the vectors in $S$ is called the *span* of $S$.

Notated as:
$$\text{span }S$$
$$\text{span }\{\vec{v_1},\dots,\vec{v}_k\}$$

*Note*: When checking if something is in a span, if after RREF the system is inconsistent, then the given vector $\vec{v}$ is *not* in the span.
- ## Example
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