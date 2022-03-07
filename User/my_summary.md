# Pretrained User Representation

sihua.qi@shopee.com



## Datasets

| Dataset               | Address                                                      | Size |
| --------------------- | ------------------------------------------------------------ | ---- |
| Tencent TL dataset    | https://drive.google.com/file/d/1imhHUsivh6oMEtEW-RwVc4OsDqn-xOaP/view |      |
| MovieLens 25M Dataset | https://grouplens.org/datasets/movielens/25m/                | 25m  |
| Amazon                | https://nijianmo.github.io/amazon/index.html                 |      |
| Yelp                  | https://www.yelp.com/dataset                                 |      |
| MIND                  | https://msnews.github.io/                                    |      |
| AliPay                | https://tianchi.aliyun.com/dataset/dataDetail?dataId=53      |      |
| Tmall                 | https://tianchi.aliyun.com/dataset/dataDetail?dataId=42      |      |
| Alimama               | https://tianchi.aliyun.com/dataset/dataDetail?dataId=56      |      |



## User-Representation X-mind

```mermaid
graph LR;
user_representation(User Representation)--> tansformer_related(tansformer related methods);
user_representation-->graph_related(graph related methods);
tansformer_related--> paper1([<a href='https://arxiv.org/pdf/1805.10727.pdf'><b>DUPN</b></a>]);
tansformer_related--> paper2(2)
tansformer_related--> paper3(3)
tansformer_related--> paper4(4)
tansformer_related--> paper5(4)
tansformer_related--> paper6(4)
graph_related--> paper6(GNN-LM)

```



## TimeLine

- 2018 DUPN(DeepUserPreceptionNetwork) (an **emb + lstm** method for user behavior sequence modeling)
- 



## Embedding Method

- Item Feature + Behavior Property: 

  - Item feature: *item_id* / *shop* / *brand* / *category* / *tags*
  - Behavior property: *scenario* / *time* / *type*  

- 

  



## Training Objectives

- **AutoRegressive**(masked multi-head attention):

  <img src="../imgs/my_summary_autoregressive.png" alt="my_summary_autoregressive" height="65" />

    

  given a list of interactions(items), predict the last interaction(item) $x$ with previous $x-1$ inteactions

  > [PeterRec](./peter_rec.md)

  

- **AutoEncoder**:

  <img src="../imgs/auto_encoding.png" alt="auto_encoding" height="600" />

  

  give a list of interactions(items) with length $n$, randomly mask interaction(item) $1 \le x < n$, predict the masked interaction.

  hidden output may differ with models:

  - Use CLS
  - Use hidden output of masked item
  - Adding Negative Samples 
  - Adding additional info, order time / category / price bucket and etc with more masked prediction objectives

  > [ShopperBert](), [PeterRec]()

- **Contrastive**:

  <img src="../imgs/contrastive.png" alt="contrastive" height="270" />

    

  given a list of interactions(items), random sample two sub lists from origin list. give preidction for the outputs of two sub lists.
  
  - Use CLS
  - Use hidden output of last item
  - Adding Negative Samples 

    

  <img src="../imgs/contrastive1.png" height="270" />
  
     

  given a list of interactions(items), premuatation the list getting a new interaction list, give preidction for the outputs of two  lists.
  
  - Use CLS
  - Use hidden output of last item
  - Adding Negative Samples 
  
  

## Backbones

- TCN
- LSTM
- Transformer
- Aggregated



## Finetuning Methods





## Downstream Tasks

- CTR Prediction
- Learning to Rank
- Price Perference Prediction
- Fashion Icon Following Prediction
- Shop Perference Prediction

## Performance

