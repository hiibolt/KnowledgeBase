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
  **If the population of mice grows at a 5% rate pergeneration in the absence