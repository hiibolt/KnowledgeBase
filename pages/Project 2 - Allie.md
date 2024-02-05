## Introduction
In this project, we will be deriving variations of a predator-prey model. In this model, hawks and owls are found in an environment where they coexist but complete for prey. This causes for an increase in hawks to cause a decrease in owls, and vice versa. This non-linear relationship is quantified with the following model:

**Owls vs. Hawks** (Competing species in same environment)
$$\Delta O_n = k_1O_n-k_3O_nH_n$$
$$\Delta H_n = k_1O_n-k_3O_nH_n$$
Explanation of variables and constants:
* $\Delta O_n$: Change in owl population between generations*
* $\Delta H_n$: Change in hawk population between generations*
* $k_{1-4}$: Positive constants
* $O_n$ Population of owls at $n$ generation
* $H_n$ Population of hawks at $n$ generation

Our project deals with a similar model (Mice vs. Hawks), except they are not both predators, but predator-prey. As such, an increase in hawks causes the mice population to fall, but a decrease in mice also causes the hawk population to fall. You may notice that this is similar to the above, and indeed, we can draw similar conclusions as the textbook does with only minor tweaks.
- # Base Equation
  We are given a basic relation model composed of two equations:
  $$\Delta x_n = r_1x_n(1-\frac{y_0}{M_1}$$
  $$\text{and}$$
  $$\Delta x_n = r_1x_n(1-\frac{y_0}{M_1})$$
- # 1 - If the population of mice grows at a 5%