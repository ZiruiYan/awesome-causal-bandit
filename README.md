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
Nomally the last node $X_N$ is defined as reward. The goal is to minimize the cumulative regret over horizon $T$
$$E[R(T)] = T\mu_a^{*} - \sum_{t=1}^{T}\mu_{a(t)}$$

### Key Assumptions
(a) Extent of information aviliable about topology
(b) Extent of information about conditional distributions
(c) Nature of interventions (soft, hard, do)


## List of causal bandit papers
|Paper|Venue|Year|
|---|---|---|
|[Linear Causal Bandits: Unknown Graph and Soft Interventions](https://nips.cc/virtual/2024/poster/95325) | NeurIPS| 2024|
|[Partial Structure Discovery is Sufficient for No-regret Learning in Causal Bandits](https://nips.cc/virtual/2024/poster/93277) | NeurIPS| 2024|
|[Improved Bound for Robust Causal Bandits with Linear Models](https://arxiv.org/pdf/2405.07795v1) | ISIT| 2024|
|[Graph Identification and Upper Confidence Evaluation for Causal Bandits with Linear Models](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10445823) | ICASSP| 2024|
|[Causal Contextual Bandits with Adaptive Context](https://arxiv.org/pdf/2405.18626) | arXiv| 2024|
|[Adversarial Causal Bayesian Optimization](https://openreview.net/pdf?id=YcW8i9VCf5) | ICLR| 2024|
|[Model-based causal Bayesian optimization](https://arxiv.org/pdf/2211.10257) | ICLR| 2023|
|[Bandits with unobserved confounders: A causal approach](https://proceedings.neurips.cc/paper/2015/hash/795c7a7a5ec6b460ec00c5841019b9e9-Abstract.html) | NeurIPS| 2015|
|[Causal bandits: Learning good interventions via causal inference](https://proceedings.neurips.cc/paper/2016/hash/b4288d9c0ec0a1841b3b3728321e7088-Abstract.html) | NeurIPS| 2016|
|[Identifying best interventions through online importance sampling](https://proceedings.mlr.press/v70/sen17a.html)| ICML| 2017|
|[Regret analysis of bandit problems with causal background knowledge](https://proceedings.mlr.press/v124/lu20a.html)| UAI| 2020|
|[Budgeted and non-budgeted causal bandits](https://proceedings.mlr.press/v130/nair21a.html)| AISTATS| 2021|
|[Causal bandits with propagating inference](https://proceedings.mlr.press/v80/yabe18a.html)| ICML | 2018|
|[A causal bandit approach to learning good atomic interventions in presence of unobserved confounders](https://proceedings.mlr.press/v180/maiti22a.html)| UAI | 2022|
|[Combinatorial Pure Exploration of Causal Bandits](https://openreview.net/forum?id=pBBsrPzq7aF)| ICLR | 2023|
|[Combinatorial causal bandits](https://ojs.aaai.org/index.php/AAAI/article/view/25917)| AAAI | 2023|
|[Learning Good Interventions in Causal Graphs via Covering](https://dl.acm.org/doi/10.5555/3625834.3626005)| UAI | 2023|
|[Causal bandits with unknown graph structure](https://proceedings.neurips.cc/paper/2021/hash/d010396ca8abf6ead8cacc2c2f2f26c7-Abstract.html)| NeurIPS | 2021|
|[Adaptively exploiting d-separators with causal bandits](https://proceedings.neurips.cc/paper_files/paper/2022/hash/801ec05b0aae9fcd2ef35c168bd538e0-Abstract-Conference.html) | NeurIPS | 2022|
|[Causal bandits without prior knowledge using separating sets](https://proceedings.mlr.press/v177/kroon22a.html) | CLeaR| 2022|
|[Combinatorial Causal Bandits without Graph Skeleton](https://arxiv.org/abs/2301.13392)| arXiv | 2023 |
|[Causal Bandits without Graph Learning](https://arxiv.org/abs/2301.11401)| arXiv | 2023 |
|[Additive Causal Bandits with Unknown Graph](https://dl.acm.org/doi/10.5555/3618408.3619393)| ICML | 2023 | 
|[Causal bandits for linear structural equation models](https://www.jmlr.org/papers/volume24/22-0969/22-0969.pdf) | JMLR| 2023 |
|[Model-based causal Bayesian optimization](https://iclr.cc/virtual/2023/oral/14239)| ICLR | 2023 |
|[Robust Causal Bandits for Linear Models](https://arxiv.org/abs/2310.19794)| arXiv | 2023|


## Contact
Opening an issue or dropping me an email (yanz11@rpi.edu).
