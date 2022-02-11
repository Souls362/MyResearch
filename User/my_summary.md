# Pretrained User Representation

sihua.qi@shopee.com



## Datasets

| Dataset               | Address                                                      | Size |
| --------------------- | ------------------------------------------------------------ | ---- |
| Tencent TL dataset    | https://drive.google.com/file/d/1imhHUsivh6oMEtEW-RwVc4OsDqn-xOaP/view |      |
| MovieLens 25M Dataset | https://grouplens.org/datasets/movielens/25m/                | 25m  |
| Amazon                | https://nijianmo.github.io/amazon/index.html                 |      |
| Yelp                  | https://www.yelp.com/dataset                                 |      |



## Training Objects

- AutoRegressive:

  <img src="/Users/sihua.qi/Desktop/github/MyResearch-Shopee/imgs/my_summary_autoregressive.png" alt="my_summary_autoregressive" style="zoom:33%;" />

  given a list of interactions(items), predict the last interaction(item) $x$ with previous $x-1$ inteactions

  - [PeterRec](./peter_rec.md)

    

- AutoEncoding:

  <img src="/Users/sihua.qi/Desktop/github/MyResearch-Shopee/imgs/auto_encoding.png" alt="auto_encoding" style="zoom:33%;" />

  

  give a list of interactions(items) with length $n$, randomly mask interaction(item) $1 \le x < n$, predict the masked interaction.

  hidden output may differ with models:

  - Use CLS
  - Use hidden output of masked item
  - Adding Negative Samples 
  - Adding additional info, order time / category / price bucket and etc with more masked prediction objectives

  > [ShopperBert](), [PeterRec]()

- Contrastive:

  <img src="/Users/sihua.qi/Desktop/github/MyResearch-Shopee/imgs/contrastive.png" alt="contrastive" style="zoom:33%;" />

  given a list of interactions(items), random sample two sub lists from origin list. give preidction for the outputs of two sub lists.

  - Use CLS
  - Use hidden output of last item
  - Adding Negative Samples 

  <img src="/Users/sihua.qi/Desktop/github/MyResearch-Shopee/imgs/contrastive1.png" style="zoom:33%;" />

  given a list of interactions(items), premuatation the list getting a new interaction list, give preidction for the outputs of two  lists.

  - Use CLS
  - Use hidden output of last item
  - Adding Negative Samples 

  

## Backbones





## Performance

