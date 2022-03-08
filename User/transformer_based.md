# Transformer Based 

## Papers

| No.  | year | paper                                                        | pdf                                                         | note                            |
| ---- | ---- | ------------------------------------------------------------ | ----------------------------------------------------------- | ------------------------------- |
| 1    | 2022 | Learning Universal User Representations via Self-Supervised Lifelong Behaviors Modeling | [PDF](https://openreview.net/pdf?id=YTtMaJUN_uc)            | [Notes](./User/lifelonge_ur.md) |
| 2    | 2021 | Scaling Law for Recommendation Models: Towards General-purpose User Representations | [PDF](https://arxiv.org/pdf/2111.11294.pdf)                 | [Notes](./User/gpur.md)         |
| 3    | 2021 | One4all User Representation for Recommender Systems in E-commerce | [PDF](https://arxiv.org/pdf/2106.00573.pdf)                 | [Notes](./User/shopperbert.md)  |
| 4    | 2021 | UserBERT: Contrastive User Model Pre-training                | [PDF](https://arxiv.org/pdf/2109.01274.pdf)                 | [Notes](./User/userbert.md)     |
| 5    | 2021 | UPRec: User-Aware Pre-training for Recommender Systems       | [PDF](https://arxiv.org/pdf/2102.10989.pdf)                 | [Notes](./User/uprec.md)        |
| 6    | 2020 | PTUM: Pre-training User Model from Unlabeled User Behaviors via Self-supervision | [PDF](https://aclanthology.org/2020.findings-emnlp.174.pdf) | [Notes](./User/ptum.md)         |
| 7    | 2018 | Perceive Your Users in Depth: Learning Universal User Representations from Multiple E-commerce Tasks | [PDF](https://arxiv.org/pdf/1805.10727.pdf)                 | [Notes]()                       |

## Methods

#### Transformer Family

> 1. Learning Universal User Representations via Self-Supervised Lifelong Behaviors Modeling
> 1. Scaling Law for Recommendation Models: Towards General-purpose User Representations
> 1. One4all User Representation for Recommender Systems in E-commerce
> 2. UserBERT: Contrastive User Model Pre-training
> 3. UPRec: User-Aware Pre-training for Recommender Systems
> 4. PTUM: Pre-training User Model from Unlabeled User Behaviors via Self-supervision
> 5. Perceive Your Users in Depth: Learning Universal User Representations from Multiple E-commerce Tasks

Since Transfomer is so successful in NLP tasks, lots of the researchers considering user behavior sequence (click/order/search/follow...) as another format of word sequence which makes it quite popular for applying NLP methods on user representation tasks. 

- Paper1: 

- Paper2: Contrastive Learning User Encoder between different **Services**(No clear definition)? (BST like structure)

- Paper3: **Data augmentation** with crop/shuffle sequence, doing **MLM** **pretraining** with multi tasks: category / date prediction

- Paper4: **Contrastive learning** with behvior sequence matching / masked behvior prediction, tricky on getting negative samples

- Paper5: Pretraining with **Masked Item Prediction** / **User Attribute Prediction** / **Social Relation Detection** 

- Paper6: Pretraining with MLM

- Paper7: Pretraining using LSTM with MLM

  

## Training Objectives

- **AutoRegressive**(masked multi-head attention):

  given a list of interactions(items), predict the last interaction(item) $x$ with previous $x-1$ inteactions

- **AutoEncoder**:

  give a list of interactions(items) with length $n$, randomly mask interaction(item) $1 \le x < n$, predict the masked interaction.

  hidden output may differ with models:

  - Use CLS
  - Use hidden output of masked item
  - Adding Negative Samples 
  - Adding additional info, order time / category / price bucket and etc with more masked prediction objectives

- **Contrastive**:

  - given a list of interactions(items), random sample two sub lists from origin list. give preidction for the outputs of two sub lists.
  - given a list of interactions(items), premuatation the list getting a new interaction list, give preidction for the outputs of two  lists.


  

