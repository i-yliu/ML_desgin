To do:
  1. Phil 的project
  2. curve 分类的拓展： 检测异常filaments? -> intensity: 每张图片normalize
  3. adaboost ; gbdt
  4. dataset scale, how much you needed, 
  5. 训练时间， 训练技巧
  6. Cold start problem
  7. attention mechanism
  8. transformer
  9. Representation learning/contrastive loss
  10. 各个模型区别
  11. 系统对可解释性的要求
  12. 情感分析
  13. https://towardsdatascience.com/deep-surveillance-6b389abeaf95
  14. 

* Complexities consideration for an ML system (Requirement)

  * Compare between: Multiple Additive Regression Trees (MART)/ Gradient boosting decision tree(GBDT); Neural Network; Linear/Logistic Regression (Batch) 
  * Training complexity
  * Evaluation complexity
  * Sample complexity
  * Funnel approach for an ad prediction system (Logistic regression -> neural network / GBDT)
  
* Data

  Data collection
  
  * Online data collection through a user's interaction with the system in place
  * Human labelers (offline)
  
   * Crowdsourcing
   * Specialized labelers
   * Open-source dataset
   * Build the product in a way that it collects data from users
   * Creative manual expansion (data augmentation)
   * Data expansion using GANs (For image translation)
    
  
  Train, test, & validation splits
  
  Cleaning up data:
    * missing data
    
    * Unblanced data
    
    * outliers
    * duplicates
    * dropping out irrelevant features
    
    * Removing bias
    * Bootstrapping new items
    
  Embeddings
    TEXT:
    * word2vec 
        Self-supervised learning from a large corpus of text data
      * CBOW (continuous bag of words)
        predict the current word from its surrounding words
        Loss = -log (p(wt| wt-n ......wt+n)
      * Skipgram: 
        predict surrounding words from the current word
    
    * Embedding from language models(ELMo)
    * BERT
    * GPT
      
    Visual:
    * Auto-encoders
    * pre-trained model as our image embedding.
    
  
