# Pretrained User Representation

sihua.qi@shopee.com



## Roadmaps

```mermaid
flowchart TD;
subgraph backbone;
    user_representation(User Representation)--> tansformer_related([<a href='./transformer_based.md'><b>Transformer</b></a>]);
    user_representation--> graph_related([<a href='./graph_based.md'><b>Graph Based</b></a>]);
    user_representation--> cnn_related([<a href='./others.md'><b>Others</b></a>]);
    end;
subgraph strategy;
    contrastive(Contrastive Learning);
    data_aug(Data Augmentation);
    transfer_learning(Transfer Learning);
    end;
backbone<--> strategy


```


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





