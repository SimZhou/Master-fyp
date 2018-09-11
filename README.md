# Master-fyp

In this project I will utilize machine learning/deep learning to analyse the relationship between news contents and stock price.


Research Steps: 
1. 抓取大量新闻平台上的股市相关新闻，例如新浪财经，金融界等。
2. 利用 Li (2018) 等人制作的 pre-trainned 大型中文词向量数据集，进行 Words-embedding。
3. 采用LSTM，结合近期大热的最早由 Google Brains 在图像处理上提出的 Self-Attensive 自注意力机制，将词向量结合成句向量，再将句向量结合为文向量，最后用激活函数激活。最终训练任务为预测股市的涨跌（0,1分类）。(Yang, etc., 2016)
4. 在模型中或许会考虑加入技术面因素，以完善模型精准度。
使用的工具为Python，平台为Tensorflow。



## 1. Data Source
### 1.1 News Data
News data from news media, hot platforms are prefered, since articles with low pv would apprently have less influence on market price. 
potential platforms to be chosed: 
### 1.2 Market Data
Daily data of stocks, including openning price and closing price, can be easily fetched from various of platforms.

### 1.3 Calculated Technical Indicators & Macro-environment Factors 
###### (might not have sufficient time to do this but important for research purpose)


## 2. Mothods
### 2.1 Word Tokenization

### 2.2 Word/Token Embedding

#### - LSTM on sentance level+mean-pooling on articles / LSTM on article level (to be chosed)
#### 
### 2.2 Trainning Models
To label the data by different ways we could have totally different ways: </br>
#### a. label the data for a particular sentiment orientation (e.g. 1 for positive, 0 for negative) </br>
Train for each article and then do mean-pooling for each day, then analyse its influence on stock
>pros: logically reasonable - positive/negative sentiment can affect stock price </br>
>cons: Need to label a lot of articles mannually, takes lots of time </br>
#### b. label the data by market reaction (e.g. 1 for intra-day raise, 0 for intra-day fall) </br>
Need to train the model on all intra-day articles, this might be a problem, on math, try to figure out. </br>
>pros: Do not need to do labeling (since the label already exists), so we have huge training data to use (fantastic!) </br>
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

#### References：

Shen Li, Zhe Zhao, Renfen Hu, Wensi Li, Tao Liu, Xiaoyong Du, Analogical Reasoning on Chinese Morphological and Semantic Relations, ACL 2018. 
Yang, Z., Yang, D., Dyer, C., He, X., Smola, A. and Hovy, E., 2016. Hierarchical attention networks for document classification. In Proceedings of the 2016 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (pp. 1480-148

### materials
[NLP 笔记 - Dependency Parsing and Treebank](http://www.shuang0420.com/2017/03/09/NLP%20%E7%AC%94%E8%AE%B0%20-%20Dependency%20Parsing%20and%20Treebank/) </br>
[Markdown 语法大全 包括设置字体 颜色](https://blog.csdn.net/qcx321/article/details/53780672#commentBox) </br>
[The Ultimate Guide to Markdown](https://blog.ghost.org/markdown/) </br>
[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) </br>
[Concluding Pooling Methods](https://blog.csdn.net/danieljianfeng/article/details/42433475) </br>
