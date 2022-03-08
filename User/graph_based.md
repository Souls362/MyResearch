# Graph Based

## Papers

| No.  | year | paper                                                        | pdf                                                         | note                            |
| ---- | ---- | ------------------------------------------------------------ | ----------------------------------------------------------- | ------------------------------- |
| 1 | 2021 | Explicit Semantic Cross Feature Learning via Pre-trained Graph Neural Networks for CTR Prediction | [PDF](https://arxiv.org/pdf/2105.07752.pdf) | [Notes]() |
| 2 | 2021 | Dual Graph enhanced Embedding Neural Network for CTR Prediction | [PDF](https://arxiv.org/pdf/2106.00314.pdf) | [Notes]() |
| 3  | 2019 | Fi-GNN: Modeling Feature Interactions via Graph Neural Networks for CTR Prediction | [PDF](https://openreview.net/pdf?id=YTtMaJUN_uc)            | [Notes]() |
| 4  | 2019 | AutoInt: Automatic Feature Interaction Learning via Self-Attentive Neural Networks | [PDF](https://arxiv.org/pdf/1810.11921.pdf) | [Notes]()         |

## Methods

#### Graph in Feature

> Fi-GNN: Modeling Feature Interactions via Graph Neural Networks for CTR Prediction
>
> AutoInt: Automatic Feature Interaction Learning via Self-Attentive Neural Networks

Graph related algorithms using in recommendation system.

- Paper1: 
- Paper3: **Sample Level Feature Graph** connecting all Features(Nodes) with learnable weights on Edges. Using **Gated Graph Neural Network** catching cross features. 
- Paper4: similar with Paper3, using GAT(Transformers) for catching cross features.



#### Graph in Pretrain

> Explicit Semantic Cross Feature Learning via Pre-trained Graph Neural Networks for CTR Prediction

- Paper1: **Global Feature Graph**, contrusted based on the interactions(co-occurance) among features in history. Using GNN to get attribute of edge, pretrain with *weighted square loss* btw precalculated edge attribute.
- 

