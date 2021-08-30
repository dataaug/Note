[SimCSE: Simple Contrastive Learning of Sentence Embeddings](https://www.google.com.hk/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwj_9b3HpdjyAhVOE6YKHW6mBeUQFnoECAgQAQ&url=https%3A%2F%2Farxiv.org%2Fabs%2F2104.08821&usg=AOvVaw17P5QeznQE6wfKrI7qT9OF)

![Screen Shot 2021-08-30 at 8.03.08 PM](/Users/heyeting/Documents/Note/papers/images/Screen Shot 2021-08-30 at 8.03.08 PM.png)

该文章提出对比学习的方法，其中包括有监督和无监督方法。左侧的无监督方法正样本通过BERT进行两次推断（仅dropout随机种子不同）获得，副样本则是所有其他句子，通过下式计算损失函数：

![](/Users/heyeting/Documents/Note/papers/images/Screen Shot 2021-08-30 at 8.04.53 PM.png)

有监督方法则采用如下损失函数，正样本是数据集中（entailment）标签负样本是数据集中（contradiction）标签。

![](/Users/heyeting/Documents/Note/papers/images/Screen Shot 2021-08-30 at 8.06.50 PM.png)



各向异性相关证明先略过。

