# REU-2025-AIRobotics-HandsOn-Stiles

## 📌 Project Overview
This project simulates a post-earthquake hospital rescue scenario that explores how digital twins, multi-agent coordination, and quantum-enhanced optimization can support real-time decision-making. A Neo4j-based knowledge graph models agents, patients, environmental hazards, and tasks—providing the foundation for running simulations and applying quantum algorithms for task assignment and routing. As a part of this assignment, I also trained AI models, and I learned about how to code some classic problems.
---

## ✅ Task Progress

### Task 1: Knowledge Graph Modeling
- **What I did:** Designed and imported a multi-part knowledge graph into Neo4j using `.csv` files and a Cypher script. Nodes included agents (robots, medics), tasks (triage, delivery), patients, and environment entities (rooms, hazards).
- **Status:** Complete. 
- **Challenge:** Honestly, the entire thing was a challenge. Learning how to graph in Neo4J, set up the csv files for it, learn how to connect nodes, learn how to take the generated cypher and turn it into a graphml that is useable for Task 4. Everything gave me trouble.

### Task 2: Dynamic Programming Practice
- **What I did:** Solved the classic problems of Longest Increasing Subesquence, 0/1 Knapsack, and Edit Distance.
- **Status:** Complete.
- **Challenge:** There was really not much challenge here. I had never heard of these problems before, so I just had to learn more about them, but it wasn't too challenging after that.

### Task 3: Reinforcement Learning with Gymnasium
- **What I did:** Trained CartPole-v1 to successfully move 500 steps consistently. Did 1000 iterations.
- **Status:** Complete.
- **Challenge:** I did not know the functionality of CartPole going into this, and I have never trained an AI model before. All of it wasn't too hard once I learned more about how CartPole worked, and it was very interesting to me.

### Task 4: Quantum Optimization with Graph Input
- **What I did:** Attempted to use Qiskit for QUBO modeling but faced severe package compatibility issues. Switched to D-Wave Ocean SDK for Max-Cut modeling using my graph structure.
- **Status:** Complete.
- **Challenge:** Qiskit’s recent library conflicts made QAOA or QUBO modeling nearly impossible on Colab. Pivoted to D-Wave for completion.

### Task 5: Literature Review
- **What I did:** Reviewed two relevant papers:
  - *A Factor Graph Model of Trust for Collaborative MAS* – informed my trust-based coordination modeling.
  - *Quantum-Enhanced Digital Twin IoT for Healthcare* – supported my digital twin architecture and justified secure data pipelines.
- **Status:** Complete.
  
---

## 💡 Key Insights & Challenges

- **Neo4j integration was very challenging, but was and will be a very useful tool going forward:** The knowledge graph served as a flexible backbone for modeling dynamic trust-aware systems.
- **Quantum tools are fragile:** Real-world deployment of QAOA/QUBO models is heavily restricted by tooling compatibility. Simulations with D-Wave local solvers were a helpful workaround.
- **Digital twins need security + adaptability:** Drawing from the literature, I saw how important it is to protect digital twin data *and* keep the models reactive to change.
- **Trust is multi-dimensional:** Encoding behavioral trust (navigation accuracy, transparency, etc.) in graph form enabled me to imagine richer coordination schemes than simple rule-based routing.

---

## 🔍 Additional Exploration

- **Dynamic trust simulation:** In future work, I plan to simulate agents that adapt their trust values over time based on task success/failure, near-collisions, and path divergence.
- **Real-time feedback loop:** I envision a full loop where Unity simulations feed live updates into Neo4j, and optimization results get pushed back to guide agent behavior.
- **Expanded QUBO models:** I can convert more nuanced optimization tasks (e.g., task prioritization, triage queueing) into QUBO problems for quantum solvers.

---

## 📁 File Structure

- `neo4j_HospitalSim.cypher` – Cypher script to populate Neo4j  
- `agents.csv`, `tasks.csv`, `patients.csv`, etc. – Data model  
- `qubo_maxcut_demo.ipynb` – D-Wave simulation for QUBO  
- `Quantum_KG_Results.md` – Quantum modeling reflection  
- `Literature_Review.md` – Related work summaries (2 papers)  
- `README.md` – This file
