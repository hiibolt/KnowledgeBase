- Given a cost equation
  $$C(x)=\sum^n_{i=1}{kN_i|x-x_i|}$$
  where
  $$n = \text{\# of stations}$$
  $$N_i = \text{\# of trips}$$
  $$k = \text{Cost per mile}$$
  $$x = \text{distance from west-most location}$$
  
  The slope (derivative) of a given interval $i \text{to} i+1$ is the following pattern:
  $$S_0=-N_1-N_2-N_3-...N_n$$
  $$S_1=N_1-N_2-N_3-...N_n$$
  $$S_2=N_1+N_2-N_3-...N_n$$