# Master-fyp


In this project I will utilize machine learning/deep learning to analyse the relationship between news contents and stock price. 


Research Steps: 
1. Crawling Financial & Business & Market news from fin websites，e.g SinaFinance, jrj, etc. 
2. Do word-embedding with pre-trainned massive Chinese word vector provided by Li (2018). 
3. Adopting LSTM, with Self-Attensive Mechenism introduced by Google, aggregate those word-vectors into sentence vectors, and then document vectors. Then an activation function is used to train the model aligned with market change (either 0 for decline, 1 for rise) (Yang, etc., 2016). </br>
4. *Adding technical indicators, in order to increase the accuracy. (if time is permitted)*



## 1. Data Source
### 1.1 News Data
News data from news media, hot platforms are prefered, since articles with low pv would apprently have less influence on market price. 
Potential platforms to be chosed: 
- SinaFinance
- EastMoney
- Jrj
- xueqiu.com
All the news data should at least have a title, with their contents, and a release date to align with the stock return. 

### 1.2 Market Data
Daily data of stocks, including openning price and closing price, can be easily fetched from various of platforms, e.g. Wind. 

### 1.3 Calculated Technical Indicators & Macro-environment Factors 
###### (might not have sufficient time to do this but important for research purpose)
Since news should not be the only 

## 2. Mothods
### 2.1 Word Tokenization
The word tokenization is going to be implemented using 'Jieba' (see: https://pypi.org/project/jieba/), a python library  HMM. 

### 2.2 Word/Token Embedding

#### - LSTM on sentance level+mean-pooling on articles / LSTM on article level (to be chosed)
#### 
### 2.2 Trainning Models
To label the data by different ways we could have totally different ways: 

~~a. label the data for a particular sentiment orientation (e.g. 1 for positive, 0 for negative) </br>
Train for each article and then do mean-pooling for each day, then analyse its influence on stock~~
>~~pros: logically reasonable - positive/negative sentiment can affect stock price~~</br>
>~~cons: Need to label a lot of articles mannually, takes lots of time~~</br>
#### b. label the data by market reaction (e.g. 1 for intra-day raise, 0 for intra-day fall) </br>
Need to train the model on all intra-day articles, this might be a problem, on math, try to figure out. </br>
>pros: Do not need to do labeling (since the label already exists), so we have huge training data to use (fantastic!). And the neural network actually learns itself which kind of news is more relevant to stock market change. </br>
>cons: Not really knowing what is the neural network is doing on the logic of the model </br>










</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>

## Potential References 
### Chinese Word-Embedding
Chinese Word Vectors: Shen Li, Zhe Zhao, Renfen Hu, Wensi Li, Tao Liu, Xiaoyong Du, Analogical Reasoning on Chinese Morphological and Semantic Relations, ACL 2018. https://github.com/Embedding/Chinese-Word-Vectors
(Refer as: Shen Li, Zhe Zhao, Renfen Hu, Wensi Li, Tao Liu, Xiaoyong Du, [Analogical Reasoning on Chinese Morphological and Semantic Relations](https://arxiv.org/pdf/1805.06504.pdf), ACL 2018. )

### NN Architecture & Attention Mechanism
Yang, Z., Yang, D., Dyer, C., He, X., Smola, A. and Hovy, E., 2016. [Hierarchical attention networks for document classification](https://www.cs.cmu.edu/~hovy/papers/16HLT-hierarchical-attention-networks.pdf). In Proceedings of the 2016 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (pp. 1480-148

Lin, Z., Feng, M., Santos, C.N.D., Yu, M., Xiang, B., Zhou, B. and Bengio, Y., 2017. [A structured self-attentive sentence embedding](https://arxiv.org/pdf/1703.03130.pdf). arXiv preprint arXiv:1703.03130.

Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A.N., Kaiser, Ł. and Polosukhin, I., 2017. [Attention is all you need. In Advances in Neural Information Processing Systems](http://papers.nips.cc/paper/7181-attention-is-all-you-need.pdf) (pp. 5998-6008).

### Skip-Gram Model
[1] [Mikolov T, Chen K, Corrado G, et al. Efficient Estimation of Word Representations in Vector Space[J]. Computer Science, 2013.](https://arxiv.org/pdf/1301.3781.pdf)（这篇文章就讲了两个模型：CBOW 和 Skip-gram） 

[2] [Mikolov T, Sutskever I, Chen K, et al. Distributed Representations of Words and Phrases and their Compositionality[J]. 2013, 26:3111-3119.](https://arxiv.org/pdf/1310.4546.pdf)（这篇文章针对Skip-gram模型计算复杂度高的问题提出了一些该进） 

[3] [Presentation on Word2Vec](https://docs.google.com/file/d/0B7XkCwpI5KDYRWRnd1RzWXQ2TWc/edit)（这是NIPS 2013workshop上Mikolov的PPT报告）
### B 


## Materials
[NLP 笔记 - Dependency Parsing and Treebank](http://www.shuang0420.com/2017/03/09/NLP%20%E7%AC%94%E8%AE%B0%20-%20Dependency%20Parsing%20and%20Treebank/) </br>
[Markdown 语法大全 包括设置字体 颜色](https://blog.csdn.net/qcx321/article/details/53780672#commentBox) </br>
[The Ultimate Guide to Markdown](https://blog.ghost.org/markdown/) </br>
[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) </br>
[Concluding Pooling Methods](https://blog.csdn.net/danieljianfeng/article/details/42433475) </br>
