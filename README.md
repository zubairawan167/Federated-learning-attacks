# Federated Learning Attacks: A Curated FedRecSec Index

> **A curated, quality-filtered index of attacks, defenses, benchmarks, and reproducible codebases for security and privacy in Federated Recommender Systems (FedRS).**

[![Awesome](https://img.shields.io/badge/Awesome-FedRecSec-blue)](https://github.com/topics/awesome)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Last Updated](https://img.shields.io/badge/updated-September%202026-orange)](README.md)

Federated Recommender Systems promise personalization without centralizing user data — but the same decentralization that protects privacy also removes the server's ability to inspect what clients send. This makes FedRS structurally vulnerable to poisoning, backdoor, and inference attacks. This repository tracks that threat landscape and, critically, **only lists work you can actually run and reproduce**.

---

## 📌 Inclusion Criteria

Every entry in this repository must satisfy **both** of the following:

| # | Criterion | Rationale |
|---|-----------|-----------|
| **1** | **Public code available** | A paper without an implementation cannot be reproduced, benchmarked, or used as a baseline. Every `[Code]` link in this repository has been checked to resolve to a live, non-empty repository. |
| **2** | **Top-tier venue** | Peer-reviewed at a **CORE A\*/A conference** or a **Q1/Q2 journal** (JCR). arXiv preprints are included only when the work is widely cited or has been accepted at such a venue. |

Venue ranks are verified against the [CORE Conference Portal](https://portal.core.edu.au/conf-ranks/) and journal quartiles against [LetPub](https://www.letpub.com.cn/index.php?page=journalapp) / JCR. Where a paper appears both as a preprint and a proceedings version, the **venue of record** is listed.

**Legend:** 🔴 Attack · 🟢 Defense · 🔵 Benchmark/Framework · 📊 Survey

---

## 📖 Table of Contents

- [Surveys and Related Collections](#-surveys-and-related-collections)
- [Attack Models](#-attack-models)
  - [Targeted / Item-Promotion Poisoning](#targeted--item-promotion-poisoning)
  - [Untargeted / Availability Poisoning](#untargeted--availability-poisoning)
  - [Backdoor Attacks](#backdoor-attacks)
  - [Inference and Privacy Attacks](#inference-and-privacy-attacks)
- [Defense Strategies](#-defense-strategies)
- [Benchmarks and Frameworks](#-benchmarks-and-frameworks)
- [Datasets](#-datasets)
- [Evaluation Protocol](#-evaluation-protocol)
- [Threat Model Taxonomy](#-threat-model-taxonomy)
- [Contributing](#-contributing)
- [Citation](#-citation)

---

## 📊 Surveys and Related Collections

| Title | Venue | Year | Material |
|-------|-------|------|----------|
| Navigating Threats in Federated Recommender Systems: A Survey of Attack Models and Defense Strategies | Artificial Intelligence Review (Q1) | 2026 | [Paper](https://link.springer.com/article/10.1007/s10462-026-11579-6), [Repo](https://github.com/waqar-uestc/AttackDic) |
| Manipulating Recommender Systems: A Survey of Poisoning Attacks and Countermeasures | ACM Computing Surveys (Q1) | 2024 | [Repo](https://github.com/tamlhp/awesome-recsys-poisoning) |
| A Scenario-Oriented Survey of Federated Recommender Systems | TPAMI (under review) | 2025 | [Repo](https://github.com/SmilesLab-XJTU/Survey-FedRec) |
| A Collection of Research Papers on Federated Recommender Systems | — | 2025 | [Repo](https://github.com/XuanangD/FederatedRS) |
| Adversarial Attack and Defense on Recommender Systems | — | 2024 | [Repo](https://github.com/EdisonLeeeee/RS-Adversarial-Learning) |
| Awesome Federated Learning (papers + code) | — | 2026 | [Site](https://youngfish42.github.io/Awesome-FL/) |
| RSPapers — Recommender System Paper Collection | — | 2025 | [Repo](https://github.com/hongleizhang/RSPapers) |

---

## 🔴 Attack Models

### Targeted / Item-Promotion Poisoning

*Adversary goal: force specific items into as many users' top-K lists as possible.*

| Title | Affiliation | Venue | Rank | Year | Material |
|-------|-------------|-------|------|------|----------|
| Spattack: Subgroup Poisoning Attacks on Federated Recommender Systems | Beijing Univ. of Posts and Telecommunications | WWW | A\* | 2026 | [Paper](https://arxiv.org/abs/2507.06258), [Code](https://github.com/BUPT-GAMMA/Subgroup_Poison_Attack) |
| Preventing the Popular Item Embedding Based Attack in Federated Recommendations (PIECK) | Zhejiang Univ. | ICDE | A\* | 2024 | [Paper](https://arxiv.org/abs/2502.12958), [Code](https://github.com/junzhang-zj/PIECK) |
| Poisoning Attack on Federated Knowledge Graph Embedding | Hong Kong Polytechnic Univ. | WWW | A\* | 2024 | [Paper](https://dl.acm.org/doi/10.1145/3589334.3645422), [Code](https://github.com/jisooma/FKGEPoison) |
| An Optimization-Based Attack Framework Against SOTA Poisoning Defenses | Jilin Univ. | arXiv | — | 2024 | [Paper](https://arxiv.org/abs/2407.15267), [Code](https://github.com/Yuxin104/BreakSTOAPoisoningDefenses) |
| FedRecAttack: Model Poisoning Attack to Federated Recommendation | — | ICDE | A\* | 2022 | [Paper](https://ieeexplore.ieee.org/document/9835228), [Code](https://github.com/rdz98/FedRecAttack) |
| Poisoning Deep Learning Based Recommender Model in Federated Learning Scenarios | — | IJCAI | A\* | 2022 | [Paper](https://doi.org/10.24963/ijcai.2022/306), [Code](https://github.com/rdz98/PoisonFedDLRS) |
| HidAttack: An Effective and Undetectable Model Poisoning Attack to Federated Recommenders | UESTC | TKDE (Q1) | — | 2024 | [Paper](https://ieeexplore.ieee.org/document/10816078), [Code](https://github.com/waqar-uestc/HidAttack) |

### Untargeted / Availability Poisoning

*Adversary goal: degrade overall recommendation quality for all users.*

| Title | Affiliation | Venue | Rank | Year | Material |
|-------|-------------|-------|------|------|----------|
| FedAttack: Effective and Covert Poisoning Attack on Federated Recommendation via Hard Sampling | Tsinghua Univ. | KDD | A\* | 2022 | [Paper](https://dl.acm.org/doi/10.1145/3534678.3539119), [Code](https://github.com/wuch15/FedAttack) |
| UA-FedRec: Untargeted Attack on Federated News Recommendation | USTC | KDD | A\* | 2023 | [Paper](https://dl.acm.org/doi/10.1145/3580305.3599923), [Code](https://github.com/yjw1029/UA-FedRec) |
| Untargeted Attack against Federated Recommendation Systems via Poisonous Item Embeddings and the Defense | USTC | AAAI | A\* | 2023 | [Paper](https://ojs.aaai.org/index.php/AAAI/article/view/25611), [Code](https://github.com/yflyl613/FedRec) |
| Unveiling and Mitigating Untargeted Poisoning Attacks on Federated Knowledge Graph Embedding | — | WWW | A\* | 2026 | [Paper](https://dl.acm.org/doi/10.1145/3774904.3792117) |

### Backdoor Attacks

*Adversary goal: implant a trigger that produces attacker-chosen output while leaving clean accuracy intact.*

| Title | Affiliation | Venue | Rank | Year | Material |
|-------|-------------|-------|------|------|----------|
| Backdoor Federated Learning by Poisoning Backdoor-Critical Layers | Stony Brook Univ. | ICLR | A\* | 2024 | [Paper](https://openreview.net/pdf?id=AJBGSVSTT2), [Code](https://github.com/zhmzm/Poisoning_Backdoor-critical_Layers_Attack) |
| Focused Flip: Vulnerability of Backdoor Defenses for Federated Learning | UCLA | AAAI | A\* | 2023 | [Paper](https://ojs.aaai.org/index.php/AAAI/article/view/26393), [Code](https://github.com/jinghuichen/Focused-Flip-Federated-Backdoor-Attack) |

### Inference and Privacy Attacks

*Adversary goal: recover user interactions, attributes, or membership from shared updates.*

| Title | Affiliation | Venue | Rank | Year | Material |
|-------|-------------|-------|------|------|----------|
| RAIFLE: Reconstruction Attacks on Interaction-based Federated Learning with Adversarial Data Manipulation | Univ. of Massachusetts | PoPETs (Q1) | — | 2024 | [Paper](https://arxiv.org/abs/2310.19163), [Code](https://github.com/dzungvpham/raifle) |
| Interaction-level Membership Inference Attack Against Federated Recommender Systems | Univ. of Queensland | WWW | A\* | 2023 | [Paper](https://dl.acm.org/doi/10.1145/3543507.3583359) |
| Cocktail Party Attack: Breaking Aggregation-Based Privacy in FL | Meta AI | ICML | A\* | 2023 | [Paper](https://proceedings.mlr.press/v202/kariyappa23a.html), [Code](https://github.com/facebookresearch/cocktail_party_attack) |
| LANCE: Exploration and Reflection for LLM-based Textual Attacks on News Recommender Systems | — | — | — | 2025 | [Code](https://github.com/Go0day/LANCE) |
| Privacy Risks of LLM-Empowered Recommender Systems: An Inversion Attack Perspective | — | — | — | 2024 | [Code](https://github.com/huiminzeng/gpt-fedrec) |

---

## 🟢 Defense Strategies

| Title | Approach | Affiliation | Venue | Rank | Year | Material |
|-------|----------|-------------|-------|------|------|----------|
| User Consented Federated Recommender System Against Personalized Attribute Inference Attack | Consent-aware training | HKUST | WSDM | A\* | 2024 | [Paper](https://dl.acm.org/doi/10.1145/3616855.3635830), [Code](https://github.com/hkust-knowcomp/uc-fedrec) |
| FedDefender: Client-Side Attack-Tolerant Federated Learning | Client-side robustness | Microsoft Research Asia | KDD | A\* | 2023 | [Paper](https://arxiv.org/pdf/2307.09048), [Code](https://github.com/deu30303/FedDefender) |
| Dual Personalization on Federated Recommendation (PFedRec) | Personalization as defense | Univ. of Technology Sydney | IJCAI | A\* | 2023 | [Paper](https://arxiv.org/abs/2301.08143), [Code](https://github.com/Zhangcx19/IJCAI-23-PFedRec) |
| CoLR: Communication-Efficient and Secure FedRec via Low-Rank Training | Low-rank update masking | VinUniversity | arXiv | — | 2024 | [Paper](https://arxiv.org/pdf/2401.03748), [Code](https://github.com/NNHieu/CoLR-FedRec) |
| Parameter Transmission-Free Federated Recommender System (PTF-FedRec) | No gradient sharing | Univ. of Queensland | arXiv | — | 2024 | [Paper](https://arxiv.org/pdf/2311.14968), [Code](https://github.com/hi-weiyuan/PTF-FedRec) |
| Federated Recommendation with Additive Personalization (FedRAP) | Additive decomposition | VinUniversity | ICLR | A\* | 2024 | [Paper](https://arxiv.org/pdf/2401.03748v1), [Code](https://github.com/mtics/FedRAP) |
| FedRoLA: Robust FL Against Model Poisoning via Layer-based Aggregation | Layer-wise robust agg. | — | KDD | A\* | 2024 | [Paper](https://dl.acm.org/doi/10.1145/3637528.3671906), [Code](https://github.com/GYan58/KDD-2024-FedRoLA) |
| Trust-GRS: Trustworthy Training Framework for GNN Recommenders Against Shilling Attacks | Trust-aware GNN | Chinese Academy of Sciences | — | — | 2024 | [Code](https://github.com/IIE-MLY/Trsut-GRS) |
| RFRec: Efficient and Robust Regularized Federated Recommendation | Robust regularization | — | CIKM | A\* | 2024 | [Paper](https://dl.acm.org/doi/10.1145/3627673.3679682), [Code](https://github.com/Applied-Machine-Learning-Lab/RFRec) |
| CLOUD: Privacy-Preserving Sequential Recommendation with Collaborative Confusion | Collaborative confusion | — | TOIS | A\* | 2025 | [Paper](https://dl.acm.org/doi/full/10.1145/3707204), [Code](https://github.com/weiwang0927/CLOUD) |
| FedMF: Secure Federated Matrix Factorization | Homomorphic encryption | — | IEEE Intelligent Systems (Q2) | — | 2021 | [Paper](https://ieeexplore.ieee.org/document/9162459), [Code](https://github.com/Di-Chai/FedMF) |
| FedPerGNN: Federated Graph Neural Network for Privacy-Preserving Personalization | Privacy-preserving GNN | — | Nature Communications (Q1) | — | 2022 | [Paper](https://www.nature.com/articles/s41467-022-30714-9), [Code](https://github.com/wuch15/FedPerGNN) |
| PFGNNPlus: Personalized Federated GNN for Item-to-Item Recommendation | Personalized GNN | Univ. of Illinois Chicago | arXiv | — | 2023 | [Paper](https://arxiv.org/abs/2306.03191), [Code](https://github.com/zfan20/PFGNNPlus) |

---

## 🔵 Benchmarks and Frameworks

### Poisoning-Specific Benchmarks

| Name | Scope | Material |
|------|-------|----------|
| **FLPoison** | Benchmarking poisoning attacks and defenses in FL — unified attack/defense implementations | [Code](https://github.com/vio1etus/FLPoison) |
| **ARLib** | Library of poisoning attacks and defenses for recommender systems | [Paper](https://arxiv.org/abs/2406.01022), [Code](https://github.com/CoderWZW/ARLib) |
| **CleverHans** | Adversarial example benchmark library | [Code](https://github.com/cleverhans-lab/cleverhans) |

### Federated Learning Frameworks

| Name | Affiliation | Material |
|------|-------------|----------|
| **FATE** | WeBank AI | [Paper](https://www.jmlr.org/papers/volume22/20-815/20-815.pdf), [Code](https://github.com/FederatedAI/FATE) |
| **Flower** | Adap / Univ. of Cambridge / Nokia Bell Labs | [Paper](https://arxiv.org/pdf/2007.14390.pdf), [Code](https://github.com/adap/flower) |
| **FedML** | FEDML Inc. | [Paper](https://arxiv.org/pdf/2007.13518.pdf), [Code](https://github.com/FedML-AI/FedML) |
| **OpenFL** | Intel / Univ. of Pennsylvania | [Paper](http://iopscience.iop.org/article/10.1088/1361-6560/ac97d9), [Code](https://github.com/securefederatedai/openfl) |
| **TensorFlow Federated** | Google | [Link](https://www.tensorflow.org/federated) |

### Recommender System Toolkits

| Name | Affiliation | Material |
|------|-------------|----------|
| **RecBole** | Renmin Univ. of China | [Paper](https://dl.acm.org/doi/abs/10.1145/3511808.3557680), [Code](https://github.com/RUCAIBox/RecBole) |
| **Microsoft Recommenders** | Microsoft | [Paper](https://dl.acm.org/doi/abs/10.1145/3366424.3382692), [Code](https://github.com/recommenders-team/recommenders) |
| **Cornac** | Singapore Management Univ. | [Paper](https://dl.acm.org/doi/abs/10.1145/3460231.3473324), [Code](https://github.com/PreferredAI/cornac) |
| **DaisyRec** | Macquarie Univ. | [Paper](https://dl.acm.org/doi/10.1145/3383313.3412489), [Code](https://github.com/AmazingDD/daisyRec) |
| **ELLIOT** | SisInfLab | [Paper](https://doi.org/10.1145/3404835.3463245), [Code](https://github.com/sisinflab/elliot) |
| **FuxiCTR** | Huawei Noah's Ark Lab | [Paper](https://dl.acm.org/doi/10.1145/3477495.3531723), [Code](https://github.com/reczoo/FuxiCTR) |

---

## 📁 Datasets

Standard benchmarks used across the FedRS attack/defense literature. Federated partitioning is by user (each user = one client) unless stated otherwise.

| Dataset | Domain | Users | Items | Interactions | Link |
|---------|--------|-------|-------|-------------|------|
| MovieLens-100K | Movies | 943 | 1,682 | 100K | [Link](https://grouplens.org/datasets/movielens/100k/) |
| MovieLens-1M | Movies | 6,040 | 3,706 | 1M | [Link](https://grouplens.org/datasets/movielens/1m/) |
| MovieLens-10M/20M | Movies | 72K / 138K | 10K / 27K | 10M / 20M | [Link](https://grouplens.org/datasets/movielens/) |
| Amazon Reviews | E-commerce | varies | varies | 233M | [Link](https://cseweb.ucsd.edu/~jmcauley/datasets/amazon_v2/) |
| Steam | Games | 334K | 15K | 4M | [Link](https://cseweb.ucsd.edu/~jmcauley/datasets.html#steam_data) |
| Gowalla | POI / check-in | 107K | 1.28M | 6.4M | [Link](https://snap.stanford.edu/data/loc-gowalla.html) |
| Yelp | Business reviews | 2M | 160K | 8.6M | [Link](https://www.yelp.com/dataset) |
| MIND | News | 1M | 161K | 24M | [Link](https://msnews.github.io/) |
| Last.FM | Music | 1,892 | 17,632 | 92K | [Link](https://grouplens.org/datasets/hetrec-2011/) |
| Pinterest | Images | 55K | 9,916 | 1.5M | [Link](https://github.com/edervishaj/pinterest-recsys-dataset) |

---

## 🧪 Evaluation Protocol

For results to be comparable across papers, report the following. Most inconsistency in the FedRS attack literature comes from silently varying these.

**Recommendation utility**

- `HR@K`, `NDCG@K`, `Recall@K`, `Precision@K` — K ∈ {5, 10, 20}
- Evaluation strategy: leave-one-out vs. ratio split (state which)
- Negative sampling: full-ranking vs. 99/100-negative sampling (results are **not** comparable across these)

**Attack effectiveness**

- `ER@K` (Exposure Ratio) — fraction of users whose top-K contains a target item
- `HR@K` on target items specifically, not just overall
- Attacker budget: **malicious client ratio** (typically 0.1%–5%) and **items per fake user**
- Attacker knowledge: black-box / grey-box (partial item popularity) / white-box

**Defense evaluation**

- Clean-model utility drop (the cost of the defense when no attack is present)
- Attack effectiveness under defense vs. without
- Adaptive attacker: does the attack still work when the attacker *knows* the defense?
- Communication and computation overhead per round

**Reproducibility checklist**

- [ ] Fixed random seeds, ≥3 runs, mean ± std reported
- [ ] Client sampling rate and local epochs stated
- [ ] Data partition script included
- [ ] Hyperparameters for **both** the base model and the attack/defense
- [ ] Hardware and wall-clock training time

---

## 🗾️ Threat Model Taxonomy

Use this to position any new paper you read.

| Dimension | Options |
|----------|---------|
| **Adversary goal** | Targeted promotion · Targeted demotion · Untargeted degradation · Privacy inference · Backdoor |
| **Adversary capability** | Malicious clients only · Malicious server · Colluding clients · Client + auxiliary data |
| **Knowledge** | Black-box · Grey-box (public item popularity) · White-box (full model + defense) |
| **Attack surface** | Item embeddings · User embeddings · Gradients/updates · Local training data · Aggregation rule |
| **Defense family** | Robust aggregation (Krum, Trimmed-Mean, Median, Bulyan) · Anomaly/outlier detection · Differential privacy · Secure aggregation / HE · Personalization · Norm clipping · Trust & reputation |

---

## 🤝 Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) — the short version: an entry is accepted only if it has **public working code** and a **CORE A\*/A or Q1/Q2 venue**, and the code link must resolve.

---

## 📄 Citation

If this collection helps your research, please cite it:

```bibtex
@misc{khan2026fedrecsec,
  author       = {Khan, Muhammad Zubair},
  title        = {Federated Learning Attacks: A Curated Index of Attacks, Defenses and
                  Reproducible Codebases for Federated Recommender Systems},
  year         = {2026},
  publisher    = {GitHub},
  howpublished = {\url{https://github.com/zubairawan167/Federated-learning-attacks}}
}
```

Please also cite the foundational survey this collection builds upon:

```bibtex
@article{ali2026navigating,
  author  = {Ali, Waqar and others},
  title   = {Navigating Threats in Federated Recommender Systems:
             A Survey of Attack Models and Defense Strategies},
  journal = {Artificial Intelligence Review},
  year    = {2026},
  doi     = {10.1007/s10462-026-11579-6}
}
```

---

## ⭐ Acknowledgements

This repository draws on and cross-checks several existing curated lists — [AttackDic](https://github.com/waqar-uestc/AttackDic), [awesome-recsys-poisoning](https://github.com/tamlhp/awesome-recsys-poisoning), [FederatedRS](https://github.com/XuanangD/FederatedRS), [Survey-FedRec](https://github.com/SmilesLab-XJTU/Survey-FedRec), [RS-Adversarial-Learning](https://github.com/EdisonLeeeee/RS-Adversarial-Learning), [RSPapers](https://github.com/hongleizhang/RSPapers), and [Awesome-FL](https://youngfish42.github.io/Awesome-FL/) — a large share of the attack, defense, and toolkit entries here originate from these sources rather than independent discovery; this repository's contribution is re-verifying every code link, applying a uniform venue-rank filter, and adding newer (2025–2026) papers and the evaluation-protocol/taxonomy sections.

---

### 🔄 This repository is actively maintained. Star it to follow updates, or open a PR to add a paper.
