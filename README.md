# DeciCore
# DeciCore — Decision Intelligence Core

DeciCore is a decision intelligence system that transforms raw data into actionable business decisions using simulation and uncertainty modeling. Unlike traditional machine learning systems that focus only on prediction, DeciCore focuses on answering the critical question: what should be done next?

---

## Overview

Most data systems generate insights but fail to translate those insights into concrete actions. DeciCore bridges this gap by evaluating multiple possible actions, simulating outcomes under uncertainty, and recommending the optimal decision along with a clear explanation.

The system is designed to be modular and extensible so it can integrate with different types of business data and decision scenarios.

---

## Key Features

- Data ingestion from structured sources (CSV for MVP, extensible to databases and APIs)
- Feature engineering layer to transform raw data into decision-ready inputs
- Decision engine that evaluates multiple possible actions
- Scenario simulation to account for uncertainty in predictions
- Explainability layer that provides reasoning behind each decision
- Action-oriented output with recommended steps
- Interactive dashboard for demonstration and exploration
- API-ready architecture for integration into real systems

---

## System Architecture

The system follows a modular pipeline:

Data Sources → Data Processing → Feature Engineering → Decision Engine → Simulation → Explanation → Output (UI/API)

Each component is designed to be independent, allowing easy extension and integration.

---

## Project Structure
DeciCore/
├── data/ # Data generation and ingestion
├── model/ # Predictive models (baseline regression)
├── decision_engine/ # Core decision logic and explanation
├── simulation/ # Uncertainty modeling and scenario simulation
├── dashboard/ # Streamlit-based UI
├── api/ # FastAPI endpoints (planned)
├── utils/ # Helper functions
├── notebook/ # Experiments and exploration
├── requirements.txt
├── README.md

---

## How It Works

1. Data is ingested and preprocessed.
2. A simple predictive model estimates outcomes (e.g., demand).
3. The decision engine evaluates multiple actions (e.g., increase price, decrease price).
4. A simulation layer introduces uncertainty to test robustness.
5. The system selects the optimal action based on expected outcomes.
6. An explanation layer provides reasoning for the selected decision.
7. Results are displayed via a dashboard or returned through an API.

---

## Example Use Case

Pricing Optimization:

- Input: current price, historical demand data
- Actions evaluated:
  - Increase price
  - Decrease price
  - Keep price constant
- Output:
  - Recommended pricing strategy
  - Expected revenue impact
  - Confidence and uncertainty estimates
  - Explanation of decision factors

---

## Getting Started

### 1. Install dependencies

```bash
pip install -r requirements.txt
2. Generate sample data
python data/generate_data.py
3. Run the dashboard
streamlit run dashboard/app.py
```
Current Scope (MVP)
Single-variable pricing decision system
Linear regression-based demand estimation
Basic rule-based decision evaluation
Monte Carlo-style uncertainty simulation
Streamlit dashboard for interaction

Future Enhancements
FastAPI integration for production-ready endpoints
Database connectors (PostgreSQL, cloud storage)
Multi-variable decision models
Reinforcement learning for sequential decisions
LLM-based natural language explanations
Multi-domain support (energy systems, supply chain, product analytics)
Design Principles
Decisions over predictions
Simplicity over unnecessary complexity
Modularity for extensibility
Transparency through explainability
Practical applicability to real-world problems


Author
Charan Kuragayala
Computational Data Science, Penn State University
