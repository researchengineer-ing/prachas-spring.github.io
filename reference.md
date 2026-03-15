# Spring 2026 Research Lines — Deep Dive with Parallel Fundamentals

> _Each research line maps: **What to study** → **Foundations to learn in parallel** → **Courses** → **Key papers** → **Communities & venues**_  
> _Following the Karpathy method: go depth-first, build from scratch, foundations are non-negotiable_

---

## 1. LLM Interpretability & Alignment

> **Goal:** Find new ideas and hypotheses at the intersection of interpretability + teleodynamics / representation engineering + SSMs / causality

### What to study in depth

| Topic | Description |
|-------|-------------|
| Mechanistic interpretability | Circuits, superposition, sparse autoencoders (SAEs), probing, causal tracing |
| Representation engineering | Steering vectors, activation patching, concept erasure, linear probes |
| Alignment theory | RLHF, DPO, constitutional AI, reward hacking, scalable oversight |
| Teleodynamics connection | Information-theoretic view of internal representations; how do LLMs form "attractors"? |

### Foundations to learn in parallel

| Foundation | Why it matters | Course |
|-----------|---------------|--------|
| Information theory | KL divergence, mutual information for understanding representations | Stanford STATS 311 (Duchi) · UIUC ECE 563 |
| Linear algebra + SVD | SAEs decompose activations; singular value structure of weight matrices | Stanford EE 263 · CMU 10-606 |
| Causal inference basics | Causal tracing is intervention-based; do-calculus formalizes "what if we ablate?" | Columbia COMS W4775 (Bareinboim) |
| Statistical learning theory | Generalization bounds explain what representations can/cannot encode | NYU CSCI-GA 2566 (Mohri) · Stanford CS 229M (Ma) |
| Dynamical systems | Teleodynamics frames representations as emergent attractors in a dynamical system | UIUC ECE 528 (Nonlinear Systems) |

### Courses

