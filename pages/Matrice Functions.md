## Functions
A function $f : S \rarr T$ is a set of ordered pairs $(s,t)$ where $s\in S$ and $t \in T$, such that for every $s \in S$, there exists exactly one $t\in T$ for which $f(x)=t$.

$S$ can be defined as the *domain*
$T$ can be defined as the *codomain*, **not** to be confused with the term *range*.
- ## Linear Functions
  $$f : \mathbb{R}^n \rarr \mathbb{R}m$$
  $$\vec{v} \mapsto A\vec{v}$$
  It's worth noting that the above notation is *maps-to* notation, which can be re-written as:
  $$f(\vec{v})=A\vec{v}$$
  
  Requirements to be a linear function:
  $$f(\vec{v}_1+\vec{v}_2)=f(\vec{v}_1)+f(\vec{v}_2)$$
  $$f(c\vec{v})=cf(\vec{v})$$
- ## Composition
  Let $f:A\rarr B$ be a function and $g:B\rarr C$ be another function.
  
  The composition of *f and g* is the function:
  $(g\circ f)(x)=g(f(x))$ where $g\circ f:A\rarr C$
  
  This is read as "$g$ composed with $f$". This composition is *only* valid if the *image* of $f$ is contained in the domain of $g$.