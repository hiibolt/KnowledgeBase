-
- ### 7.1.E1
  Integrate $f(x,y) = xy^2$ over the region inside circle $r=3\cos\theta$ outside the cardioid $r=1+\cos\theta$
  
  Upper bound is $3\cos\theta$.
  Lower bound is $1+\cos\theta$.
  
  They are both equal at $\theta = \pm\frac{\pi}{3}$.
  $$\int_{\frac{-\pi}{3}}^{\frac{pi}{3}}\int_{1+\cos\theta}^{3\cos\theta}((r\cos\theta)(r\sin\theta)^2r)drd\theta$$
  $$\text{or}$$
  $$\int_{\frac{-\pi}{3}}^{\frac{\pi}{3}}\int_{1+\cos\theta}^{3\cos\theta}(\cos\theta\sin^2\theta r^4)drd\theta$$
  $$\text{or}$$
  $$\int_{\frac{-\pi}{3}}^{\frac{\pi}{3}}(\cos\theta\sin^2\theta \frac{r^5}{5}|_{1+\cos\theta}^{3\cos\theta})d\theta$$
  $$\text{...}$$
- ### 7.1.E2
  Find the volume of the solid above the cone $z = \sqrt{x^2+y^2}$ and below the sphere $x^2+y^2+z^2=1$.
  
  ?? dude didn't explain shit LOL
  
  $$\int_0^{2\pi}\int_{0}^{\frac{1}{\sqrt{2}}}((\sqrt{1-r^2}-r)r)drd\theta$$
  $$\text{...}$$
  $$\frac{(2-\sqrt{2})\pi}{3}$$
- ### 7.1.E3
  Evaluate the integral $\int_{-\infty}^\infty (e^{-x^2})dx$
  
  $$\int_{-\infty}^\infty\int_{-\infty}^\infty(e^{-(x^2+y^2)})dydx$$
  $$\text{or}$$
  $$\int_{0}^{2\pi}\int_{0}^\infty(e^{-r^2}r)drd\theta$$
  $$\text{or (u-sub)}$$
  $$=\sqrt{\pi}$$