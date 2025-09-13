# Part 1 — Economist

## 1. Game and Equilibrium Concept
We study a two-player bargaining game adapted from the standard oTree bargaining demo.  
In the original version, two players simultaneously demand an integer share of 100 tokens.  
- If the sum of demands does not exceed 100, each receives their demand.  
- Otherwise, both receive zero.  

**Modification for our project:**  
Instead of a one-shot interaction, players now play in 2-round and 5-round versions.  
This allows us to compare outcomes across different horizons while keeping the payoff structure fixed.  

**Formal model:**  
- Players: \( I = \{1,2\} \)  
- Strategy set: \( s_i \in S_i = \{0,1,2,\ldots,100\} \)  
- Payoff function:  
\[
u_i(s_1, s_2) =
\begin{cases}
s_i, & \text{if } s_1+s_2 \leq 100 \\
0,   & \text{if } s_1+s_2 > 100
\end{cases}
\]

**Equilibrium concept (Nash, 1950):**  
A strategy profile \( s^\ast = (s_1^\ast, s_2^\ast) \) is a Nash equilibrium if for each player \( i \):  
\[
u_i(s_i^\ast, s_{-i}^\ast) \geq u_i(s_i, s_{-i}^\ast), \quad \forall s_i \in S_i
\]

**Existence theorem:**  
- For any finite normal-form game, a mixed-strategy Nash equilibrium exists (Nash, 1950, p.xx).  
- Proof uses Kakutani’s fixed point theorem.  
- For continuous strategy spaces, existence extends by Glicksberg’s theorem (1952, p.xx).  

---

## 2. Analytical Solution

### Pure-strategy equilibria
All pairs \( (s_1^\ast, s_2^\ast) \) such that \( s_1^\ast + s_2^\ast = 100 \) are Nash equilibria.  

- If one player increases demand → total > 100 → payoff drops to 0.  
- If one player decreases demand → payoff decreases directly.  

Thus, no unilateral deviation is profitable.  

### Symmetry and focal point
Although many equilibria exist, **(50,50)** is a natural symmetric focal equilibrium:  
- Equal split,  
- Easily recognized by players.  

### Efficiency
- Every equilibrium with \( s_1+s_2=100 \) is **Pareto efficient**.  
- Total surplus always equals 100.  
- From a utilitarian perspective: all equilibria are equivalent (\( \sum_i u_i = 100 \)).  

### Fairness
- Extreme equilibria (e.g., (100,0)) are highly unequal.  
- Symmetric split (50,50) is perfectly fair: satisfies envy-freeness and proportionality.  

---

## 3. Interpretation

### Realism and coordination
- In the one-shot version (R=1), equilibrium multiplicity creates a coordination problem.  
- In practice, experiments cluster around equal splits → fairness norms and focal-point effects (Roth, 1995, p.xx).  

### Multiplicity and refinements
- Not all equilibria are equally compelling.  
- Refinements (e.g., trembling-hand perfection) reduce plausibility of extreme allocations.  
- Equal split is more robust and empirically observed.  

### Repeated rounds (R=2,5)
- In finitely repeated games: any stage-game NE repeated each round forms a subgame perfect equilibrium (by backward induction).  
- In practice: repeated interaction enables learning/history dependence.  
- Prediction: more rounds → convergence toward fairer, more stable splits (closer to (50,50)).  

### Bounded rationality
- Players cannot enumerate all equilibria.  
- Use heuristics: “demand half,” “repeat last round.”  
- Explains empirical prevalence of equal splits.  

### Computational tractability
- This game is analytically simple (\( s_1+s_2=100 \)).  
- But in general, computing Nash equilibria is PPAD-complete (Daskalakis, Goldberg & Papadimitriou, 2009, p.xx).  
- This example illustrates the gap between theory and computation.  

---

## References
- Nash, J. (1950). *Equilibrium points in n-person games*.  
- Glicksberg, I. (1952). *A further generalization of the Kakutani fixed point theorem*.  
- Roth, A. (1995). *Bargaining experiments*.  
- Daskalakis, C., Goldberg, P., & Papadimitriou, C. (2009). *The complexity of computing a Nash equilibrium*.  

👉 Full PDFs / BibTeX files can be found in the [`refs/`](./refs/) folder.
