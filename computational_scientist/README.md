# Part 2 — Computational Scientist

This module contains the computational analysis of the two-player bargaining game.

## 1. Normal Form & Computation
We construct the normal-form representation of the bargaining game. Each player simultaneously demands an integer amount from {1, …, 100}. To make computation tractable, the action set is reduced to {0, 25, 50, 75, 100}.

Payoff function:
- If x1 + x2 ≤ 100, then payoff = (x1, x2).
- Otherwise, payoff = (0, 0).

Figures:
- **Figure 1**: Payoff matrices for Player 1 and Player 2 in the reduced action grid.  
- **Figure 2**: Nash equilibria of the reduced grid, computed using *NashPy* (Savani & Nash, 2021).

## 2. Interpretation of Results
- Pure-strategy NE: Any pair summing to 100 (e.g., 50+50, 75+25).
- Mixed strategies: Multiple equilibria exist due to degeneracy of the payoff structure.
- Symmetry: (50,50) emerges as a natural focal equilibrium due to fairness.

## 3. Extensive-Form Analysis
Using *Game Theory Explorer* (Savani & von Stengel, 2015), we build an extensive-form tree with Player 1 moving first and Player 2 responding. The action set is reduced to {0, 50, 100} for readability.

- **Figure 3**: Extensive-form game tree.  
- **Figure 4**: Equivalent strategic-form matrix.

### Insights:
- The sequential SPNE refines the multiplicity of simultaneous equilibria.
- Player 2 best-responds to Player 1’s observed action, and Player 1 anticipates this.
- Demonstrates backward induction and first-mover advantage.

## References
- Savani, R., & Nash, J. (2021). *Nashpy: A Python library for 2-player games*.  
- Savani, R., & von Stengel, B. (2015). *Game Theory Explorer—Software for the Applied Game Theorist*. Computational Management Science, 12, 5–33.
