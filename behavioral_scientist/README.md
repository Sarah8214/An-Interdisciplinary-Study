# Part 3 — Behavioral Scientist

This module contains the behavioral experiments and comparative analysis.

## 1. Human Experiment Results
Players interacted in 1-, 2-, and 5-round versions of the bargaining game.

**Table 1. Human Demands and Payoffs**
| Round | Player 1 Demand | Player 2 Demand | P1 Payoff | P2 Payoff |
|-------|-----------------|-----------------|-----------|-----------|
| Exp 1 – R1 | 51 | 50 | 0  | 0  |
| Exp 2 – R1 | 51 | 50 | 0  | 0  |
| Exp 2 – R1 | 51 | 25 | 51 | 25 |
| Exp 3 – R1 | 51 | 25 | 51 | 25 |
| Exp 3 – R2 | 49 | 51 | 49 | 51 |
| Exp 3 – R3 | 50 | 50 | 50 | 50 |
| Exp 3 – R4 | 50 | 50 | 50 | 50 |
| Exp 3 – R5 | 50 | 50 | 50 | 50 |

**Interpretation:**  
Humans initially experiment with over- or under-demands, often receiving zero payoff. Over repeated rounds, they converge to the fair 50–50 split, reflecting learning and fairness norms.

---

## 2. LLM Experiment Results
We tested ChatGPT (OpenAI, 2025) in the same game.

**Table 2. LLM Demands and Reasoning**
| Round | LLM Demand | Reasoning Summary |
|-------|------------|-------------------|
| 1 | 50 | Fair split to maximize guaranteed payoff |
| 2 | 50 | Maintains fairness and stability |
| 3 | 50 | NE-aligned choice |
| 4 | 50 | Consistency from rational reasoning |
| 5 | 50 | Immediate convergence to equilibrium |

**Interpretation:**  
The LLM immediately chooses the symmetric equilibrium (50–50) and repeats it consistently, contrasting with human trial-and-error.

---

## 3. Comparative Analysis
**Table 3. Comparison of Theory, Humans, and LLM**
| Source | Observed Behavior | Alignment with NE |
|--------|------------------|-------------------|
| Theory (NE) | Any demand pair summing to 100 | Matches pure-strategy NE |
| Humans | Trial-and-error; eventual 50–50 | Partial alignment |
| LLM | Immediate 50–50 | Full alignment |

**Observations:**  
- Humans show bounded rationality and risk considerations before converging.  
- LLMs align with theoretical predictions from the start.  
- Repeated play highlights fairness and learning for humans, but consistent rationality for AI.

---

## 4. Theory Refinement
We propose a **bounded-rationality equilibrium (BRE)** to capture human deviations:
\[
x_i^{BR} = \arg \max_{x_i \leq \theta_i} \, E[u_i(x_i, x_j)], \quad \theta_i < 100 - \min(x_j)
\]

This accounts for risk aversion, fairness, and learning over rounds.

## References
- Camerer, C. F. (2004). *Behavioral Game Theory: Experiments in Strategic Interaction*.  
- Fehr, E., & Schmidt, K. M. (1999). *A Theory of Fairness, Competition, and Cooperation*. Quarterly Journal of Economics, 114(3), 817–868.  
- OpenAI. (2025). *ChatGPT (September 2025 version)*. https://chat.openai.com
