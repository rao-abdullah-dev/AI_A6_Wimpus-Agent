# 🧠 Dynamic Wumpus Logic Agent — AI Assignment 6

**Student:** Muhammad Abdullah  
**Roll No:** 24F-0683  
**Section:** BCS-4B  
**Course:** AI 2002 – Artificial Intelligence (Spring 2026)  
**University:** National University of Computer & Emerging Sciences, Chiniot-Faisalabad Campus

---

## 🔗 Live Demo & Links

| Resource | Link |
|---|---|
| 🌐 Live App (Vercel) | https://ai-a6-wimpus-agent.vercel.app/wumpus.html |
| 💼 LinkedIn Post | https://www.linkedin.com/posts/muhammad-abdullah-a95b16328_artificialintelligence-propositionallogic-ugcPost-7456061507961810944-jmCQ |
| 📁 GitHub Repo | https://github.com/rao-abdullah-dev |

---

## 📌 Project Overview

This project implements a **Web-based Dynamic Pathfinding Agent** that operates inside a **Wumpus World-style grid**. The agent acts as a **Knowledge-Based Agent (KBA)** — it perceives its environment, updates its Propositional Logic Knowledge Base, and uses **Resolution Refutation** to logically deduce safe cells before moving.

The entire application is a **single-file HTML/CSS/JavaScript** web app — no frameworks, no server needed. Just open `wumpus.html` in any browser.

---

## ⚙️ Features

- 🔲 **Dynamic Grid Sizing** — User defines Rows × Columns before each episode
- 💣 **Random Hazard Placement** — Pits (20% probability per cell) and one Wumpus placed randomly each episode
- 👃 **Percept Generation** — Breeze near Pits, Stench near Wumpus
- 🧠 **Propositional Logic KB** — Agent TELLs the KB new CNF clauses based on percepts
- 🔍 **Resolution Refutation Engine** — Agent ASKs KB if adjacent cells are safe before moving
- 🎨 **Grid Visualization** — Color-coded canvas: Green (Safe), Gray (Unknown), Red (Danger), Blue (Agent)
- 📊 **Real-Time Metrics** — Live display of Inference Steps and active Percepts

---

## 🧩 How the Inference Engine Works

### 1. CNF Conversion
All propositional sentences are stored in **Conjunctive Normal Form (CNF)**. When the agent perceives a Breeze at cell (x, y), the rule:

```
B_x_y ⟺ (P_n1 ∨ P_n2 ∨ ...)
```
is encoded as the CNF clause:
```
[~B_x_y, P_n1, P_n2, ...]
```

### 2. Resolution Refutation
To check if cell (nx, ny) is safe, the agent runs:
```
resolution("P_nx_ny")  // Is there a pit?
resolution("W_nx_ny")  // Is there a Wumpus?
```
The algorithm:
1. Negates the query and adds it as a unit clause
2. Tries all clause pairs looking for complementary literals
3. If an **empty clause** is derived → contradiction found → cell is **SAFE**
4. If no new clauses possible → cell safety **cannot be proven**

---

## 🚀 How to Run Locally

1. Download or clone this repository
2. Open `wumpus.html` in any web browser (Chrome, Firefox, Edge)
3. Set your desired grid size (Rows × Cols)
4. Click **Start** to initialize the environment
5. Click **Next Step** to advance the agent one move at a time

No installation, no dependencies, no server required.

---

## 📁 File Structure

```
AI_A6_24F-0683/
├── wumpus.html        # Complete web app (HTML + CSS + JS)
├── Report_24F-0683.pdf  # Comprehensive PDF report
└── README.md          # This file
```

---

## 🛠️ Technologies Used

- **HTML5 Canvas** — Grid visualization
- **Vanilla JavaScript** — Agent logic, KB, Resolution engine
- **CSS3** — Dark-themed responsive UI
- **Propositional Logic** — Knowledge representation
- **Resolution Refutation** — Automated theorem proving

---

## 📚 Topics Covered (AI 2002 Assignment 6)

- Knowledge-Based Agents
- Propositional Logic — Syntax & Semantics
- Entailment & Inference Rules
- Conjunctive Normal Form (CNF)
- Propositional Resolution
- Model Checking

---

*Submitted for AI 2002 – Artificial Intelligence, Spring 2026*
