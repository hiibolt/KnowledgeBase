## Introduction
In this project, we will be deriving variations of a predator-prey model. In this model, hawks and owls are found in an environment where they coexist but complete for prey. This causes for an increase in hawks to cause a decrease in owls, and vice versa. This non-linear relationship is quantified with the following model:

**Owls vs. Hawks** (Competing species in same environment)
$$\Delta O_n = k_1O_n-k_3O_nH_n$$
$$\Delta H_n = k_1O_n-k_3O_nH_n$$
Explanation of variables and constants:
* $\Delta O_n$: Change in owl population between generations
* $\Delta H_n$: Change in hawk population between generations
* $k_{1-4}$: Positive 'weight' constants
* $O_n$ Population of owls at $n$ generation
* $H_n$ Population of hawks at $n$ generation

Our project deals with a similar model (Mice vs. Hawks), except they are not both predators, but predator-prey. As such, an increase in hawks causes the mice population to fall, but a decrease in mice also causes the hawk population to fall. You may notice that this is similar to the above, and indeed, we can draw similar conclusions as the textbook does with only minor tweaks.
- # Base Equation
  We are given a basic relation model composed of two equations:
  $$\Delta x_n = r_1x_n(1-\frac{y_n}{M_1})$$
  $$\text{and}$$
  $$\Delta x_n = r_2y_n(1-\frac{x_n}{N_1})$$
  
  It's not immediately obvious what these variables and constants are, however. We'll start by assigning $$x$$ to **mice** and $$y$$ to **hawks**:
  * $\Delta x_n$: Change in mice population between generations
  * $\Delta y_n$: Change in hawk population between generations
  * $x_n$ Population of mice at $n$ generation
  * $y_n$ Population of hawks at $n$ generation
  * $r_{1-2}$: ??
  * $M_1\text{ and }N_1$: ??
- # 1
  **If the population of mice grows at a 5% rate per generation in the absence of hawks, and the population of hawks falls by 6%per generation in the absence of mice, what can you say about the parameters of the model?**
  
  With $$x$$ representing mice, we will assign $r_1$ to be $+0.05$, as it can be inferred by the direct distribution onto other terms that $$r_1$$ is a constant representing scale factor between the two populations. Because the mice population *increases*, we will use positive 0.05 as our constant. Because the hawk *decreases*, we will use negative 0.06 as our constant.
  
  This updates our equations to be:
  $$\Delta x_n = (0.05)x_n(1-\frac{y_n}{M_1})$$
  $$\text{and}$$
  $$\Delta x_n = (-0.06)y_n(1-\frac{x_n}{N_1})$$
- # 2
  **Suppose that there is an equilibrium when the population of mice is 200,000 and that of hawks is 1500. What can you say about the parameters of this model?**
  
  Equilibrium is achieved when both populations have a Yrate of change of zero. Setting our equations equal to zero and plugging in the population values gives us the following:
  $$0 = (0.05)(200,000)(1-\frac{1500}{M_1})$$
  $$0 = (-0.06)(1500)(1-\frac{200,000}{N_1})$$
  
  We can solve for $M_1$:
  $$0 = (1-\frac{1500}{M_1})$$
  $$\frac{1500}{M_1} = 1$$
  $$M_1 = 1500$$
  And do the same for $N_1$:
  $$0 = (1-\frac{200,000}{N_1})$$
  $$\frac{200,000}{N_1} = 1$$
  $$M_1 = 200,000$$
  
  What can now be said about the parameters is that:
  * $M_1$ is the number of hawks required for mice population equilibrium
  * $N_1$ is the number of mice required for hawk population equilibrium
  
  
  This updates our equations to be:
  $$\Delta x_n = x_n(0.05)(1-\frac{y_n}{1500})$$
  $$\text{and}$$
  $$\Delta x_n = y_n(-0.06)(1-\frac{x_n}{200,000})$$