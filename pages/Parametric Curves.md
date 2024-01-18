## Definition
For two continuous curves $x, y$ defined on an interval I, the following parameter $$t$$ equations describe a parametric curve:
$$x=x(t)$$
$$y=y(t)$$

Alternatively: $$\gamma(t) = (x(t), y(t))$$

For an interval I(\alpha, \beta), \alpha is the **initial point**, and \beta is the **terminal point**.

$$C(t) = \gamma (a + b -t)\text{ for }a \leq t \leq b$$
Is a reversal of the **orientation** of the parametric curve, meaning $$C(a) = \gamma(b)$$.

A **closed curve** is considered where $$\gamma(a) = \gamma(b)$$.

A **double traversal** is where you complete the bounds twice, etc.

Flipping the bounds often flips the direction of the parametric.

A **direction reversal** can be accomplished for $\gamma(t)$ on $[a, b]$ by $\beta(a+b-t)$
- ## Eliminating the Parameter
  Functions might not need to be represented parametrically, typically functions that pass the vertical line test.
  
  $$\gamma(t) = (a\cos(t),b\sin(t))$$
  $$=$$
  $$1 = (\frac{x}{a})^2 + (\frac{y}{b})^2$$
  
  The typical approach is to isolate $t$, otherwise using trig or logarithmic identities.
- ## Calculus for a Parametric Curve
  
  If $x=x(t)$ and $y=y(t)$ are differentiable at $t$ (and x \neq 0), $\frac{dy}{dx} = \frac{y'(t)}{x'(t)}$.
  
  Higher order derivatives can be calculated as $$\frac{\frac{d}{dt}*\frac{dy}{dx}}{\frac{dx}{dt}}$$.
  
  *Note: The tangent line can easily be found using the x and y components of the parabola, given you have calculated* $\frac{dy}{dx}$.