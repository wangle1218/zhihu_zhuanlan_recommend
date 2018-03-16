# 知乎ML/NLP/DL领域专栏文章整理

### 2018-03-16 更新

经常浏览知乎，发现有很多专栏文章写的非常不错，看完受益匪浅；于是想更全面的、更方便的找到自己想看的文章，同时也想看看在 AI 领域，哪些文章最受知乎用户的欢迎。于是开始了这个项目。

本项目属于简单的自然语言处理相关的项目，里面包括的技术有：**爬虫**、**网页解析**、**数据分析**、**TF-IDF** 和 **LDA 关键词提取**、**LDA 主题模型**、**文本自动摘要**、**文本聚类**等等。

当初花了2、3天的闲暇时间做这个事，同时也在我的[知乎专栏](https://zhuanlan.zhihu.com/leemoo)发了三篇文章来记录我的想法和完成过程，文章如下：

1. [分析了558个知乎专栏，竟然让我发现这样的事](https://zhuanlan.zhihu.com/p/32822550)
2. [ML/DL/NLP/AI领域最值得关注的知乎专栏](https://zhuanlan.zhihu.com/p/32856237)
3. [AI领域TOP100知乎最受欢迎专栏文章--提取关键词和摘要展示](https://zhuanlan.zhihu.com/p/32911340)

---
完成以上事情的一些简单代码（都是 .ipynb 文件，打开链接可能需要时间）如下：

1. [使用 Beautiful 将 HTML 文件解析，使用 pandas 将文本数据格式化成 csv 文件](https://github.com/wangle1218/zhihu_zhuanlan_recommend/blob/master/zhuanlan_info%E8%A7%A3%E6%9E%90.ipynb)
2. [利用专栏关注人数、文章点赞数、评论数、文章数量计算每个专栏的推荐指数，计算专栏发文周期，另外对一些专栏做了主题展示](https://github.com/wangle1218/zhihu_zhuanlan_recommend/blob/master/zhuanlan_recommend_index_publish_period.ipynb)
3. [利用各项指标计算了每一篇文章的受欢迎指数，提取前100篇文章的关键词和摘要](https://github.com/wangle1218/zhihu_zhuanlan_recommend/blob/master/Best-article.ipynb)

---
最终结果（markdown 文件）如下：

1. [558个ML/NLP/DL知乎专栏按关注人数排序列表](https://github.com/wangle1218/zhihu_zhuanlan_recommend/blob/master/sort_by_followers.md)，包含专栏名称、专栏作者、专栏介绍、专栏文章数、专栏关注人数（所有数据都是两个月前的）。
2. [AI领域558个知乎专栏的发文章时间周期统计](https://github.com/wangle1218/zhihu_zhuanlan_recommend/blob/master/publish_Period.md)，计算了每个专栏的发文周期频率，看看哪个专栏博主最积极。
3. [AI领域558个知乎专栏推荐指数](https://github.com/wangle1218/zhihu_zhuanlan_recommend/blob/master/recommend_Index.md)，综合了以下数据：专栏名称、专栏推荐指数、专栏链接、专栏发文平均周期（天）、专栏文章数量、专栏关注人数、所有文章中最少评论数、所有文章中的平均评论数、所有文章中的最大评论数、所有文章中最少点赞数、所有文章中平均点赞数、所有文章中最多点赞数。
4. [AI领域100篇最受欢迎知乎专栏文章](https://github.com/wangle1218/zhihu_zhuanlan_recommend/blob/master/top100_articles.md)，里面有文章链接、推荐指数、文章点赞数、评论数、发文日期、文章关键词、摘要。

---
### 以下是最开始的 readme 文件内容，里面列的一些事情还没做，实在是好忙。。。

本项目志在对知乎ML/NLP/DL领域的相关专栏文章做一些整理，并且为读者推荐值得看的文章。后续工作安排如下：

* 提取所有专栏的所有文章的发文时间分析发文周期(总共6559篇文章)；

* 提取所有文章的赞同数、评论数；

* 针对ML、NLP、DL等细分领域做文章主题分类；

* 提取每篇文章的精简摘要、关键词；

* 相似文章整合；

* 综合以上所有数据做一个推荐榜，推荐每个细分领域最值得读的文章。

558个专栏的总体情况，详细介绍可以参看这篇[知乎文章](https://zhuanlan.zhihu.com/p/32822550)

[所有专栏按关注人数排序列表](https://github.com/wangle1218/zhihu_zhuanlan_recommend/blob/master/sort_by_followers.md)