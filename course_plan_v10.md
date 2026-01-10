# Foundations of Artificial Intelligence
## A First Principles Approach

> **Version 10** | 30 Classes | Agent-Centric Design

---

## Table of Contents

1. [Course Philosophy](#course-philosophy)
2. [Course Structure](#course-structure)
3. [Assessment Overview](#assessment-overview)
4. [Phase 1: Foundations (Classes 1-11)](#phase-1-foundations)
5. [Phase 2: Inference & Search (Classes 12-18)](#phase-2-inference--search)
6. [Phase 3: Sequential & Strategic (Classes 19-24)](#phase-3-sequential--strategic)
7. [Phase 4: Learning & RL (Classes 25-30)](#phase-4-learning--rl)
8. [Summary Tables](#summary-tables)

---

## Course Philosophy

### Core Pedagogical Framework

Every topic is framed through the **agent-modeling lens**:

```
APPLICATION → AGENT FRAMING → MODELING ASSUMPTIONS → TOOL SELECTION → TRADE-OFFS
```

For each class, students answer four questions:

| Question | Focus |
|----------|-------|
| **What is the agent?** | Decision-maker, learner, planner |
| **What is the environment?** | Deterministic, stochastic, adversarial, partially observable |
| **What information/actions are available?** | Full state, observations, action space |
| **What objective is the agent optimizing?** | Utility, reward, accuracy |

### Recurrent Themes

Tracked across the entire course:

- ⚖️ **Decision-making under uncertainty**
- 🔍 **Exploration vs exploitation**
- 📐 **Exact vs approximate methods**
- ⚔️ **Adversarial vs stochastic assumptions**
- 🖥️ **Computational constraints and bounded rationality**
- 📊 **Model assumptions and their consequences**

### Application Anchors

Used throughout to ground theory:

| Domain | Example Applications |
|--------|---------------------|
| 🎮 **Games** | Chess, Go, poker, board games |
| 💰 **Finance** | Portfolio allocation, risk, trading |
| 🤖 **Control** | Robotics, thermostats, autonomous systems |
| 📦 **Resources** | Scheduling, assignment, logistics |
| 🔄 **Sequential** | Medical treatment, inventory |

---

## Course Structure

### Time Budget Per Class

| Component | Duration | Notes |
|-----------|----------|-------|
| **Core lecture** | 1:30 | Must-cover material |
| **Buffer** | 0:30 | Discussion, questions, optional content |
| **Quiz** (when scheduled) | 0:20 | During buffer time |

### Homework Budget

| Situation | Average Time | Notes |
|-----------|--------------|-------|
| Regular classes | ~1:30 | Flexibility based on topic |
| Quiz week | Reduced | Quiz serves as reinforcement |
| First 4 classes | ~45-60 min | Adjustment period |
| Projects | Separate | Own timeline |

### Course Map

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                           COURSE ARCHITECTURE                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  PHASE 1: FOUNDATIONS          PHASE 2: INFERENCE & SEARCH                  │
│  Classes 1-11 (11 classes)     Classes 12-18 (7 classes)                    │
│  ─────────────────────────     ─────────────────────────                    │
│  1.  Introduction              12. Causality                                │
│  2.  Agents & Environments     13. Bayesian Inference                       │
│  3.  Logic                     14. Monte Carlo Sampling                     │
│  4.  Computation               15. Informed Search                          │
│  5.  Probability               16. Adversarial Search                       │
│  6.  Fat Tails                 17. Simulation-Based Planning                │
│  7.  Information Theory I      18. Classical Planning                       │
│  8.  Information Theory II                                                  │
│  9.  Optimization                                                           │
│  10. Prediction Taxonomy                                                    │
│  11. Decision Theory                                                        │
│                                                                              │
│  PHASE 3: SEQUENTIAL           PHASE 4: LEARNING & RL                       │
│  Classes 19-24 (6 classes)     Classes 25-30 (6 classes)                    │
│  ─────────────────────────     ─────────────────────────                    │
│  19. Constraints & Local       25. Learning Theory                          │
│  20. Markov Models & HMMs      26. Neural Networks                          │
│  21. MDPs I                    27. RL I - Foundations                       │
│  22. MDPs II                   28. RL II - TD Methods                       │
│  23. Game Theory I             29. RL III - Deep RL                         │
│  24. Game Theory II            30. Synthesis                                │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Assessment Overview

### Quizzes (9 Total)

| Quiz | After Class | Coverage | Focus |
|:----:|:-----------:|----------|-------|
| Q1 | 4 | Logic, Computation | Inference, complexity |
| Q2 | 8 | Probability, Information Theory | Bayesian reasoning, entropy |
| Q3 | 11 | Optimization, Decision Theory | Modeling, expected utility |
| Q4 | 14 | Inference Methods | Causal vs predictive, sampling |
| Q5 | 18 | Search and Planning | Method selection, trade-offs |
| Q6 | 22 | Sequential Decisions | Bellman, algorithms |
| Q7 | 24 | Game Theory | Equilibria, repeated games |
| Q8 | 27 | Learning, Neural Networks | Bias-variance, backprop |
| Q9 | 29 | Reinforcement Learning | TD, DQN, when to use RL |

**Format**: ~20 min, during buffer time, focus on modeling and trade-offs

### Projects (3 Total)

| Project | Assigned | Due | Focus |
|---------|:--------:|:---:|-------|
| **P1: Agent Modeling** | Class 11 | Class 16 | Full PEAS + state space + decision framework |
| **P2: Search/Planning** | Class 15 | Class 22 | Complex search or planning problem |
| **P3: Axelrod Tournament** | Class 24 | Class 30 | Strategy design for iterated games |

---

## Phase 1: Foundations

> **Classes 1-11** | Building the conceptual and mathematical foundations

---

### Class 1: Introduction and History of AI

#### Agent Framing
- **What is an intelligent agent?** Preview of the central abstraction
- **Why study AI?** Practical and intellectual motivations

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| What is intelligence? | 20 min | Natural vs artificial, definitions, Turing's question |
| Historical arc | 30 min | Turing → Dartmouth → Expert Systems → Winters → Renaissance |
| AI paradigms | 25 min | Symbolic, Connectionist, Statistical, Hybrid |
| Course preview | 15 min | Agent-centric view, Cursor as tool |

#### In-Class Exercise
> **"What would convince you?"**: Small group discussion on criteria for intelligence. Share and critique criteria.

#### Application Anchors
- Chess programs as historical milestone
- Expert systems in medicine (MYCIN)
- Modern LLMs as current frontier

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| AIMA | Ch.1 | Historical context |
| Turing (1950) | Full paper | Foundational thinking |

#### Homework (Light: ~45 min)

| Task | Time | Type |
|------|:----:|:----:|
| Write reflection: What would convince you something is intelligent? | 20 min | Reflection |
| Install Cursor, verify Python environment | 15 min | Setup |
| Skim AIFoundations Ch.1 | 10 min | Prep |

---

### Class 2: Agents and Environments

#### Agent Framing
This class defines the central abstraction: **the agent**. Everything builds on this.

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Agent abstraction | 25 min | Perceive → Decide → Act cycle |
| Environment properties | 25 min | Observable, Deterministic, Episodic, Static, Discrete |
| PEAS framework | 25 min | Performance, Environment, Actuators, Sensors |
| Agent architectures | 15 min | Reflex, Model-based, Goal-based, Utility-based |

#### In-Class Exercise
> **PEAS Analysis**: Given three systems (self-driving car, spam filter, chess engine), specify full PEAS in pairs. Compare and critique.

#### Application Anchors

| System | P | E | A | S |
|--------|---|---|---|---|
| Thermostat | Comfort + efficiency | Room, weather | Heater on/off | Temperature |
| Chess engine | Win/draw/loss | Board, opponent | Move selection | Board state |
| Trading bot | Returns, risk | Market, news | Buy/sell/hold | Prices |

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| AIMA | Ch.2 | Core framework |
| AIFoundations | Ch.1-2 | Alternative view |

#### Homework (Light: ~1 hr)

| Task | Time | Type |
|------|:----:|:----:|
| Full PEAS for 3 systems of your choice | 30 min | Reinforce |
| Review: graphs, BFS, DFS from algorithms | 20 min | Review |
| Classify 5 environments by properties | 10 min | Reinforce |

---

### Class 3: Logic - Reasoning with Certainty

#### Agent Framing
- **Agent**: Knowledge-based agent reasoning about its environment
- **Environment**: Fully observable, deterministic
- **Objective**: Derive true conclusions from known facts

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Why logic for agents? | 10 min | Knowledge representation, inference |
| Propositional logic | 35 min | Syntax, semantics, truth tables |
| Inference rules | 25 min | Modus ponens, And/Or elimination |
| Validity & satisfiability | 20 min | What can be proved, SAT preview |

#### In-Class Exercise
> **Wumpus World Logic**: Given partial observations, formalize in propositional logic and derive safe moves.

#### Application Anchors
- Wumpus World: Classic AI testbed
- Circuit verification: SAT in hardware
- Expert systems: Rule-based diagnosis

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| AIMA | Ch.7.1-7.4 | Core logic |
| AIFoundations | Ch.5.1-5.3 | Alternative |

#### Homework (Light: ~1 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 5 propositional logic exercises | 25 min | Reinforce |
| Formalize 2 scenarios in logic | 15 min | Reinforce |
| Read Jaynes Ch.1 "Plausible Reasoning" | 20 min | Prep |

---

### Class 4: Computation and Its Limits

#### Agent Framing
- **Agent**: Computational agent with finite resources
- **Key Question**: What can be computed? What's tractable?
- **Implication**: Bounded rationality is a necessity

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Finite automata | 15 min | Simplest model, limitations |
| Turing machines | 25 min | Universal computation, Church-Turing |
| Undecidability | 25 min | Halting problem |
| P vs NP | 25 min | Tractability, implications |

#### In-Class Exercise
> **Complexity Classification**: Classify 10 problems (sorting, SAT, TSP, etc.) by complexity class. Discuss implications for agents.

#### Application Anchors
- SAT solvers in AI planning
- Why chess is "solved" for small boards
- Why optimal planning is often intractable

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| Sipser | Ch.1 (automata) | Background |
| Sipser | Ch.4.2 (halting) | Undecidability |
| Sipser | Ch.7.3-7.4 | P, NP |

#### Homework (Light: ~1 hr)

| Task | Time | Type |
|------|:----:|:----:|
| Classify 8 problems by complexity | 30 min | Reinforce |
| Reflection: Why can't agents compute optimal solutions? | 15 min | Reinforce |
| Identify 3 AI tasks and complexity implications | 15 min | Reinforce |

#### 📝 QUIZ 1
> **Coverage**: Logic (Class 3), Computation (Class 4)  
> **Focus**: Inference, complexity classification, implications for agents

---

### Class 5: Probability as Extended Logic

#### Agent Framing
- **Agent**: Reasoning under uncertainty
- **Environment**: Stochastic, partially observable
- **Key Insight**: Probability extends logic to uncertainty (Jaynes)

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Why logic isn't enough | 15 min | Uncertainty is fundamental |
| Jaynes' desiderata | 25 min | What plausible reasoning must satisfy |
| Probability rules | 25 min | Sum rule, product rule—derived |
| Bayes' theorem | 25 min | Prior × Likelihood ∝ Posterior |

#### In-Class Exercise
> **Medical Diagnosis**: Compute posterior probability of disease given positive test. Discuss base rate neglect.

#### Application Anchors
- Medical diagnosis: Priors, test accuracy, posteriors
- Spam filtering: Naive Bayes
- Finance: Updating market beliefs

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| Jaynes | Ch.1-2 | Core philosophy |
| AIMA | Ch.12.1-12.3 | Standard treatment |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| Derive product rule from desiderata (guided) | 30 min | Reinforce |
| 6 Bayes' theorem problems | 40 min | Reinforce |
| Read Taleb excerpt on fat tails | 20 min | Prep |

---

### Class 6: When Assumptions Break - Fat Tails

#### Agent Framing
- **Agent**: Decision-maker relying on probabilistic models
- **Problem**: When standard assumptions fail
- **Objective**: Robust decisions despite model uncertainty

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Law of Large Numbers | 20 min | Convergence, when it applies |
| Central Limit Theorem | 25 min | Why Gaussians appear, assumptions |
| When CLT fails | 25 min | Fat tails, infinite variance, Cauchy |
| Implications | 20 min | Black Swans, robust decisions |

#### In-Class Exercise
> **Simulation Comparison**: Observe mean convergence for Gaussian vs Cauchy. Discuss implications.

#### Application Anchors
- **Finance**: Stock returns have fat tails
- **Insurance**: Catastrophic events
- **Networks**: Viral phenomena

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| Taleb | Selected sections | Core content |
| Supplementary | CLT review | Background |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Simulate LLN convergence (Gaussian vs Cauchy) | 30 min | Creation |
| 💻 Simulate CLT, then CLT failure | 30 min | Creation |
| Identify 3 fat-tailed phenomena | 20 min | Reinforce |
| Read MacKay Ch.2 | 10 min | Prep |

---

### Class 7: Information Theory I - Entropy

#### Agent Framing
- **Agent**: Learning agent acquiring information
- **Question**: How do we measure what the agent knows?
- **Connection**: Entropy quantifies uncertainty

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Surprise | 20 min | -log P(x): rare = informative |
| Entropy definition | 25 min | H(X) = E[surprise] |
| Properties | 25 min | Non-negative, max at uniform, zero at certainty |
| Conditional entropy | 20 min | H(X\|Y), chain rule |

#### In-Class Exercise
> **Twenty Questions**: How should an agent ask questions to identify an object? Connect to entropy maximization.

#### Application Anchors
- Communication: Shannon's channel capacity
- Decision trees: Split on max information gain
- Active learning: Query selection

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| MacKay | Ch.2 | Core |
| Cover & Thomas | Ch.2.1-2.4 | Depth |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| Entropy calculations (6 problems) | 40 min | Reinforce |
| Prove H(X\|Y) ≤ H(X) | 20 min | Reinforce |
| Design optimal 20-questions for 8 objects | 20 min | Reinforce |
| Read MacKay Ch.2.6-2.8 on KL | 20 min | Prep |

---

### Class 8: Information Theory II - Divergence and Compression

#### Agent Framing
- **Agent**: Learning agent comparing models to reality
- **Question**: How "wrong" is the agent's model?
- **Key Insight**: Learning is compression

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| KL divergence | 30 min | D(P\|\|Q) = "extra bits" using Q instead of P |
| Properties | 15 min | Non-negative, asymmetric, zero iff P=Q |
| Cross-entropy | 20 min | H(P,Q) = H(P) + D(P\|\|Q) |
| MDL principle | 25 min | Best model = shortest description |

#### In-Class Exercise
> **Model Comparison**: Given data and two models, compute cross-entropy. Which is better? Why?

#### Application Anchors
- ML: Cross-entropy loss
- Compression: Huffman, arithmetic coding
- Model selection: MDL

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| MacKay | Ch.2.6-2.8, Ch.4 | KL, compression |
| MDL book | Ch.1 | MDL principle |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| KL divergence problems (5) | 40 min | Reinforce |
| Cross-entropy model comparison | 20 min | Reinforce |
| Essay: Why is KL asymmetric? | 20 min | Reinforce |
| Read IntroOptim Ch.1-2 | 20 min | Prep |

#### 📝 QUIZ 2
> **Coverage**: Probability (5-6), Information Theory (7-8)  
> **Focus**: Bayesian reasoning, entropy, KL interpretation

---

### Class 9: Optimization - Landscapes and Intuition

#### Agent Framing
- **Agent**: Optimizer seeking best decisions
- **Environment**: Objective function landscape
- **Question**: How does the agent navigate?

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Optimization as agent problem | 15 min | Objective + constraints |
| Gradient descent | 25 min | Following the slope, step size |
| Convexity | 25 min | Why it matters (local = global) |
| Lagrangian | 25 min | Constraints, geometric intuition |

#### In-Class Exercise
> **Landscape Visualization**: Use Cursor to visualize gradient descent on convex bowl, saddle point, multiple minima.

#### Application Anchors
- Portfolio optimization (Markowitz)
- Resource allocation
- ML loss minimization

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| IntroOptim | Ch.1-2 | Foundations |
| DLBook | Ch.4.1-4.3 | ML view |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Visualize gradient descent on 2D surfaces | 40 min | Creation |
| Model 3 problems as optimization | 30 min | Reinforce |
| Lagrangian problems (2) | 20 min | Reinforce |

---

### Class 10: The Prediction Taxonomy

#### Agent Framing
- **Question**: How do we organize all prediction methods?
- **Framework**: Every method is a point in 5D space
- **Value**: Understanding the space > memorizing methods

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| The fundamental problem | 15 min | Infinite hypotheses, finite data |
| D1: Source | 20 min | Deductive / Inductive / Hybrid |
| D2: Probability | 15 min | Frequentist / Bayesian |
| D3: Objective | 20 min | E[Y\|X], P(Y\|X), P(Y\|do(X)) |
| D4-D5: Architecture & bias | 20 min | Structure, hypothesis restrictions |

#### In-Class Exercise
> **Method Mapping**: Map 5 methods (linear regression, decision tree, Bayesian network, causal model, neural network) to 5 dimensions.

#### Application Anchors
- Medical: Why causal vs predictive matters
- Finance: Forecasting vs intervention
- Recommenders: Associative vs causal

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| taxonomia_prediccion.md | Full | Core framework |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| Analyze 5 methods using 5 dimensions | 40 min | Reinforce |
| Example where each dimension choice matters | 20 min | Reinforce |
| Read DMUU Ch.3.1-3.3 | 30 min | Prep |

---

### Class 11: Decision Theory

#### Agent Framing
- **Agent**: Utility-maximizing decision-maker
- **Question**: Given beliefs and desires, what should the agent do?
- **Answer**: Maximize expected utility

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Preferences and utility | 20 min | What agents want, quantifying value |
| Axioms of rationality | 20 min | Transitivity, completeness, independence |
| Expected utility | 25 min | E[U] = Σ P(s) U(s) |
| Value of information | 25 min | When to gather more info |

#### In-Class Exercise
> **Medical Decision**: Model test vs treat decision. Compute optimal policy with prior, test accuracy, outcomes, costs.

#### Application Anchors
- Medical decisions: Test vs treatment
- Business: Market research value
- Engineering: Sensor deployment

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| DMUU | Ch.3 | Core |
| AIMA | Ch.16.1-16.3 | Standard |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 5 expected utility problems | 40 min | Reinforce |
| Value of information exercise | 30 min | Reinforce |
| Model a personal decision | 20 min | Reinforce |

#### 📋 PROJECT 1 ASSIGNED
> **Agent Modeling**: Full PEAS + state space + decision framework  
> **Due**: Class 16

#### 📝 QUIZ 3
> **Coverage**: Optimization (9), Prediction Taxonomy (10), Decision Theory (11)  
> **Focus**: Optimization modeling, method classification, expected utility

---

## Phase 2: Inference & Search

> **Classes 12-18** | Methods for inference, search, and planning

---

### Class 12: Causality

#### Agent Framing
- **Agent**: Decision-maker who must intervene, not just observe
- **Key Insight**: P(Y|X) ≠ P(Y|do(X))
- **Environment**: Structured by causal mechanisms

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Correlation ≠ causation | 15 min | Why observational data misleads |
| Structural Causal Models | 25 min | Variables, functions, graphs |
| do-calculus basics | 25 min | P(Y\|do(X)) vs P(Y\|X) |
| Confounding & adjustment | 25 min | Backdoor criterion |

#### In-Class Exercise
> **Simpson's Paradox**: Hospital survival rates. Draw causal graph, explain paradox, compute correct comparison.

#### Application Anchors
- Medical treatment: Drug trials
- Policy evaluation: Intervention effects
- Marketing: True advertising effect

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| CausalInference | Ch.1-3 | Core |
| AIFoundations | Ch.11 | Agent view |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| Identify confounders in 4 scenarios | 25 min | Reinforce |
| Draw causal graphs for 3 problems | 20 min | Reinforce |
| Apply backdoor criterion (2) | 25 min | Reinforce |
| Read Bishop Ch.1.2 | 20 min | Prep |

---

### Class 13: Bayesian Inference

#### Agent Framing
- **Agent**: Learning agent updating beliefs from evidence
- **Environment**: Partially observable
- **Objective**: Maintain accurate beliefs via optimal updating

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Bayes as learning | 20 min | Prior → Posterior via likelihood |
| Sequential updating | 20 min | Multiple observations |
| Bayesian networks | 25 min | Graphical structure, factorization |
| d-separation | 25 min | Reading independence from graphs |

#### In-Class Exercise
> **Belief Network**: Given diagnostic network, answer inference queries using d-separation and Bayes.

#### Application Anchors
- Medical diagnosis: Symptom networks
- Fault diagnosis: Industrial systems
- Spam filtering: Naive Bayes

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| Bishop | Ch.1.2, Ch.2.1 | Framework |
| AIMA | Ch.13.1-13.3 | Networks |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Implement sequential Bayesian updating | 30 min | Creation |
| Bayesian network exercises (d-sep, inference) | 35 min | Reinforce |
| Design Bayesian network for a domain | 25 min | Reinforce |

---

### Class 14: Monte Carlo Sampling Methods

#### Agent Framing
- **Agent**: Needs to compute expectations over complex distributions
- **Problem**: Exact computation intractable
- **Solution**: Approximate via sampling

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Monte Carlo idea | 15 min | Sample to estimate; LLN justification |
| When to sample | 15 min | High-dimensional, complex distributions |
| Rejection sampling | 20 min | Simple but wasteful |
| Importance sampling | 25 min | Focus samples; variance reduction |
| MCMC preview | 15 min | Sampling from complex distributions |

#### In-Class Exercise
> **Estimating π**: Monte Carlo estimate by sampling points. Discuss convergence rate.

#### Application Anchors
- Finance: Option pricing
- Physics: Particle simulations
- Bayesian: Posterior sampling

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| AIFoundations | Ch.9.7 | Methods |
| Bishop | Ch.11.1-11.2 | Sampling |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Monte Carlo integration (π, other integrals) | 35 min | Creation |
| Compare rejection vs importance sampling | 25 min | Creation |
| Read AIMA Ch.3.1-3.3 on search | 20 min | Prep |

#### 📝 QUIZ 4
> **Coverage**: Causality (12), Bayesian (13), Monte Carlo (14)  
> **Focus**: Causal vs predictive, updating, when to sample

---

### Class 15: Informed Search and Heuristics

#### Agent Framing
- **Agent**: Goal-based agent searching for solution
- **Environment**: Deterministic, fully observable state space
- **Challenge**: Space too large; need guidance

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| State space review | 10 min | States, actions, goals (BFS/DFS from HW) |
| Heuristics | 20 min | Domain knowledge as h(n) |
| A* algorithm | 30 min | f(n) = g(n) + h(n) |
| Admissibility | 20 min | h(n) ≤ h*(n) → optimality |
| Heuristic design | 10 min | Relaxation, patterns |

#### In-Class Exercise
> **Designing Heuristics**: For 8-puzzle, derive admissible heuristics. Compare search performance.

#### Application Anchors
- Navigation: GPS, robot planning
- Puzzles: 8-puzzle, Rubik's cube
- Games: Move ordering

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| AIMA | Ch.3.4-3.5 | A*, heuristics |
| Review | BFS, DFS (Class 2 HW) | Prerequisite |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Implement A* for grid pathfinding | 45 min | Creation |
| Design admissible heuristics for 2 problems | 25 min | Reinforce |
| Prove Manhattan distance admissible | 20 min | Reinforce |

#### 📋 PROJECT 2 ASSIGNED
> **Search/Planning Project**  
> **Due**: Class 22

---

### Class 16: Adversarial Search

#### Agent Framing
- **Agent**: Game-playing against intelligent opponent
- **Environment**: Two-player, zero-sum, perfect information
- **Assumption**: Opponent plays optimally (worst case)

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Game trees | 15 min | MAX and MIN nodes |
| Minimax algorithm | 25 min | Optimal vs optimal opponent |
| Alpha-beta pruning | 25 min | Same answer, less work |
| Evaluation functions | 15 min | When search is bounded |
| Trade-offs | 10 min | Depth vs breadth vs evaluation |

#### In-Class Exercise
> **Minimax by Hand**: Compute values on small tree, identify alpha-beta prunes.

#### Application Anchors
- Chess: Deep Blue, evaluation
- Checkers: Chinook
- Simple games: Tic-tac-toe

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| AIMA | Ch.5.1-5.3 | Core |
| AIFoundations | Ch.14.1-14.2 | Game playing |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Minimax + alpha-beta for Tic-Tac-Toe | 45 min | Creation |
| Trace alpha-beta on paper | 20 min | Reinforce |
| Design evaluation function | 25 min | Reinforce |

---

### Class 17: Simulation-Based Planning

#### Agent Framing
- **Agent**: Planner in complex domain where exact methods fail
- **Environment**: May be stochastic, large state space
- **Key Insight**: When you can't search exactly, simulate

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Limitations of exact | 10 min | When minimax/A* don't scale |
| Monte Carlo Tree Search | 35 min | Selection (UCB), expansion, simulation, backprop |
| Rollout policies | 15 min | Random vs informed |
| When to use simulation | 15 min | Stochastic, large action space |
| Comparison with exact | 15 min | Trade-offs |

#### In-Class Exercise
> **MCTS for Simple Game**: Walk through iterations. Compare to minimax. When does each win?

#### Application Anchors
- Go: AlphaGo's triumph
- Complex games: Hard evaluation
- Online planning: Real-time

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| MCTS Survey | Introduction | Core algorithm |
| AIMA | Ch.5.4 | Context |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Implement basic MCTS | 50 min | Creation |
| Compare MCTS vs minimax | 25 min | Creation |
| Essay: When prefer simulation over exact? | 15 min | Reinforce |

---

### Class 18: Classical Planning

#### Agent Framing
- **Agent**: Goal-directed planner with structured actions
- **Environment**: Deterministic, STRIPS representation
- **Key Insight**: Actions have structure search can exploit

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Planning vs search | 15 min | Why structure matters |
| STRIPS representation | 30 min | Preconditions, add/delete effects |
| Forward planning | 20 min | State-space search |
| Planning heuristics | 25 min | Relaxed problems |

#### In-Class Exercise
> **Blocks World**: Write STRIPS operators and trace forward planning.

#### Application Anchors
- Robotics: Task planning
- Logistics: Delivery planning
- Game AI: NPC behavior

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| AIMA | Ch.10.1-10.2 | Core |
| AIFoundations | Ch.6 | Agent view |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| Write STRIPS for new domain | 30 min | Reinforce |
| Trace forward planning | 25 min | Reinforce |
| Design planning heuristic | 15 min | Reinforce |
| Read AIMA Ch.6.1-6.3 on CSPs | 20 min | Prep |

#### 📝 QUIZ 5
> **Coverage**: Search (15), Adversarial (16), Simulation (17), Planning (18)  
> **Focus**: Method selection, heuristics, trade-offs

---

## Phase 3: Sequential & Strategic

> **Classes 19-24** | Agents reasoning over time and against others

---

### Class 19: Constraints and Local Search

#### Agent Framing
- **Agent**: Problem solver exploiting structure or escaping local optima
- **Trade-off**: Complete (backtracking) vs incomplete (local search)

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| CSP formulation | 20 min | Variables, domains, constraints |
| Constraint propagation | 20 min | Arc consistency |
| Local search | 20 min | Hill climbing |
| Escaping local optima | 20 min | Restarts, simulated annealing |
| Genetic algorithms | 10 min | Population-based |

#### In-Class Exercise
> **N-Queens**: Formulate as CSP. Apply arc consistency. Solve with local search. Compare.

#### Application Anchors
- Scheduling: Timetabling
- Circuit design: Placement
- Non-convex optimization

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| AIMA | Ch.6.1-6.4 | CSPs |
| AIMA | Ch.4.1 | Local search |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Solve N-Queens with local search | 40 min | Creation |
| Formulate 2 problems as CSPs | 20 min | Reinforce |
| Compare hill climbing vs SA | 30 min | Creation |

---

### Class 20: Markov Models and HMMs

#### Agent Framing
- **Agent**: Reasoning about sequential processes
- **Environment**: State evolves; may be hidden
- **Key Insight**: Markov property enables tractable reasoning

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Markov property | 15 min | Future ⊥ past \| present |
| Markov chains | 20 min | Transitions, stationary distributions |
| HMM definition | 20 min | Hidden states, observations |
| Forward algorithm | 20 min | P(observations) |
| Viterbi algorithm | 15 min | Most likely path |

#### In-Class Exercise
> **Robot Localization**: Model as HMM. Use forward algorithm to track belief.

#### Application Anchors
- Speech recognition
- Finance: Regime detection
- Biology: Gene finding

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| AIFoundations | Ch.9.6 | Sequential |
| Bishop | Ch.13.1-13.2 | HMMs |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Implement forward and Viterbi | 50 min | Creation |
| HMM exercises (3 problems) | 30 min | Reinforce |
| Read DMUU Ch.4.1-4.3 | 10 min | Prep |

---

### Class 21: MDPs I - Foundations

#### Agent Framing
- **Agent**: Sequential decision-maker
- **Environment**: Stochastic transitions, rewards
- **Objective**: Maximize cumulative discounted reward

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| MDP definition | 20 min | S, A, T, R, γ |
| Return and discounting | 15 min | Why discount? |
| Bellman equation | 30 min | V(s) recursive decomposition |
| Optimal value V* | 15 min | Bellman optimality |
| Policy | 10 min | States → actions |

#### In-Class Exercise
> **Gridworld MDP**: Define MDP. Write Bellman equations for several states.

#### Application Anchors
- Robotics: Navigation
- Finance: Portfolio over time
- Healthcare: Treatment sequences

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| DMUU | Ch.4.1-4.3 | Foundations |
| BartoSutton | Ch.3 | RL view |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| Derive Bellman equation (guided) | 25 min | Reinforce |
| MDP modeling (3 problems) | 35 min | Reinforce |
| Analyze discount factor effect | 15 min | Reinforce |
| Read BartoSutton Ch.4.1-4.3 | 15 min | Prep |

---

### Class 22: MDPs II - Algorithms

#### Agent Framing
- **Agent**: Computing optimal behavior
- **Question**: Given MDP, how find optimal policy?

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Value iteration | 30 min | Iterative Bellman, convergence |
| Policy iteration | 25 min | Evaluate then improve |
| Comparison | 15 min | When use which |
| Policy extraction | 10 min | V* → π* |
| Practical issues | 10 min | State space size |

#### In-Class Exercise
> **Value Iteration by Hand**: Small MDP (4-5 states). Iterate to convergence. Extract policy.

#### Application Anchors
- Inventory management
- Maintenance policies
- Stochastic games

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| BartoSutton | Ch.4.1-4.4 | DP |
| DMUU | Ch.4.4-4.5 | Algorithms |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Value iteration for gridworld | 45 min | Creation |
| Compare convergence with different γ | 20 min | Creation |
| Policy iteration by hand | 25 min | Reinforce |

#### 📝 QUIZ 6
> **Coverage**: Markov/HMMs (20), MDPs (21-22)  
> **Focus**: Sequential modeling, Bellman, algorithm selection

---

### Class 23: Game Theory I

#### Agent Framing
- **Agent**: Decision-maker among other agents
- **Environment**: Others also optimizing
- **Key Insight**: Best action depends on others

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Normal form games | 20 min | Players, strategies, payoffs |
| Dominant strategies | 15 min | Clear choices |
| Nash equilibrium | 30 min | Stable outcomes |
| Classic games | 15 min | Prisoner's Dilemma, coordination |
| Mixed strategies | 10 min | Randomization |

#### In-Class Exercise
> **Find Equilibrium**: 3 different games. Find Nash. Discuss efficiency vs stability.

#### Application Anchors
- Economics: Oligopoly
- Auctions: Bidding
- Security: Attack-defense

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| DMUU | Ch.8.1-8.3 | Basics |
| Axelrod | Introduction | Preview |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| Find Nash in 5 games | 40 min | Reinforce |
| Analyze Prisoner's Dilemma | 15 min | Reinforce |
| Design game with multiple equilibria | 15 min | Reinforce |
| Read Axelrod Ch.1-2 | 20 min | Prep |

---

### Class 24: Game Theory II - Repeated Games

#### Agent Framing
- **Agent**: Repeated interaction with same opponents
- **Question**: Does repetition change behavior?
- **Key Insight**: Shadow of the future enables cooperation

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Repeated games | 20 min | Why iteration matters |
| Folk theorem | 15 min | Cooperation sustainable |
| Strategies for IPD | 30 min | TFT, Grim Trigger, Pavlov |
| Axelrod's tournament | 15 min | Empirical findings |
| Evolution of cooperation | 10 min | Why "nice" wins |

#### In-Class Exercise
> **Strategy Design**: Propose IPD strategies. Discuss: nice? forgiving? retaliatory?

#### Application Anchors
- Business: Supplier relationships
- International: Treaties
- Biology: Evolution

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| Axelrod | Ch.1-3 | Core |
| DMUU | Ch.8.4 | Repeated |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| Design and test 2 IPD strategies | 40 min | Creation |
| Analysis: Why TFT works? When fails? | 25 min | Reinforce |
| Propose strategy beating TFT in specific env | 25 min | Reinforce |

#### 📋 PROJECT 3 ASSIGNED
> **Axelrod Tournament**: Strategy design  
> **Due**: Class 30

#### 📝 QUIZ 7
> **Coverage**: Game Theory (23-24)  
> **Focus**: Equilibria, repeated games, strategy properties

---

## Phase 4: Learning & RL

> **Classes 25-30** | Agents that learn from experience

---

### Class 25: Learning Theory

#### Agent Framing
- **Agent**: Learner that must generalize from finite data
- **Question**: When will learning succeed?
- **Key Insight**: Bias-variance trade-off is fundamental

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Learning as approximation | 15 min | Hypothesis space, target |
| Generalization | 20 min | Train vs test |
| Bias-variance tradeoff | 30 min | Fundamental tension |
| Overfitting & regularization | 25 min | Constraining complexity |

#### In-Class Exercise
> **Polynomial Fitting**: Fit degrees 1, 5, 15 to noisy data. Observe under/overfitting.

#### Application Anchors
- Any prediction: Model complexity
- Deep learning: Regularization
- Science: Model selection

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| DLBook | Ch.5.1-5.4 | Basics |
| ESL | Ch.2.1-2.4, Ch.7 | Bias-variance |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Demonstrate bias-variance empirically | 40 min | Creation |
| Model selection exercise | 25 min | Reinforce |
| Read DLBook Ch.6.1-6.3 | 25 min | Prep |

---

### Class 26: Neural Networks

#### Agent Framing
- **Agent**: Function approximator learning representations
- **Question**: How learn complex nonlinear functions?
- **Key Insight**: Composition yields expressive power

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Perceptron | 15 min | Simplest unit |
| Multilayer networks | 20 min | Composition, nonlinearity |
| Backpropagation | 30 min | Chain rule for gradients |
| Universal approximation | 15 min | What NNs can represent |
| Practical training | 10 min | Init, learning rate, batches |

#### In-Class Exercise
> **Backprop by Hand**: Small network (2-3-1). Forward and backward pass. Verify with autodiff.

#### Application Anchors
- Vision: Image classification
- Language: Text processing
- Games: Value/policy networks

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| DLBook | Ch.6.1-6.5 | Core |
| AIFoundations | Ch.8 | Agent view |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Implement feedforward network from scratch | 45 min | Creation |
| Backprop calculation by hand | 20 min | Reinforce |
| Read BartoSutton Ch.1-2 | 25 min | Prep |

---

### Class 27: RL I - Foundations

#### Agent Framing
- **Agent**: Learner acting and receiving rewards
- **Environment**: Unknown dynamics
- **Challenge**: No supervisor, delayed reward, exploration

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| RL problem | 15 min | Agent, environment, reward |
| Exploration vs exploitation | 20 min | Fundamental tradeoff |
| Multi-armed bandits | 30 min | Simplest RL |
| Bandit algorithms | 25 min | ε-greedy, UCB |

#### In-Class Exercise
> **Bandit Simulation**: 3 unknown slot machines. Decide which to pull. Track regret.

#### Application Anchors
- Clinical trials
- Advertising
- Recommendations

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| BartoSutton | Ch.1-2 | Foundations |
| AIFoundations | Ch.13 | Agent view |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Implement bandit algorithms | 45 min | Creation |
| Compare across environments | 20 min | Creation |
| When does exploration hurt short-term? | 25 min | Reinforce |

#### 📝 QUIZ 8
> **Coverage**: Learning (25), Neural Nets (26), RL Foundations (27)  
> **Focus**: Bias-variance, backprop, exploration-exploitation

---

### Class 28: RL II - Temporal Difference

#### Agent Framing
- **Agent**: Learning value functions without model
- **Question**: How learn when environment unknown?
- **Key Insight**: Bootstrap from estimates

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| TD idea | 20 min | Bootstrapping |
| TD(0) | 20 min | One-step TD |
| Q-learning | 30 min | Off-policy |
| SARSA | 20 min | On-policy |

#### In-Class Exercise
> **Q-learning Trace**: Small gridworld. Trace updates for several episodes. Observe propagation.

#### Application Anchors
- Games: Self-play
- Robotics: Model-free control
- Operations: Online learning

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| BartoSutton | Ch.5-6 | TD |
| DMUU | Ch.5 | Alternative |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Q-learning for gridworld | 45 min | Creation |
| Compare Q-learning vs SARSA | 20 min | Creation |
| Read BartoSutton Ch.9-10 | 25 min | Prep |

---

### Class 29: RL III - Deep RL

#### Agent Framing
- **Agent**: RL with neural network approximation
- **Challenge**: Scaling to large/continuous spaces
- **Key Insight**: Stability is hard

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Why function approximation | 15 min | Tabular doesn't scale |
| DQN | 30 min | Deep Q-networks |
| Stability tricks | 20 min | Experience replay, target networks |
| Policy gradient | 15 min | REINFORCE |
| Challenges | 10 min | Sample efficiency, stability |

#### In-Class Exercise
> **DQN Components**: Why each component? What happens without them?

#### Application Anchors
- Games: Atari, Go
- Robotics: Continuous control
- Operations: Complex management

#### Readings

| Source | Sections | Purpose |
|--------|----------|---------|
| BartoSutton | Ch.9-10 | Function approx |
| DQN paper | Selected | Key algorithm |

#### Homework (~1.5 hr)

| Task | Time | Type |
|------|:----:|:----:|
| 💻 Train DQN on CartPole | 50 min | Creation |
| Ablation: without experience replay? | 20 min | Creation |
| Essay: RL vs planning? | 20 min | Reinforce |

#### 📝 QUIZ 9
> **Coverage**: RL (27-29)  
> **Focus**: TD vs MC, Q-learning, DQN, when to use RL

---

### Class 30: Course Synthesis

#### Agent Framing
Connecting all threads: What does it mean to build intelligent agents?

#### Core Content (1:30)

| Topic | Time | Content |
|-------|:----:|---------|
| Course review | 25 min | The arc: Foundations → Methods → Sequential → Learning |
| Method selection guide | 20 min | When use which tool |
| Trade-offs synthesis | 15 min | Exact/approx, adversarial/stochastic, model-based/free |
| Axelrod Tournament | 15 min | Run, discuss results |
| What's next | 15 min | ML course connections, frontiers |

#### In-Class Activity
> **Axelrod Tournament**: Run strategies. Analyze winners. Why did they work?

#### Homework
None. Projects due.

---

## Summary Tables

### Complete Class Schedule

| # | Class | Phase | Quiz | Project |
|:-:|-------|:-----:|:----:|:-------:|
| 1 | Introduction | 1 | | |
| 2 | Agents & Environments | 1 | | |
| 3 | Logic | 1 | | |
| 4 | Computation | 1 | Q1 | |
| 5 | Probability | 1 | | |
| 6 | Fat Tails | 1 | | |
| 7 | Information Theory I | 1 | | |
| 8 | Information Theory II | 1 | Q2 | |
| 9 | Optimization | 1 | | |
| 10 | Prediction Taxonomy | 1 | | |
| 11 | Decision Theory | 1 | Q3 | P1 |
| 12 | Causality | 2 | | |
| 13 | Bayesian Inference | 2 | | |
| 14 | Monte Carlo Sampling | 2 | Q4 | |
| 15 | Informed Search | 2 | | P2 |
| 16 | Adversarial Search | 2 | | |
| 17 | Simulation-Based Planning | 2 | | |
| 18 | Classical Planning | 2 | Q5 | |
| 19 | Constraints & Local | 3 | | |
| 20 | Markov & HMMs | 3 | | |
| 21 | MDPs I | 3 | | |
| 22 | MDPs II | 3 | Q6 | |
| 23 | Game Theory I | 3 | | |
| 24 | Game Theory II | 3 | Q7 | P3 |
| 25 | Learning Theory | 4 | | |
| 26 | Neural Networks | 4 | | |
| 27 | RL I | 4 | Q8 | |
| 28 | RL II | 4 | | |
| 29 | RL III | 4 | Q9 | |
| 30 | Synthesis | 4 | | |

### Homework Type Legend

| Symbol | Type | Description |
|:------:|------|-------------|
| 💻 | Creation | Implement agents, models, simulations |
| 📖 | Reinforce | Consolidate current material |
| 📚 | Prep | Prepare for next class |

### Application Anchors by Domain

| Domain | Classes |
|--------|---------|
| 🎮 Games | 1, 16, 17, 23, 24, 28, 29 |
| 💰 Finance | 5, 6, 9, 11, 20, 21 |
| 🏥 Medical | 5, 11, 12, 13, 27 |
| 🤖 Robotics | 15, 18, 21, 29 |
| 📦 Resources | 9, 18, 19 |

### Key Design Decisions

| Decision | Rationale |
|----------|-----------|
| Agent framing every class | Core pedagogical philosophy |
| MCTS as separate class | Central to modern AI |
| Markov + HMMs combined | Natural progression |
| 9 quizzes | Spaced reinforcement |
| Light first 4 classes | Adjustment period |
| Homework categorized | Explicit purpose |

---

## References

### Primary Textbooks

| Abbreviation | Full Title |
|--------------|------------|
| AIMA | Artificial Intelligence: A Modern Approach |
| AIFoundations | AI: Foundations of Computational Agents |
| BartoSutton | Reinforcement Learning: An Introduction |
| DMUU | Decision Making Under Uncertainty |
| DLBook | Deep Learning (Goodfellow et al.) |
| ESL | Elements of Statistical Learning |
| Jaynes | Probability Theory: The Logic of Science |
| MacKay | Information Theory, Inference, and Learning |
| Sipser | Introduction to the Theory of Computation |

### Supplementary

- CausalInference: Elements of Causal Inference
- MDL book: Minimum Description Length Principle
- IntroOptim: Introduction to Optimization
- Axelrod: Evolution of Cooperation
- Taleb: Statistical Consequences of Fat Tails

---

*End of Course Plan v10*

