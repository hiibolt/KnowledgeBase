## General Definition
**Properties**:
\begin{equation}
\int\int_D(mf(x,y)\pm Mg(x,y))dA =
m\int\int_D(f(x,y))dA \pm M\int\int_D(g(x,y))dA
\end{equation}
	- #### 6.1.E1
	  Evaluate $\int\int x\cos(x+2y)dA$ for $R = [0,\frac{\pi}{2}] * [0,\pi]$
	  
	  $$\int (x\sin(x+2y)+\cos(x+2y)|_0^{\frac{\pi}{2}})$$
	  $$\text{or}$$
	  $$\int (\frac{\pi-2}{2}cos(2y) - sin(2y))dy$$
- ## General Areas
  Use a new function F:
  \begin{cases}
  f(x,y)\text{ if }(x,y) \in D\\
  0\text{ if }(x,y) \notin D
  \end{cases}
  
  Then:
  $$\int\int F(x,y) dA$$
	- ### 6.2.E1
	  $$=\int_0^1\int_0^{x^3}cos(x^4)dydx$$
	  $$\text{or}$$
	  $$=\int_0^1y\cos(x^4)|_0^{x^3}dx$$
	  $$\text{or}$$
	  $$=\int_0^1x^3\cos(x^4)dx$$
	  $$\text{or (u-sub)}$$
	  $$\text{...}$$
	- ### 6.2.E2
	  Evaluate $$\int\int_Dx^2y^2dA$$ for 
	  \begin{equation}
	  D = 
	  \begin{cases}
	  (x,y) | \frac{y}{2} \leq x \leq \sqrt{y}, 0 \leq y \leq 4
	  \end{cases}
	  \end{equation}
	  
	  Our box is $(0,2)$ for $x$, and $(0,4)$ for $y$.
	  
	  $$\int_0^4\int_0^2 F(x,y)dA$$
	  $$\text{or}$$
	  $$\int_0^4\int_{\frac{y}{2}}^{\sqrt{y}} x^2y^2 dxdy$$
	  $$\text{or}$$
	  $$\int_0^4 \frac{x^3}{3}y^2|_{\frac{y}{2}}^{\sqrt{y}}dy$$
	  $$\text{or}$$
	  $$\int_0^4(\frac{y^\frac{7}{2}}{3}-\frac{y^5}{24})dy$$
	  $$\text{(latter half is arithmetic, no deviation from Calc II)}$$
	- ### 6.2.E3
	  Integrate $f(x,y) = 2x+3y+4$ over the unit disk.
	  
	  \begin{equation}
	  D = \{(x,y) | -1 \leq x \leq 1, -\sqrt{1-x^2} \leq y \leq \sqrt{1-x^2} \}
	  \end{equation}
	  $$\int_{-1}^1\int_0^1(2x+3y+4)dxdy$$
	  $$\text{or}$$
	  $$\int_{-1}^1\int_{-\sqrt{1-x^2}}^{\sqrt{1-x^2}}(2x+3y+4)dxdy$$
	  $$\text{or}$$
	  $$\int_{-1}^1[2xy+\frac{3}{2}y^2+4y]|_{-\sqrt{1-x^2}}^{+\sqrt{1-x^2}}dx$$
	  $$\text{or}$$
	  $$\int_{-1}^1(4x\sqrt{1-x^2}+8\sqrt{1-x^2})dx$$
	  $$\text{or}$$
	  $$2\int_0^1(8\sqrt{1-x^2})dx$$
	  $$\text{or}$$
	  $$8\pi$$
	- ### 6.2.E4
	  Integrate $f(x,y) = e^{x^2}$ over the triangle with vertices $(0,0), (1,0),\text{ and }(1,1)$
	  
	  $$D=\{(x,y) | 0 \leq x \leq 1, 0 \leq y \leq x\}$$
	  
	  $$\int_0^1\int_0^x(e^{x^2})dydx$$
	  $$\text{or}$$
	  $$\int_0^1([ye^{x^2}]|_0^x)dx$$
	  $$\text{or}$$
	  $$\int_0^1xe^{x^2}dx$$
	  $$\text{or (u-sub)}$$
	  $$\frac{1}{2}\int_{0^2}^{1^2}(e^udu)$$
	  $$\text{?}$$
	- ### 6.2.E5
	  Evaluate the iterated integral:
	  $$\int_0^2\int_{y^2}^4(\sqrt{x}\sin(x))dxdy$$
	  
	  We must reverse the order of integration!
	  $$\text{(new) }D=\{(x,y) | 0 \leq x \leq 4, 0 \leq y \leq \sqrt{x}\}$$
	  $$\text{so}$$
	  $$\int_0^4\int_0^{\sqrt{x}}(\sqrt{x}\sin(x))dydx$$
	  $$\text{or}$$
	  $$\int_0^4(x\sin(x))dx$$
	  $$\text{or}$$
	  $$[-x\cos(x)+sin(x)]|_0^4$$