| Course | University | Why |
|--------|-----------|-----|
| CS 294-267 — Understanding LLMs: Foundations & Safety | Berkeley (D. Song) | Core LLM safety + interpretability |
| COMS 6998 — Theoretical Foundations of LLMs | Columbia (D. Hsu) | Mathematical theory of what LLMs learn |
| CMSC 848R — Language Model Interpretability | UMD | Dedicated interp course |
| CSCI-GA 3033 — Building LLM Reasoners | NYU (G. Durrett) | FlashAttention, SFT, RL for reasoning |
| MT875 — Mechanistic Interpretability | Boston College (E. Grigsby) | Geometry of neural nets + circuits |
| LLM Interpretability Seminar | Tel Aviv (M. Geva) | [github.com/mega002/llm-interp-tau](https://github.com/mega002/llm-interp-tau) |

### Programs & communities

| Program | Format | Link |
|---------|--------|------|
| **MATS** — ML Alignment Theory Scholars | 12 weeks, Berkeley; mentors: Neel Nanda (DeepMind), ARC, MIRI, Anthropic researchers | [matsprogram.org](https://www.matsprogram.org/) |
| **ARENA** — Alignment Research Engineer Accelerator | 5 weeks London (ARENA 8.0: May–Jun 2026); free 5-chapter curriculum online | [arena.education](https://www.arena.education/) |
| **AI Safety Camp** | 14 weeks, part-time online | [aisafety.camp](https://www.aisafety.camp/) |
| **Redwood MLAB** | 3 weeks intensive, Berkeley | [redwoodresearch.org](https://www.redwoodresearch.org/) |
| Mech Interp Workshop @ NeurIPS 2025 | Workshop | [mechinterpworkshop.com](https://mechinterpworkshop.com/) |
| Mech Interp Workshop @ ICML 2024 | Workshop (140+ submissions) | [icml2024mi.pages.dev](https://icml2024mi.pages.dev/) |

### Key starting papers

| Paper | Why |
|-------|-----|
| Elhage et al., "Toy Models of Superposition" (Anthropic 2022) | Foundation of how features are stored in neural networks |
| Conmy et al., "Towards Automated Circuit Discovery" (2023) | Algorithmic approach to finding circuits |
| Bricken et al., "Towards Monosemanticity" (Anthropic 2023) | SAEs applied to language models at scale |
| Templeton et al., "Scaling Monosemanticity" (Anthropic 2024) | Scaling SAE interpretability to Claude 3 Sonnet |
| Nanda & Lieberum, "A Mechanistic Interpretability Analysis of GPT-2" | TransformerLens-based circuit analysis |

---

## 2. Diffusion & Flows

> **Goal:** Find new ideas and hypotheses; explore manifold and geometrical connections

### What to study in depth

| Topic | Description |
|-------|-------------|
| Score-based generative models | Score matching, Langevin dynamics, denoising diffusion (DDPM, DDIM) |
| Continuous normalizing flows | Neural ODEs, flow matching, conditional flow matching |
| Riemannian diffusion | Diffusion processes on manifolds (spheres, hyperbolic spaces, SO(3)) |
| Optimal transport | Wasserstein distances, Monge-Ampère, Schrödinger bridges |

### Foundations to learn in parallel

| Foundation | Why it matters | Course |
|-----------|---------------|--------|
| Stochastic calculus & SDEs | Diffusion = solving an SDE forward/backward; score function guides the reverse SDE | Columbia IEOR E6711/6712 · UIUC STAT 551/552 |
| Differential geometry & manifolds | Riemannian metrics, geodesics, curvature — needed for diffusion on non-Euclidean spaces | NYU CSCI-GA 3033 (Bruna) · UIUC ECE 557 |
| Measure theory & probability | Girsanov theorem, change of measure — core to understanding likelihood in diffusion models | Stanford STATS 310A/B |
| Optimal transport | Monge maps connect flows to transport; Wasserstein geometry is the right metric space | Columbia COMS 4995 (Blumberg) |
| ODE/PDE theory | Continuous normalizing flows solve ODEs; probability flow ODE connects score to sampling | Columbia COMS 4995 (Beigi) |

### Courses

| Course | University | Why |
|--------|-----------|-----|
| CS 236 — Deep Generative Models | Stanford (Ermon/Grover) | Full family: VAEs → flows → diffusion → score-based |
| 10-799 — Diffusion Models & Flow Matching (Sp2026) | CMU | New dedicated course |
| ECE 598 — Generative Modeling w/ Diffusion & Flow | UIUC | Dedicated offering |
| COMP760 — Geometry & Generative Models | McGill/Mila (J. Bose) | **Only course** covering Riemannian score-based models |
| CS 294-158 — Deep Unsupervised Learning | Berkeley (Abbeel) | Broad generative coverage |
| CSCI-GA 3033 — Mathematics of Deep Learning | NYU (Bruna) | Information geometry + optimal transport foundations |

### Key venues & communities

| Venue | Link |
|-------|------|
| **GRaM Workshop** — Geometry-grounded Representation & Generation @ ICLR 2026 / ICML 2024 | [gram-workshop.github.io](https://gram-workshop.github.io/) |
| NeurReps Workshop @ NeurIPS | Symmetry, geometry, and neural representations |
| DiffGeo4DL Workshop | Differential geometry for deep learning |

### Key researchers & papers

| Researcher | Contribution |
|-----------|-------------|
| Yang Song (OpenAI) | Score-based generative models through SDEs |
| Valentin De Bortoli (CNRS/ENS Paris) | Riemannian score-based generative modeling |
| Emile Mathieu (Cambridge) | Diffusion on manifolds (SO(3), hyperbolic) |
| Yaron Lipman (Meta/Weizmann) | Flow matching, conditional flow matching |
| David Duvenaud (Toronto) | Neural ODEs, continuous normalizing flows |
| Joey Bose (McGill/Mila) | Geometry and generative models |

---

## 3. Continual Learning

> **Goal:** Explore and progress; shape the idea around **Causality + SSL → Continual Learning**

### What to study in depth

| Topic | Description |
|-------|-------------|
| Catastrophic forgetting | EWC, SI, PackNet, progressive nets — why neural nets forget |
| Replay & pseudo-rehearsal | Experience replay, generative replay (DER, LUMP) |
| SSL for CL | Self-supervised pre-training as a foundation for continual representation learning |
| Causal mechanisms for CL | Invariant causal mechanisms don't change across tasks → natural continual learning |
| Representation-level approaches | CRL hypothesis: if representations are causally-aligned, forgetting is reduced |

### Foundations to learn in parallel

| Foundation | Why it matters | Course |
|-----------|---------------|--------|
| Representation learning theory | Understanding what makes a representation transferable vs. task-specific | NYU DS-GA 1008 (LeCun) · Stanford CS 330 (Finn) |
| Causal inference | Invariant causal prediction (ICP) provides the mechanism-stability principle | Columbia COMS W4775 (Bareinboim) |
| SSL theory | Contrastive learning, non-contrastive (BYOL, VICReg), JEPAs — what do they encode? | Berkeley CS 294-158 (Abbeel) |
| Bayesian methods | Bayesian online learning, sequential updating, posterior approximation for CL | Columbia STAT GU4224 · CMU 10-624 |
| Information theory | Forgetting = information loss; mutual information bounds on representation quality | Stanford STATS 311 (Duchi) |

### Courses

| Course | University | Why |
|--------|-----------|-----|
| COMS 6998 — Continual Learning & Memory Models | Columbia (**R. Zemel**) | **Rare dedicated CL course** |
| DS-GA 3001 — Embodied Learning & Vision | NYU (**M. Ren**) | CL in embodied/world-model context |
| CS 330 — Deep Multi-Task & Meta Learning | Stanford (C. Finn) | CL within meta-learning framework |
| COMS W4775 — Causal Inference I | Columbia (Bareinboim) | Invariant mechanisms = CL foundations |
| DS-GA 1008 — Deep Learning (SSL section) | NYU (LeCun) | SSL/JEPA as CL-friendly representations |

### Key communities & venues

| Community | Link |
|-----------|------|
| **ContinualAI** — monthly seminars, paper repo, Avalanche library | [continualai.org](https://www.continualai.org/) |
| **Avalanche** — end-to-end CL library (EWC, SI, GEM, A-GEM, LwF, iCaRL, DER) | [avalanche.continualai.org](https://avalanche.continualai.org/) |
| ContinualAI Paper Repository | [github.com/ContinualAI/continual-learning-papers](https://github.com/ContinualAI/continual-learning-papers) |
| **CLVision Workshop** @ CVPR / ICCV (6th edition, ICCV 2025) | [sites.google.com/view/clvision2024](https://sites.google.com/view/clvision2024) |
| CL Workshop @ NeurIPS (running since 2016) | [neurips.cc](https://neurips.cc/) |

### Your hypothesis thread: Causality + SSL → CL

| Step | What to explore |
|------|----------------|
| 1 | ICP (Invariant Causal Prediction, Peters et al. 2016) — mechanisms stable across environments = stable across time |
| 2 | SSL pre-training (VICReg, I-JEPA) learns representations that are more "mechanism-aligned" than supervised |
| 3 | CRL (Causal Representation Learning) — if latent factors are causally disentangled, new tasks only modify downstream modules |
| 4 | **Your paper idea:** Show that CRL + SSL representations suffer less catastrophic forgetting because they isolate invariant mechanisms |
| 5 | Test on standard CL benchmarks (Split-CIFAR, Split-ImageNet, CORe50) with SSL pre-training + causal regularization |

---

## 4. Causal Representation Learning

> **Goal:** Explore and progress on CRL + Invariance + Foundation Models

### What to study in depth

| Topic | Description |
|-------|-------------|
| Identifiability of causal variables | When can we recover latent causal factors from observations? (Locatello et al., Hyvarinen et al.) |
| Interventional CRL | Using interventions (do-calculus) to learn causal representations |
| Invariant Risk Minimization (IRM) | Arjovsky et al. 2019 — environments as proxy for interventions |
| Causal abstraction | Mapping between micro and macro causal models |
| CRL + Foundation Models | Do LLMs / VLMs learn causal structure? How to enforce it? |

### Foundations to learn in parallel

| Foundation | Why it matters | Course |
|-----------|---------------|--------|
| Causal inference (Pearl) | do-calculus, identification, transportability — the formal language | Columbia COMS W4775 + 4995 (**Bareinboim**, 2-course sequence) |
| Nonlinear ICA | Identifiability theory (Hyvarinen) underpins most CRL results | Self-study: Hyvarinen et al. 2019 |
| Representation learning theory | What makes representations disentangled? β-VAE, DCI metrics | NYU DS-GA 1008 (LeCun) |
| Group theory & symmetries | Equivariant representations, group actions on latent spaces | NYU CSCI-GA 3033 (Bruna) · GDL Course (Bronstein) |
| Statistical learning theory | Sample complexity of causal discovery from finite interventions | NYU CSCI-GA 2566 (Mohri) |

### Courses

| Course | University | Why |
|--------|-----------|-----|
| COMS W4775 — Causal Inference I | Columbia (**Bareinboim**) | Pearl's framework: d-sep, do-calculus, backdoor/frontdoor |
| COMS 4995 — Causal Inference II | Columbia (**Bareinboim**) | Transportability, causal RL, counterfactual reasoning, CRL |
| COMS 4995 — Causal Trustworthy AI | Columbia (**Bareinboim**) | Causal reasoning for fairness |
| DS-GA 3001 — Causal Inference in ML | NYU (H. He) | ML-oriented causal methods |
| CSCI-GA 3033 — Mathematics of Deep Learning | NYU (J. Bruna) | Group theory, symmetry, geometry for representations |

### Key resources

| Resource | Link |
|----------|------|
| CausalAI Textbook (Bareinboim) — 3 modular tracks: Causal Decision-Making, Causal Generalization, Causal Generative Modeling | [causalai-book.net](https://causalai-book.net/) |
| Bareinboim ICML Tutorial on Causal RL | [crl.causalai.net](https://crl.causalai.net/) |
| Bareinboim courses on Coursicle | [coursicle.com/columbia/professors/Elias+Bareinboim](https://www.coursicle.com/columbia/professors/Elias+Bareinboim/) |
| C♥LM Workshop @ NeurIPS 2024 (Causality & Large Models) | [calm-workshop-2024.github.io](https://calm-workshop-2024.github.io/about/) |
| CRL Workshop @ NeurIPS 2023 | [neurips.cc](https://neurips.cc/) |

### Key researchers

| Researcher | Affiliation | Contribution |
|-----------|------------|-------------|
| **Elias Bareinboim** | Columbia | Pearl's hierarchy, causal RL, CRL textbook |
| **Bernhard Schölkopf** | MPI Tübingen | Causal representation learning pioneer |
| **Yoshua Bengio** | Mila | Causal-neural connection, meta-transfer |
| Sara Magliacane | Amsterdam | Interventional CRL, domain adaptation |
| Caroline Uhler | MIT | Causal discovery, optimal transport |
| Aapo Hyvarinen | Helsinki | Nonlinear ICA, identifiability for CRL |

---

## 5. Port-Hamiltonian System Dynamics

> **Goal:** How to turn Lyapunov stability into energy functions; connect to neural network training dynamics

### What to study in depth

| Topic | Description |
|-------|-------------|
| Hamiltonian mechanics | Energy conservation, symplectic structure, phase space |
| Port-Hamiltonian systems | Energy-based modeling with dissipation and external ports |
| Lyapunov stability → energy functions | V(x) as a "learned energy landscape"; stability ↔ convergence of representations |
| Neural ODEs + Hamiltonian structure | Constrain neural ODE dynamics to preserve physical structure |
| PINNs | Physics-informed loss functions for incorporating known dynamics |

### Foundations to learn in parallel

| Foundation | Why it matters | Course |
|-----------|---------------|--------|
| ODEs & PDEs | Hamiltonian systems are ODEs; understanding flow, fixed points, bifurcations | Columbia COMS 4995 (Beigi) |
| Nonlinear systems & Lyapunov theory | Lyapunov functions ARE energy functions — stability = energy dissipation | UIUC ECE 528 |
| Optimal control & calculus of variations | Hamilton-Jacobi-Bellman connects optimal control to Hamiltonian mechanics | UIUC ECE 553 |
| Riemannian geometry | Symplectic manifolds, Poisson brackets, geometric mechanics | UIUC ECE 557 (Geometric Control) |
| Energy-based models | LeCun's EBMs: energy function over configurations, inference = energy minimization | NYU DS-GA 1008 (LeCun) |

### Courses (no dedicated course — compose from these)

| Course | University | What it covers |
|--------|-----------|---------------|
| ECE 528 — Analysis of Nonlinear Systems | UIUC | **Lyapunov stability**, perturbation theory, input-to-state stability |
| ECE 553 — Optimum Control | UIUC | Calculus of variations, maximum principle, Hamilton-Jacobi-Bellman |
| ECE 557 — Geometric Control Theory | UIUC | Differential geometry, Lie groups, symplectic structure |
| 6.8210 — Underactuated Robotics | MIT (Tedrake) | Lyapunov analysis, trajectory optimization, energy shaping |
| DS-GA 1008 — Deep Learning | NYU (LeCun) | Energy-based models as a unifying framework |
| CMSC 838B — Differentiable Programming | UMD (M. Lin) | Neural ODEs, differentiable physics simulations |

### Key papers & resources

| Paper/Resource | Why |
|---------------|-----|
| Greydanus et al., "Hamiltonian Neural Networks" (NeurIPS 2019) | Foundational: learn Hamiltonian from data, conserve energy by construction |
| Cranmer et al., "Lagrangian Neural Networks" (2020) | Learn Lagrangian instead; more flexible coordinate choices |
| "Stochastic Port-Hamiltonian NNs" (arXiv 2025) | [arxiv.org/html/2603.10078](https://arxiv.org/html/2603.10078) — universal approximation with passivity guarantees |
| Cueto, "Port-metriplectic neural networks" (Springer 2023) | [link.springer.com](https://link.springer.com/article/10.1007/s00466-023-02296-w) — thermodynamics-informed ML |
| Berkenkamp et al., "Safe Model-based RL with Stability Guarantees" (NeurIPS 2017) | [las.inf.ethz.ch](https://las.inf.ethz.ch/files/berkenkamp17safe_model.pdf) — Lyapunov + RL |
| NeurIPS Workshop: ML & Physical Sciences | [neurips.cc/virtual/2024/workshop/84717](https://neurips.cc/virtual/2024/workshop/84717) |

### Your hypothesis thread: Lyapunov stability → energy functions

| Step | Exploration |
|------|------------|
| 1 | A Lyapunov function V(x) certifying stability IS an energy function — it decreases along trajectories |
| 2 | Port-Hamiltonian systems decompose dynamics into energy-storing + energy-dissipating + external port components |
| 3 | **Hypothesis:** Can we learn a Port-Hamiltonian structure for the *training dynamics* of neural networks? i.e., loss = energy, parameters = state, gradients = forces |
| 4 | If training dynamics are Port-Hamiltonian, the "energy" (generalization-aware loss) must decrease — gives stability guarantees |
| 5 | Connection to EBMs: the learned energy landscape of an EBM can be constrained to satisfy Lyapunov conditions → guaranteed convergence of inference |

---

## 6. JEPAs, Model-Based RL & Model Predictive Control

> **Goal:** Shape the idea; connect JEPAs as world models to MPC-style planning

### What to study in depth

| Topic | Description |
|-------|-------------|
| JEPA architecture | Joint Embedding Predictive Architecture — predict in latent space, not pixel space |
| World models for RL | Dreamer V1/V2/V3 (Hafner), IRIS, TD-MPC, MBPO |
| Model Predictive Control | Receding-horizon optimization over a learned dynamics model |
| Planning with learned models | CEM, MPPI, differentiable planning, latent-space planning |
| V-JEPA 2 as world model | LeCun's demonstration of V-JEPA for robotics (2025) |

### Foundations to learn in parallel

| Foundation | Why it matters | Course |
|-----------|---------------|--------|
| Optimal control & MPC | The formal framework: cost function, dynamics constraint, receding horizon | UIUC ECE 553 · MIT 6.8210 (Tedrake) |
| State space models | JEPAs learn latent state transitions; SSMs formalize this | Annotated S4 · UIUC ECE 555 |
| RL theory | MDPs, Bellman equations, model-based vs model-free tradeoffs | Berkeley CS 285 (Levine) · UIUC CS 542 (Jiang) |
| Energy-based models | JEPAs minimize an energy in latent space; EBMs are the general framework | NYU DS-GA 1008 (LeCun) |
| Dynamical systems | Fixed points, attractors, stability of learned dynamics | UIUC ECE 528 |

### Courses

| Course | University | Why |
|--------|-----------|-----|
| CS 185/285 — Deep RL (**Lectures 11–12: Model-Based RL**) | Berkeley (**S. Levine**) | Premier model-based RL course; HW4 implements MBRL |
| CS 224R — Deep RL (robotics focus) | Stanford (**C. Finn**) | Offline RL, meta-RL, sim-to-real |
| 10-703 — Deep RL & Control | CMU (K. Fragkiadaki) | Model-based/free RL, visual RL, embodied agents |
| DS-GA 1008 — Deep Learning | NYU (**Y. LeCun**) | JEPAs, EBMs, SSL — the source |
| DS-GA 3001 — Embodied Learning & Vision | NYU (**M. Ren**) | World models, 3D perception, CL for agents |
| 6.8210 — Underactuated Robotics | MIT (Tedrake) | Trajectory optimization, MPC, Lyapunov analysis |
| ECE 553 — Optimum Control | UIUC | Calculus of variations, HJB, LQG, differential games |
| CS 542 — Statistical RL | UIUC (**N. Jiang**) | Rigorous finite-sample MBRL theory |

### Key papers & resources

| Paper | Why |
|-------|-----|
| LeCun, "A Path Towards Autonomous Machine Intelligence" (2022) | [openreview.net](https://openreview.net/pdf?id=BZ5a1r-kVsf) — JEPA/H-JEPA proposal |
| Hafner et al., "DreamerV3" (2023) | State-of-the-art world model for model-based RL |
| Hansen et al., "TD-MPC2" (2024) | Temporal difference learning for MPC with learned models |
| Bardes et al., "V-JEPA" (Meta, 2024) | Video JEPA — prediction in latent space without reconstruction |
| Destrade et al., "JEPA-WM" (Dec 2025) | JEPA as world model — directly relevant to your COLM target |

### Your hypothesis thread: JEPA as world model + MPC

| Step | Exploration |
|------|------------|
| 1 | JEPAs learn a latent dynamics model by predicting future latent states |
| 2 | MPC requires: (a) a dynamics model, (b) a cost function, (c) a planning horizon |
| 3 | **Key question:** Can JEPA's latent space serve as the dynamics model for MPC, with the energy function as the cost? |
| 4 | Advantage over Dreamer: JEPA doesn't reconstruct observations → more abstract, compositional latent space |
| 5 | Challenge: MPC needs differentiable dynamics; JEPA's EMA target encoder creates a non-stationary target |
| 6 | Connection to H-JEPA: hierarchical planning = multi-timescale MPC in a hierarchical latent space |

---

## 7. State Space Models & Cognitive Modeling / Continual Learning

> **Goal:** Explore SSMs as cognitive architectures; connect to continual learning

### What to study in depth

| Topic | Description |
|-------|-------------|
| S4 / HiPPO / Mamba lineage | Linear recurrences, selective state spaces, hardware-efficient implementations |
| SSMs as memory systems | HiPPO = optimal online function approximation → natural memory mechanism |
| Mamba-2 / State Space Duality | Connection between SSMs and attention (SSD framework) |
| Cognitive modeling | SSMs as models of working memory, attention, and sequential decision-making |
| SSMs + Continual Learning | Can SSMs' recurrent state serve as a "memory" that doesn't catastrophically forget? |

### Foundations to learn in parallel

| Foundation | Why it matters | Course |
|-----------|---------------|--------|
| Linear dynamical systems | SSMs ARE linear dynamical systems with learned parameters | Stanford EE 263 (Boyd) |
| Signal processing & transforms | HiPPO uses Legendre/Laguerre polynomials; S4 uses FFT for parallelization | Columbia COMS 4995 (Beigi) · UIUC ECE 534 |
| Control theory | Observability, controllability, Kalman filtering — core SSM concepts | UIUC ECE 515 · ECE 555 |
| Approximation theory | HiPPO optimally approximates functions online — why? | Stanford STATS 310 · NYU CSCI-GA 2420 |
| Stochastic processes | Hidden Markov models, filtering, prediction — classical SSMs | Columbia IEOR E6711 · UIUC ECE 534 |

### Learning sequence (paper chain)

| Order | Paper | Year | Key idea |
|-------|-------|------|----------|
| 1 | HiPPO: Recurrent Memory with Optimal Polynomial Projections | NeurIPS 2020 | Online function approximation with orthogonal polynomials |
| 2 | LSSL: Combining Recurrent, Convolutional, and Continuous-Time Models | NeurIPS 2021 | Linear state space layers |
| 3 | S4: Efficiently Modeling Long Sequences with Structured State Spaces | ICLR 2022 | Diagonal + low-rank structure, FFT-based convolution |
| 4 | S4D: On the Parameterization and Initialization of Diagonal State Space Models | 2022 | Simplified diagonal version |
| 5 | Mamba: Linear-Time Sequence Modeling with Selective State Spaces | 2023 | Selection mechanism, hardware-aware scan |
| 6 | Mamba-2: State Space Duality (SSD) | ICML 2024 | [goombalab.github.io](https://goombalab.github.io/blog/2024/mamba2-part1-model/) |

### Resources

| Resource | Link |
|----------|------|
| **The Annotated S4** — canonical hands-on tutorial | [srush.github.io/annotated-s4](https://srush.github.io/annotated-s4/) |
| Goomba Lab Blog (Albert Gu, CMU) | [goombalab.github.io](https://goombalab.github.io/) |
| Visual Guide to Mamba & SSMs | [newsletter.maartengrootendorst.com](https://newsletter.maartengrootendorst.com/p/a-visual-guide-to-mamba-and-state) |
| Covered in CMU 10-707 (Advanced DL) | [cs.cmu.edu](https://www.cs.cmu.edu/) |
| Covered in UIUC CS 498 (ML Systems) | [illinois.edu](https://illinois.edu/) |

### Your hypothesis thread: SSMs as cognitive memory for CL

| Step | Exploration |
|------|------------|
| 1 | HiPPO's polynomial projection = optimal "compression" of history into finite state |
| 2 | This is naturally a continual learning mechanism: the state vector is a bounded-capacity memory |
| 3 | Unlike transformer KV-cache, SSM state integrates all history into a fixed-size vector |
| 4 | **Hypothesis:** SSM-based architectures may be naturally more resistant to catastrophic forgetting because their recurrent state acts as a compressed, incremental memory |
| 5 | Test: Compare Mamba vs. Transformer on continual learning benchmarks (task-incremental, class-incremental) |
| 6 | Connection to cognitive science: working memory capacity (~7±2 items) maps to SSM state dimension |

---

## 8. Quantitative Social Science / Econometrics / People Analytics

> **Goal:** Combine QMSS, data analytics, and advanced analytics into a strong quant-social research profile on top of MS DS

### What to study in depth

| Topic | Description |
|-------|-------------|
| Causal inference for social science | Potential outcomes, IV, RDD, diff-in-diff, synthetic control |
| Econometric methods | Panel data, GMM, structural models, treatment effects |
| Text as data | NLP for social science: topic models, sentiment, framing, stance detection |
| People analytics | Organizational network analysis, attrition models, workforce optimization |
| Survey methodology + ML | Multilevel regression, poststratification (MRP), Bayesian survey adjustment |

### Foundations to learn in parallel

| Foundation | Why it matters | Course |
|-----------|---------------|--------|
| Causal inference (both frameworks) | Rubin (potential outcomes) for experiments; Pearl (DAGs) for mechanism | Columbia COMS W4775 (Bareinboim) · Stanford STATS 209 |
| Bayesian statistics | Hierarchical models, MRP, posterior predictive checks | Columbia STAT GU4224 · CMU 10-624 |
| Time series & panel data | Most social science data is panel; need fixed/random effects, dynamic models | Columbia STAT GU4221 (Davis) |
| Network analysis | Social networks, influence propagation, community detection | Stanford CS 224W (Leskovec) |
| NLP foundations | Text processing, embeddings, topic models for social science text data | Stanford CS 224N (Manning) · NYU DS-GA 1015 |

### Courses

| Course | University | Why |
|--------|-----------|-----|
| MGTECON 634 — Causal Inference | Stanford (**S. Athey / G. Imbens**) | Gold standard for causal ML in economics |
| QMSS Program (full sequence) | Columbia | Quantitative methods for social science |
| STAT GR5235 — Applied Causal Inference | Columbia | Applied causal methods |
| DS-GA 1015 — Text as Data | NYU | NLP for social science |
| COMS W4775 — Causal Inference I | Columbia (Bareinboim) | Formal causal framework |
| STAT GU4221 — Time Series Analysis | Columbia (R. Davis) | Panel methods, forecasting |

### Key resources

| Resource | Link |
|----------|------|
| Athey & Imbens short course (free) — Causal ML for economics | [stanford.edu](https://stanford.edu/) |
| Wharton People Analytics Conference | [whartonpeopleanalytics.com](https://whartonpeopleanalytics.com/) |
| MIT People Analytics Research | [mit.edu](https://mit.edu/) |
| Angrist & Pischke, "Mostly Harmless Econometrics" | Textbook — the econometrics bible |
| Cunningham, "Causal Inference: The Mixtape" | Free online — accessible causal methods |

### Your profile integration: QMSS + DS + ML

| Component | What it adds |
|-----------|-------------|
| MS DS (Columbia) | ML, deep learning, optimization, systems |
| QMSS perspective | Causal inference, survey methods, social theory, mixed methods |
| Advanced analytics (Mu Sigma background) | Decision science, behavioral economics, agent-based modeling |
| **Combined profile** | Quantitative social scientist who can: build ML models + design causal studies + understand human behavior + deploy at scale |

---

## Cross-Cutting Dependencies Map

_Shows which foundations serve multiple research lines simultaneously:_

| Foundation | Research Lines It Serves |
|-----------|------------------------|
| **Causal inference (Bareinboim)** | Continual Learning · CRL · LLM Interp · Quant Social Science |
| **Information theory** | LLM Interp · Diffusion & Flows · SSMs · Continual Learning |
| **Dynamical systems / ODEs** | Port-Hamiltonian · JEPAs + MBRL · SSMs · Control Theory |
| **Riemannian geometry / manifolds** | Diffusion & Flows · CRL (symmetry) · Port-Hamiltonian (symplectic) |
| **Statistical learning theory** | LLM Interp · CRL · Continual Learning · SSMs |
| **Energy-based models (LeCun)** | JEPAs + MBRL · Port-Hamiltonian · Continual Learning · LLM Interp |
| **Optimal control / MPC** | JEPAs + MBRL · Port-Hamiltonian · SSMs |
| **Bayesian methods** | Continual Learning · Quant Social Science · CRL |
| **SSL theory** | Continual Learning · CRL · JEPAs |

> **Highest-leverage foundations to study first:**  
> 1. Causal inference (Bareinboim sequence) — serves 4 lines  
> 2. Dynamical systems + ODEs — serves 4 lines  
> 3. Information theory — serves 4 lines  
> 4. Energy-based models (LeCun) — serves 4 lines
