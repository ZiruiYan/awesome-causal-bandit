# Awesome-causal-bandit

[![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)



## What are causal bandit?
### TL;DR
A *causal bandit* is an extension of the classic multi-armed bandit (MAB) problem that incorporates the concept of causality to make better decisions in uncertain environment. A causal bandit aims to not only maximize rewards but also understand the causal relationships between actions and outcomes. This means it learns how different actions influence future outcomes, potentially leading to more informed, long-term decision-making.

Causal Bandit is defined over a Probabilistic Causal Model $\mathcal{G} = (V,E)$ where $V$ is the set of vertices and $E$ is the set of edges. A directed edge from node $i$ to node $j$ is denoted by ordered tuple $(i,j)$. The set of parents of node $i$ is denoted by ${\rm pa}_i$.


### Data Model
DAG $\mathcal{G}$ represents a Bayesian network, in which we denote the causal random variable associated with node $i\in V$ by $X_i$. The relationships amont the causal variables $X$ are specified by SEMSs:
$$X_i = f(X_{\rm pa(i)})+\epsilon_i, $$
where $\epsilon_i$ is some noise and $\rm pa(i)$ is the set of parents of node $i$ in $\mathcal{G}$.

### Reward
Without loss of generality, the sink node $X_N$ is defined as the reward node. The goal is to minimize the cumulative regret over horizon $T$:

$$E[R(T)] = T\mu_a^{*} - \sum_{t=1}^{T}\mu_{a(t)} \ .$$

### Key Assumptions
The papers can be grouped according to different assumptions.
(a) Extent of information aviliable about topology
(b) Extent of information about conditional distributions
(c) Nature of interventions (soft, hard, do)


## List of causal bandit papers
|Title|Venue|Intervention|Graph topology|Metric|Comment|Year|Materials|
|---|---|---|---|---|---|---|---|
|Linear Causal Bandits: Unknown Graph and Soft Interventions | NeurIPS| | | | | 2024 |[Paper](https://nips.cc/virtual/2024/poster/95325)|
|Partial Structure Discovery is Sufficient for No-regret Learning in Causal Bandits | NeurIPS| | | | | 2024 |[Paper](https://nips.cc/virtual/2024/poster/93277)|
|Improved Bound for Robust Causal Bandits with Linear Models | ISIT| | | | | 2024 |[Paper](https://arxiv.org/pdf/2405.07795v1)|
|Graph Identification and Upper Confidence Evaluation for Causal Bandits with Linear Models | ICASSP| | | | | 2024 |[Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10445823)|
|Causal Contextual Bandits with Adaptive Context | arXiv| | | | | 2024 |[Paper](https://arxiv.org/pdf/2405.18626)|
|Adversarial Causal Bayesian Optimization | ICLR| | | | | 2024 |[Paper](https://openreview.net/pdf?id=YcW8i9VCf5)|
|Model-based causal Bayesian optimization | ICLR| | | | | 2023 |[Paper](https://arxiv.org/pdf/2211.10257)|
|Combinatorial Pure Exploration of Causal Bandits| ICLR | | | | | 2023 |[Paper](https://openreview.net/forum?id=pBBsrPzq7aF)|
|Combinatorial causal bandits| AAAI | | | | | 2023 |[Paper](https://ojs.aaai.org/index.php/AAAI/article/view/25917)|
|Learning Good Interventions in Causal Graphs via Covering| UAI | | | | | 2023 |[Paper](https://dl.acm.org/doi/10.5555/3625834.3626005)|
|Combinatorial Causal Bandits without Graph Skeleton| arXiv | | | | | 2023 |[Paper](https://arxiv.org/abs/2301.13392)|
|Causal Bandits without Graph Learning| arXiv | | | | | 2023 |[Paper](https://arxiv.org/abs/2301.11401)|
|Additive Causal Bandits with Unknown Graph| ICML | | | | | 2023 |[Paper](https://dl.acm.org/doi/10.5555/3618408.3619393)|
|Causal bandits for linear structural equation models | JMLR| | | | | 2023 |[Paper](https://www.jmlr.org/papers/volume24/22-0969/22-0969.pdf)|
|Model-based causal Bayesian optimization| ICLR | | | | | 2023 |[Paper](https://iclr.cc/virtual/2023/oral/14239)|
|Robust Causal Bandits for Linear Models| arXiv | | | | | 2023 |[Paper](https://arxiv.org/abs/2310.19794)|
|A causal bandit approach to learning good atomic interventions in presence of unobserved confounders| UAI | | | | | 2022 |[Paper](https://proceedings.mlr.press/v180/maiti22a.html)|
|Adaptively exploiting d-separators with causal bandits | NeurIPS | | | | | 2022 |[Paper](https://proceedings.neurips.cc/paper_files/paper/2022/hash/801ec05b0aae9fcd2ef35c168bd538e0-Abstract-Conference.html)|
|Causal bandits without prior knowledge using separating sets | CLeaR| | | | | 2022 |[Paper](https://proceedings.mlr.press/v177/kroon22a.html)|
|Budgeted and non-budgeted causal bandits| AISTATS| | | | | 2021 |[Paper](https://proceedings.mlr.press/v130/nair21a.html)|
|Causal bandits with unknown graph structure| NeurIPS | | | | | 2021 |[Paper](https://proceedings.neurips.cc/paper/2021/hash/d010396ca8abf6ead8cacc2c2f2f26c7-Abstract.html)|
|Regret analysis of bandit problems with causal background knowledge| UAI| | | | | 2020 |[Paper](https://proceedings.mlr.press/v124/lu20a.html)|
|Structural Causal Bandits with Non-Manipulable Variables| AAAI | | | | | 2019 |[Paper](https://ojs.aaai.org/index.php/AAAI/article/view/4320)|
|Causal bandits with propagating inference| ICML | | | | | 2018 |[Paper](https://proceedings.mlr.press/v80/yabe18a.html)|
|Identifying best interventions through online importance sampling| ICML| | | | | 2017 |[Paper](https://proceedings.mlr.press/v70/sen17a.html)|
|Causal bandits: Learning good interventions via causal inference | NeurIPS| | | | | 2016 |[Paper](https://proceedings.neurips.cc/paper/2016/hash/b4288d9c0ec0a1841b3b3728321e7088-Abstract.html)|
|Bandits with unobserved confounders: A causal approach | NeurIPS| | | | | 2015 |[Paper](https://proceedings.neurips.cc/paper/2015/hash/795c7a7a5ec6b460ec00c5841019b9e9-Abstract.html)|


## Contact
Opening an issue or dropping me an email (yanz11@rpi.edu).
