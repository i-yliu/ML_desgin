Problem Definition:
======

Data 数据处理:
======
 * 如何处理[缺失数据(missing value)](https://www.zhihu.com/question/26639110)? 各种处理方法有什么利弊？
   * 缺失值过多
     删除
     分为两类：有，或 没有
   * 较少
     用0表示
     均值
     上下数据填充
     差值法
     
      
 * 如何将描述变量(categorical variables)转为连续变量(continuous variables)?
   * 如何处理有序变量？
   * 如何处理无序变量？
   
Evaluation 评估:
=======
  * Model selection:
    * split the dataset into **training set** and **test** and **(cross) validation set** (Random sampling 60% T 20% CV 20%T)
    * Learn parameter from training data
    * compute test set error (MSE for regresssion | cross entory, [misclassification error](https://www.coursera.org/learn/machine-learning/supplement/aFpD3/evaluating-a-hypothesis) for classification/logistic regression)
    * Use Validation set to 
    
    * **[Bias/Variance](https://www.coursera.org/learn/machine-learning/lecture/yCAup/diagnosing-bias-vs-variance)**
      high train + high val -> high bias -> underfit
      low train + high val -> high variance -> overfit
      
      **Regularization with Linear regression** 
      Different regularization parameter lambda
      
      **Learning Curve
      
      **Precision/Recall/Confusion matrix**


  * 试解释什么是欠拟合与过拟合？如何应对这两种情况？
  * 什么是偏差与方差分解(Bias Variance Decomposition)？与欠拟合和过拟合有什么联系？
    * generalization error: 泛化误差可分解为偏差、方差与噪声之和
    * Bias
    * Variance
    * Bias、Variance和K-fold的关系。
       
  
  * Once we have done some trouble shooting for errors in our predictions by: 
    
    Getting more training examples -> fix high variance (model overfitting)
    
    Trying smaller sets of features -> fix high variance(model overfitting)
    
    Trying additional features -> fix high bias 
    
    Trying polynomial features -> fix high bias
    
    Increasing λ -> fix high bias
    
    Decreasing λ -> fix high variance
    
   * Model selection:
            
    
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
  
  

   
   
Experimentation 实验：
=======

Calibration 校准：
=======


设计问题：
========
  * Deep Neural Networks for YouTube Recommendations[https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45530.pdf]
  
  * [Recommendation system](https://www.coursera.org/learn/machine-learning/lecture/Rhg6r/problem-formulation)
    
    Content based recommender systems
    
    Collaborative Filtering
      users -> \[0 5 0\]
      
      given x1 x2 .... xn (and movie ratings)
        can estimate theta (user)
       
      given theta (user)
        can estimate movie features
       
      theta -> x -> theta -> x ......
      
      1. Initialize x, theta
      2. minimize J using gradient descent
        theta transpose x(i)
           
        X
        THETA
        
      Low rank matrix factorization 
      
      * Finding related movies
        
        find movies j related to moive i?
        small ||xi - xj|| similar
        
        **Mean Normalization**
        
  * Anomaly detection
      Density estimation
      
      Fraud detection 
        xi = features of user i's activities
        Model p(x) from data
        identify unusual users by checking which have p(s) < episinon
        
      Manufacturing:
      
      Monitoring computers in data center
      
      Guassian Distribution
      
      Density estimation:
        
        p(x) = p(x1    )p(x2    )p(x3    )...........p(xn    )
      
      Evaluation:
      
        fit p(x)
        
        on a cross valiadation/test example x, predict
        
        Precision/Recall
        
        F1 score
        
        Different threshold
        
      Anomaly detection vs. Supervised learning:
      
        Very small number of positive examples (y = 1, anomaly)

        Large number of negative (y = 0, normal)

        Different anomalies: Hard for any alogirhtm to learn from positive examples;

        Future anomalies may look nothing like any of the anomalous examples
      
        Supervised: Enough positive examples for algorithm to get a sense of what positive exampoles like
        Supervised: Large number of positive and negative examples
        
     Features to Use:
      
        Non-gaussian features -> log(x)/or other transform  make it more gaussian
        
        
     Error Analysis for anomaly detection:
        
        what px large for normal examples x
            px small for anomalous examples x
        
        Most commom problem: both large: may need new feature to itendtify
        
     Origional model vs multivariate Gaussian
     
     
        
        
      
      
      
      
        
        
        
        
        
        
        
        
  
    
        
    
    
  * [Spam classifier](https://www.coursera.org/learn/machine-learning/lecture/4h5X4/prioritizing-what-to-work-on)
     * Spam vs non Spam
     * x = features of email; y = spam (1) or not spam (0)
     * choose 100 words indicative of spam/not spam
       
       name day, discount, now, .....
       
       x = \[0 1 1 0 . ... 1 ..\]
       
       In practice, use the most used 100 words in training set as features.
     
     * Building a spam classifier:
     
        How could you spend your time to improve the accuracy of this classifier?
        
        Collect lots of data (for example "honeypot" project but doesn't always work)
        
        Develop sophisticated features (for example: using email header data in spam emails)
        
        Develop algorithms to process your input in different ways (recognizing misspellings in spam).
         
      * Error Analysis
         
         Manual inspect
         
         Numerical evaluation
         
      * Error metrics for Skewed Classes
       
         Cancer classification example (1% error on test set; only 0.5 % of patients have cancer)
         
         **Precision/Recall/Confusion matrix/F-score**
         Trading Off Precision and Recall
         
       * Data For Machine Learning
         
         How much data we need for training
            
            Assueme features are enough for predicting
            
            -> J train small
            -> J val small 
            
         Perceptraon
         
         Winnow x
         
         memory-based
         
         Naive-Base
         
        
        
        
        
        
         
       

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
  * https://www.youtube.com/watch?v=UA29hlsamSE&feature=emb_title
  
[Decision Tree](https://cuijiahua.com/blog/2017/11/ml_2_decision_tree_1.html):
======
  * 


  


