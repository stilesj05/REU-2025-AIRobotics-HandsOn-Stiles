# 🏥 Hospital Simulation Graph

## 📌 Objective
The goal of this project was to model a hospital rescue scenario as a graph using Neo4j and then reconstruct that graph in Python using `networkx`. The graph includes entities such as **agents**, **patients**, **tasks**, and **environmental objects**, along with their relationships and attributes like trust, assignment timestamps, and blocking status.

---

## 📁 Data Preparation
The original graph was built using **Neo4j Aura’s visual interface**. Node and relationship data were exported to five `.csv` files:
- `agents.csv`
- `patients.csv`
- `tasks.csv`
- `environment_entities.csv`
- `relationship.csv`

These files were then imported into a Google Colab notebook using `pandas`.

---

## 🧱 Graph Construction
Using `networkx`, a **directed graph** was constructed:
- Nodes were added with labels (`Agent`, `Patient`, `Task`, `Environment`) and custom attributes (e.g., trust scores).
- Edges were created using the `relationship.csv` file, preserving all metadata (relationship type, timestamps, etc.).

- The final graph was exported to `hospital_sim.graphml` which was later renamed for correct project purposes.

---

## 👁️ Visualization
A spring layout was used to visualize the graph. Nodes were color-coded by type:
- **Agents**: sky blue
- **Patients**: light green
- **Tasks**: coral
- **Environment entities**: plum

This provided an intuitive overview of the network structure.

---

## ✅ Summary
Overall, this project taught me:
- What attributes go into a knowledge graph
- How to construct csv files to contain said attributes
- How to import csv files to Neo4J Aura and construct a graph with it
- How to take the Neo4J graph cypher that it generated after drawing the graph, and using that to create the graph using python and NetowrkX simulations.

---

## 🧠 Relevance to Machine Learning and Quantum Computing

This hospital simulation graph serves as a foundation for exploring advanced coordination strategies in multi-agent systems, especially in dynamic and uncertain environments like disaster response. Here's how this work connects to broader ML and quantum research:

### 🤖 Machine Learning Applications
- **Trust Modeling:** Agent trust scores can be learned and updated over time using supervised or reinforcement learning based on successful task execution or communication reliability.
- **Task Allocation Optimization:** ML algorithms can be used to predict optimal agent-task assignments by learning from historical performance data, environmental context, or priority levels.
- **Anomaly Detection:** Machine learning models can analyze edge patterns, timestamps, or trust anomalies to detect malfunctioning agents or compromised communication pathways in real time.

### ⚛️ Quantum Computing Potential
- **Quantum-Enhanced Graph Optimization:** Quantum algorithms (e.g. QAOA or quantum walks) could be applied to optimize routing, scheduling, or resource allocation across the network graph far more efficiently than classical methods in large-scale scenarios.
- **Secure Coordination via Quantum Trust Graphs:** Quantum properties like entanglement could be used to encode trust relationships, enabling secure communication and coordination in adversarial environments.
- **Graph Encoding for Quantum ML:** The graph structure can be embedded into quantum states (via Pauli encodings, adjacency matrix encodings, etc.), enabling experimentation with quantum machine learning models for classification or clustering of agents, tasks, or threats.

### 📡 Digital Twins & Simulation
This graph directly supports the idea of a **digital twin** — a live, updatable virtual representation of the hospital rescue environment. It enables:
- Real-time simulation and decision testing
- Risk-free training for ML models
- Evaluation of trust-aware strategies before deploying to physical robots

---


