### Example
What is the probability that event $A$ will occur given that we already know $B$ has occurred?
$$P(A|B)=\frac{P(A\cap B)}{P(B)}$$

Reminder - to ensure valid data tables:
1.) You must verify that all probabilites are \ge 0
2.) You must verify that $\sum \text{probabilities} = 1$
- ## 'Given That'
  Given that a person is in B, what is the probability that they are also in A?
  $$P(A|B)=\frac{P(A\cap B)}{P(B)}$$
  
  And, when given that a person is in A, what is the probability that they are also in BB
  $$P(B|A)=\frac{P(A\cap B)}{P(A)}$$
  
  In short, *divide by the 'given that'*.
- ## Law of Total Probability
  $$P(B)=\sum_{i=1}^k(P(B|A_i)P(A_i)$$
  For example:
  **What is the probability that a randomly selected purchaser has a gaming counsel that will need repair work while under warranty?**
- ## Bayes Theorem
  Let $A_1, A_2, ..., A_k$ be a collection of mutually exclusive and exhaustive events with $P(A_i)>0 \forall i$, then for any event $B$, $P(B)>0$ we have:
  $$P(A_i|B)=\frac{P(A_i\cap B)}{P(B)}=\frac{P(B|A_i)P(A_i)}{\sum_{j=1} P(B|A_j)P(A_j)}$$
  **What is the probability that a customer returns a type 1 console, given that it needs a warranty?**
  $$P(B1|W)=\frac{P(B1\cap W)}{P(B)}$$
-