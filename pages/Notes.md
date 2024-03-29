## Derivative of Cost Equation C(x)
Given a cost equation
$$C(x)=\sum^n_{i=1}{kN_i|x-x_i|}$$
where
$$n = \text{\# of stations}$$
$$N_i = \text{\# of trips}$$
$$k = \text{Cost per mile}$$
$$x = \text{distance from west-most location}$$

The slope function (derivative) $$S(i)$$ of a given interval $i \text{ to } i+1$ is the following pattern:
$$S_0=-N_1-N_2-N_3-...N_n$$
$$S_1=N_1-N_2-N_3-...N_n$$
$$S_2=N_1+N_2-N_3-...N_n$$

Notice that this is equivalent to: 
$$S_0=-N_1-N_2-N_3-...N_n$$
$$S_1=S_0+2N_1$$
$$S_2=S_1+2N_2$$
$$...$$
$$S_i=S_{i-1}+2N_i$$

Therefore, just like any derivative, the critical (minima) points are where:
$$S(i-1) < 0 \text{ and } S(i) \geq 0$$
Ensure that you test $\alpha$ and $\beta$, as they could potentially be more cost efficient than the minima.