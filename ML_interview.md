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
  * Model selection:
    * split the dataset into **training set** and **test** and **(cross) validation set** (Random sampling 60% T 20% CV 20%T)
    * Learn parameter from training data
    * compute test set error (MSE for regresssion | cross entory, misclassification error[https://www.coursera.org/learn/machine-learning/supplement/aFpD3/evaluating-a-hypothesis] for classification/logistic regression)
    * Use Validation set to 
    
  * 分类模型评估方法？
  * 回归问题评估方法？
  * 数据不均衡的评估方法？

  
  
Feature 特征:
======

  * 如何进行选择特征选择？
    依据先验经验人工挑选
    如题目描述中的天气预测问题，可以预先确定湿度、温度、是否有云、风向、风速、近几日天气状况等明显较为相关的特征。
    
    线性特征选择。假设特征之间相互独立，不存在交互，那么可以使用卡方检验、信息增益、互信息等方法逐个检验特征与结果之间的相关程度。 更为简便的方法是使用LR等线性模型，先做一次预训练，根据特征对应的线性模型权值的绝对值大小来对特征的重要程度进行排序。
    
    非线性特征选择。如果考虑特征之间的交互，可以使用随机森林来进行特征选择，具体方法不赘述，概括来说就是将想要检验重要性的特征在样本上进行permutation，然后观察OOB错误的上升程度，上升越大，说明这个特征越重要。
    
    自动特征提取。如第一段所述，核技巧、集成学习、深度学习等较为复杂的算法都可以看做是特征提取的过程，虽然简单省力，但是模型的解释性也会下降，尤其像深度学习这种黑盒子
    
  * 如何进行数据压缩？
  
  * 特征选择：包裹式，过滤式，嵌入式
  * 数据压缩：主成分分析，自编码等

Model 模型:
=======
  
  
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
    
   * Model selection:
   
   
Experimentation 实验：
=======

Calibration 校准：
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
  * 

 
Brand Safty Related:
=======
  * avoid ad placements next to brand-inappropriate or dangerous content
  * * https://www.searchenginewatch.com/2019/02/22/google-youtube-brand-safety-next/
  
Decision Tree[https://cuijiahua.com/blog/2017/11/ml_2_decision_tree_1.html]:
======
  * 


  


