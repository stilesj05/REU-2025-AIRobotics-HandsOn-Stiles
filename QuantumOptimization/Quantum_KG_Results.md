
# 🧠 Task 4: Quantum Optimization on Hospital Simulation Graph

## 📌 Problem Modeled

I modeled a **graph partitioning problem** using the Max-Cut formulation on a real hospital simulation graph. This problem seeks to divide the nodes into two groups such that the number of edges **cut between them is maximized**.

This simulates:
- Load balancing agents across hospital zones
- Isolating infected vs. non-infected areas
- Segmenting patient clusters or critical rooms

---

## 🔁 QUBO Formulation

I used `max_cut_qubo(G)` to construct a **QUBO dictionary** representing the problem in the form:

\[
\min \sum_{i,j} Q_{ij} x_i x_j
\]

Where each variable \( x_i \in \{0, 1\} \) indicates group membership.

---

## ⚙️ Solution Method

I solved the QUBO using:

```python
maximum_cut(G, sampler=ExactSolver())
```

This simulates a quantum annealer's or QAOA's optimization using a classical exact solver.

---

## ✅ Max-Cut Result

The graph was divided into two optimal sets to maximize cut edges.

**Partition Group A** (from Max-Cut):
```
{ 'P1', 'P2', 'P3', 'P4', 'H_L', 'H_R', 'R', 'Exit', 'S', 'D' }
```

**Partition Group B**:
All other nodes in the graph (likely agents, tasks, and environment entities).

---

## 📈 Interpretation

- All patient nodes and key infrastructure were grouped together.
- Other nodes (like agents and tasks) were optimally separated to **maximize communication or logistical cuts**.
- This structure could support a **trust-aware or hazard-isolating agent deployment** strategy.

---

## ✅ Summary

- ✅ Converted graph to QUBO using Max-Cut
- ✅ Solved with `ExactSolver()` to simulate quantum behavior
- ✅ Interpreted partitioning in the context of hospital response
