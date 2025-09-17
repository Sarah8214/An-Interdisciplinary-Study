# 1. Game and Equilibrium Concept

We study a two-player bargaining game adapted from the standard oTree bargaining demo (Chen, Schonger & Wickens, 2016).  
In the original version, two players simultaneously demand an integer share of 100 tokens.  
If the sum of demands does not exceed 100, each receives their demand; otherwise, both receive zero.

### Project Modifications
- Implemented 1-, 2-, and 5-round versions of the game.  
- Adjusted the UI to display cumulative scores after each round and a final payoff summary.  
- These modifications allow us to examine how strategies evolve, compare outcomes across horizons, and observe fairness dynamics.

### Formal Definition
- Players: \( I = \{1,2\} \)  
- Strategy set: \( s_i \in S_i = \{0,1,2,\ldots,100\} \)  
- Payoff function:  

\[
u_i(s_1,s_2) =
\begin{cases}
s_i, & \text{if } s_1 + s_2 \leq 100 \\
0, & \text{if } s_1 + s_2 > 100
\end{cases}
\]

### Equilibrium Concept
We adopt the concept of **Nash Equilibrium** (Nash, 1950).  
A strategy profile \(s^\ast = (s_1^\ast, s_2^\ast)\) is a NE if:

\[
u_i(s_i^\ast, s_{-i}^\ast) \geq u_i(s_i, s_{-i}^\ast), \quad \forall s_i \in S_i
\]

**Existence theorem:**  
For any finite normal-form game, a mixed-strategy NE exists (Nash, 1950).  
The proof embeds the mixed strategy set into a compact convex simplex and applies Kakutani’s fixed point theorem.  
For continuous strategy spaces with continuous payoffs, existence extends by Glicksberg’s theorem (1952).
