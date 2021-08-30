对无标签NER任务的经验分析-ICLR2021

https://openreview.net/pdf?id=5jRVa89sZk

命名实体识别中存在大量未被标注的正样本，这些标注会严重扰乱模型的学习。因此对标签为负的样本进行采样缓解这个问题。

值得注意的是，此文章对实体的判断是通过遍历所有可能，也就是说对于从位置 i 到位置 j，其实体向量表示采用如下形式：

![Screen Shot 2021-08-27 at 2.30.39 PM](/Users/heyeting/Documents/Note/papers/images/Screen Shot 2021-08-27 at 2.30.39 PM.png)

而模型具体的推断方式则采用如下形式

![Screen Shot 2021-08-27 at 2.32.09 PM](/Users/heyeting/Documents/Note/papers/images/Screen Shot 2021-08-27 at 2.32.09 PM.png)



对于预测冲突的，选择置信度大的结果。运算复杂度是 O(n^2)，但是由于并行时间上比序列标注更快。

