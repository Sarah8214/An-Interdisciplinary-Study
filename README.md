# Computational Scientist — Claim Game

## 2a. Normal Form & Computation (Google Colab)

### Experiment Setup
- Two players simultaneously choose a demand \( x_i \in \{1,2,\dots,100\} \).
- If \( x_1 + x_2 \leq 100 \), both receive their demands; otherwise, both get zero.
- **Discretization:** For computational feasibility, strategy space reduced to  
  \(\{0,25,50,75,100\}\). This simplification preserves the strategic structure while making the game tractable for visualization and solver computation.

### Payoff Matrices
The reduced action grid produces the following payoff matrices:

*(insert `payoff_matrices.png` here if available)*

### Nash Equilibria
- Computed using **NashPy** support enumeration.  
- Solver results include:
  - **Pure-strategy equilibria** where demands sum to 100 (e.g., (50,50), (75,25), etc.).
  - **Mixed-strategy equilibria** where players randomize across actions to satisfy equilibrium conditions.
- Note: Runtime warnings reflect **degeneracy**, since the game admits multiple symmetric equilibria.

*(insert `nash_equilibria.png` here if available)*

---

## 2b. Extensive Form & SPNE (Game Theory Explorer)

### Setup
- Extensive form modeled in **Game Theory Explorer (GTE)**.  
- Player 1 moves first; Player 2 observes Player 1’s demand before choosing their own.  
- Reduced action set: \(\{0,25,50,75,100\}\).  
- Payoffs follow same rule as normal form: if \(x_1 + x_2 \leq 100\), payoffs = (x1, x2); else (0,0).

### Game Tree
*(insert `gte_game_tree.png` here if available)*

### Interpretation
- **SPNE** refines the multiplicity from the normal form by enforcing sequential rationality.  
- Player 2 best-responds after observing Player 1’s choice.  
- Player 1 anticipates Player 2’s reaction, creating **first-mover advantage**.  
- Unlike the simultaneous game with many equilibria (any \(x_1+x_2=100\)), SPNE selects credible profiles via **backward induction**.

---

## Files
- `notebook.ipynb`: Colab notebook with payoff matrices & Nash equilibrium computation.  
- `gte_game_tree.png`: Screenshot of extensive-form game and SPNE solution.  
- `payoff_matrices.png` / `nash_equilibria.png`: Supporting figures.  
