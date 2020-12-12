Problem Definition:
======

Data 数据处理:
======
 * 如何处理缺失数据(missing value)? 各种处理方法有什么利弊？
 * 如何将描述变量(categorical variables)转为连续变量(continuous variables)?
   * 如何处理有序变量？
   * 如何处理无序变量？
   
Evaluation 评估:
=======
  * From Andrew:
    * split the dataset into **training set** and **test/validation set** (Random sampling 70% 30%)
    * Learn parameter from training data
    * compute test set error (MSE for regresssion | cross entory, misclassification error for classification/logistic regression)
    
  * 分类模型评估方法？
  * 回归问题评估方法？
  * 数据不均衡的评估方法？
  
Model 模型解释：
=======

  * 试解释什么是欠拟合与过拟合？如何应对这两种情况？
  * 什么是偏差与方差分解(Bias Variance Decomposition)？与欠拟合和过拟合有什么联系？
  * Once we have done some trouble shooting for errors in our predictions by: 
    Getting more training examples
    Trying smaller sets of features
    Trying additional features
    Trying polynomial features
    Increasing or decreasing λ
  
  
Feature 特征:
======

  * 如何进行选择特征选择？如何进行数据压缩？
  
  * 特征选择：包裹式，过滤式，嵌入式
  * 数据压缩：主成分分析，自编码等

Model 模型:
=======

Experimentation 实验：
=======



设计问题：
========
  * Deep Neural Networks for YouTube Recommendations[https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45530.pdf]
  * 

其他问题：
========
 * 深度学习是否比其他学习模型都好？为什么？

NLP 相关:
=======
  * Word2Vec和Embeddings？

 
Brand Safty Related:
=======
  * avoid ad placements next to brand-inappropriate or dangerous content
  * * https://www.searchenginewatch.com/2019/02/22/google-youtube-brand-safety-next/
  