- ## Parametric Areas
  $$\int\int_Rf(x,y)dA=\int_\alpha^\beta\int_a^bf(r\cos\theta,r\sin\theta)r drd\theta$$
  
  For more general regions, we can use an equation not too dissimilar to our equation for the Cartesian coordinate system:
  $$D=\{(r, \theta) | \alpha \leq \theta \leq \beta, g(\theta) \leq r \leq h(\theta) \}$$
  \begin{equation}
  F(x,y) = 
  \begin{cases}
  f(x,y) \text{ for } (x,y) \in D\\
  0 \text{ for } (x,y) \notin D
  \end{cases}
  \end{equation}
  $$\int\int_D(f(x,y))dA=\int_\alpha^\beta\int_{g(\theta}^{h(\theta)}(f(r\cos\theta,r\sin\theta)r)drd\theta$$
	- ### 6.3.E1
	  Consider again the first basic example, integrating $f(x,y) = x^2 + y^2$ but rather over the polar rectangle $R = [0,1] x [0,1]$.
	  
	  $$\int\int_R(x^2+y^2)dA=\int_0^1\int_0^1 r^2rdrd\theta$$
	  $$\text{or}$$
	  $$=\int_0^1d\theta \int_0^1r^2rdr$$
	  $$\text{or}$$
	  $$=\frac{1}{4}$$
	- ### 6.3.E2
	  Evaluate $\int\int_R\tan^{-1}(\frac{y}{x})dA$ for $R = \{(x,y) | -x \leq y \leq x, 1 \leq x^2+y^2 \leq 4\}$.
	  
	  $$R = [1,4] x [-\frac{pi}{4},\frac{pi}{4}]$$
	  $$=\int_1^4\int_{\frac{pi}{4}}^{\frac{pi}{4}}(\theta r)drd\theta$$
	  $$\text{or}$$
	  $$=\int_1^4d\theta\int_{-\frac{pi}{4}}^{\frac{pi}{4}}(\theta r)dr$$
	  $$\text{or}$$
	  $$=0 * ...$$
	  $$\therefore$$
	  $$=0$$
	- ### 6.3.E3
	  Evaluate the iterated integral $\int_{-3}^3\int_0^{\sqrt{9-x^2}}(\cos(x^2+y^2))dydx$.
	  
	  $$=\int_0^\pi d\theta\int_0^3(\cos(r^2)r)dr$$
	  $$\text{or}$$
	  $$=\frac{\pi}{2}\sin(9)$$
	- ### 6.3.E4
	  Evaluate $R = [2, 1 + \sqrt{3}] x [\frac{pi}{6},\frac{pi}{3}]$
	  
	  $$V=\int_{\frac{pi}{6}}^{\frac{\pi}{3}}\int_2^{1 + \sqrt{3}}(r^2r)drd\theta$$
	  $$\text{or}$$
	  $$=\int_{\frac{pi}{6}}^{\frac{\pi}{3}}((1+2\cos\theta)^4-16)d\theta$$
	  $$\text{...}$$
	  $$=\frac{333\sqrt{3} - 186\pi - 368}{384}$$
	- ### 6.3.E5
	  Evaluate the iterated integral $\int_0^6\int_0^{\sqrt{6y-y^2}}(x^3)dxdy$.
	  
	  $$\int_0^{\frac{pi}{2}}\int_0^{6\sin(\theta)}((r\cos\theta)^3r)drd\theta$$
	  $$\text{or}$$
	  $$\frac{6^5}{5}\int_0^{\frac{pi}{2}}(\cos\theta(1-\sin^2(\theta))\sin^5(\theta))d\theta$$
	- ### 6.3.E6
	  Evaluate $\int\int_D(\frac{x^2}{x^2+y^2})dA$ for the region enclosed by $(x-1)^2+y^2=1$.
	  
	  $$=\int_{-\frac{\pi}{2}}^\frac{\pi}{2}\int_0^{2\cos\theta}(\frac{(r\cos\theta)^2}{r^2}r)drd\theta$$
	  $$\text{or}$$
	  $$=\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}(\cos^2\theta\frac{r^2}{2}|_0^{2\cos\theta})d\theta$$
	  $$\text{...}$$
	  $$=\frac{3\pi}{4}$$
-