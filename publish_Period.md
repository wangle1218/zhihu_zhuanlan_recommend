# AI领域558个知乎专栏的发文章时间周期统计
---

作者列表里面的ID为该专栏中发过文章的所有作者。

## 发帖周期计算方法：

使用2018年1月11日和该专栏首次发文的时间之间的相隔天数除以该专栏的文章数量。

```python
period_df['publish_period'] = period_df['first_publishedTime'].map(lambda x : datetime.strptime('2018-1-11','%Y-%m-%d') - \
                                                            datetime.strptime(x, '%Y-%m-%d'))
period_df['publish_period'] = period_df['publish_period'].map(lambda x: x.days)
period_df.loc[:,'published_period'] = period_df['publish_period'] / period_df['articles_count']
```
---

<table>

<tr>
<td>专栏名称</td>
<td>专栏地址</td>
<td>作者列表</td>
<td>文章数量</td>
<td>末次发文日期</td>
<td>首次发文日期</td>
<td>发帖周期（天）</td>
</tr>

<tr>
<td>车神的机器学习</td>
<td>https://zhuanlan.zhihu.com/c_128528277</td>
<td>Pig951001</td>
<td>18</td>
<td>2017-12-25</td>
<td>2018-01-10</td>
<td>0.944444444444</td>
</tr>

<tr>
<td>深度学习源码解析</td>
<td>https://zhuanlan.zhihu.com/c_144268772</td>
<td>小白</td>
<td>39</td>
<td>2017-11-24</td>
<td>2018-01-11</td>
<td>1.23076923077</td>
</tr>

<tr>
<td>BAT面试1000题</td>
<td>https://zhuanlan.zhihu.com/c_140166199</td>
<td>julyedu</td>
<td>40</td>
<td>2017-11-10</td>
<td>2018-01-11</td>
<td>1.55</td>
</tr>

<tr>
<td>网易智能</td>
<td>https://zhuanlan.zhihu.com/smartman163</td>
<td>小羿</td>
<td>196</td>
<td>2017-02-14</td>
<td>2018-01-11</td>
<td>1.6887755102</td>
</tr>

<tr>
<td>一片神鸦社鼓</td>
<td>https://zhuanlan.zhihu.com/yang3</td>
<td>讳莫如深</td>
<td>11</td>
<td>2017-12-18</td>
<td>2018-01-08</td>
<td>2.18181818182</td>
</tr>

<tr>
<td>人工智能成长之路</td>
<td>https://zhuanlan.zhihu.com/c_147015982</td>
<td>weapon</td>
<td>17</td>
<td>2017-12-04</td>
<td>2018-01-09</td>
<td>2.23529411765</td>
</tr>

<tr>
<td>Python中文社区</td>
<td>https://zhuanlan.zhihu.com/zimei</td>
<td>段小草 iGuo xchaoinfo 笑虎 阿橙 夏洛之枫 苍冥 九茶 Jerry Wayne Shi 邵正将 七夜 陈龙 Drei LittleCoder LucasX 陈鸣 猪了个去 超人 tonnie 爬虫 Crossin Eacon 有心人 何红亮 nmask bingtel wang RaPoSpectre cqpaul 邓旭东HIT yonggege DAIXK Wakingup 丁果 牛肉咖喱饭 王勇 chenjiandongx resolvewang zhenhang.sun Snake 松直 九毫 丁丁丁 天清 magickking 江峰 黄康德 挖掘机小王子 Deserts X 豇豆大数据 紫千豪 伟楠 老狼 QuantFisher 刘蘩 yea yee charging 瑶妹妹先生 大吉大利小米酱 两点水 王瑞 seven11 无小意丶 路人乙 熊本一身白 布道 laobigeek marsxhf 强哥 weapon 栗子君 DealiAxy marvin</td>
<td>243</td>
<td>2016-06-15</td>
<td>2018-01-04</td>
<td>2.36625514403</td>
</tr>

<tr>
<td>TensorFlowNews</td>
<td>https://zhuanlan.zhihu.com/TensorFlownews</td>
<td>灰灰</td>
<td>77</td>
<td>2017-07-11</td>
<td>2018-01-07</td>
<td>2.38961038961</td>
</tr>

<tr>
<td>nlp相关论文笔记</td>
<td>https://zhuanlan.zhihu.com/c_134593059</td>
<td>TtC的WH</td>
<td>8</td>
<td>2017-12-21</td>
<td>2018-01-10</td>
<td>2.625</td>
</tr>

<tr>
<td>PaperWeekly</td>
<td>https://zhuanlan.zhihu.com/paperweekly</td>
<td>张俊</td>
<td>216</td>
<td>2016-05-26</td>
<td>2018-01-05</td>
<td>2.75462962963</td>
</tr>

<tr>
<td>深度学习与NLP</td>
<td>https://zhuanlan.zhihu.com/lqfarmer</td>
<td>lqfarmer</td>
<td>94</td>
<td>2017-04-26</td>
<td>2017-12-25</td>
<td>2.76595744681</td>
</tr>

<tr>
<td>Java/大数据/机器学习面经</td>
<td>https://zhuanlan.zhihu.com/liuwen</td>
<td>刘文</td>
<td>20</td>
<td>2017-11-15</td>
<td>2017-11-29</td>
<td>2.85</td>
</tr>


<tr>
<td>掘金翻译计划</td>
<td>https://zhuanlan.zhihu.com/juejinfanyi</td>
<td>根号三 Lam Pui lsvih mnikn 影子小超人 临书 richardleehui Cherry lekenny LeviDing 宋海峰 张志远 杨楚天 宝宝周 Mike 2tree MummyDing 威仔</td>
<td>59</td>
<td>2017-07-20</td>
<td>2017-12-28</td>
<td>2.96610169492</td>
</tr>

<tr>
<td>炼丹炉</td>
<td>https://zhuanlan.zhihu.com/c_143903708</td>
<td>黄展鹏</td>
<td>13</td>
<td>2017-11-30</td>
<td>2018-01-10</td>
<td>3.23076923077</td>
</tr>

<tr>
<td>机器学习面试题总结</td>
<td>https://zhuanlan.zhihu.com/c_129612503</td>
<td>李理</td>
<td>27</td>
<td>2017-10-13</td>
<td>2017-12-19</td>
<td>3.33333333333</td>
</tr>

<tr>
<td>机器学习算法与自然语言处理</td>
<td>https://zhuanlan.zhihu.com/qinlibo-ml</td>
<td>忆臻 Snake Evan 花花 Aaron Yang 陈诚</td>
<td>107</td>
<td>2017-01-10</td>
<td>2018-01-11</td>
<td>3.42056074766</td>
</tr>

<tr>
<td>清醒疯子</td>
<td>https://zhuanlan.zhihu.com/iqingxingfengzi</td>
<td>利炳根</td>
<td>428</td>
<td>2013-10-14</td>
<td>2017-11-30</td>
<td>3.6214953271</td>
</tr>

<tr>
<td>程序猿数据爱好者</td>
<td>https://zhuanlan.zhihu.com/c_94187513</td>
<td>天涯浪子</td>
<td>71</td>
<td>2017-04-25</td>
<td>2018-01-08</td>
<td>3.67605633803</td>
</tr>

<tr>
<td>Python学习之路</td>
<td>https://zhuanlan.zhihu.com/python-kivy</td>
<td>CycleUser HanTheExplorer 杜兵 飞龙</td>
<td>102</td>
<td>2016-12-30</td>
<td>2018-01-01</td>
<td>3.69607843137</td>
</tr>

<tr>
<td>地球派</td>
<td>https://zhuanlan.zhihu.com/c_93988311</td>
<td>衫秋南</td>
<td>67</td>
<td>2017-05-04</td>
<td>2017-12-17</td>
<td>3.76119402985</td>
</tr>

<tr>
<td>西土城的搬砖日常</td>
<td>https://zhuanlan.zhihu.com/xitucheng10</td>
<td>三水 小打小闹 邮递员小王 simple Seven summer 王梓良 bear8133 bongbong Jason qqwang 老潇 饮水机小包 BugDen 顾秀森 兰汐汐汐汐 周晓欢 WhiteAndWhite</td>
<td>126</td>
<td>2016-09-21</td>
<td>2018-01-10</td>
<td>3.78571428571</td>
</tr>

<tr>
<td>云时之间</td>
<td>https://zhuanlan.zhihu.com/xiahongjin</td>
<td>云时之间</td>
<td>95</td>
<td>2017-01-14</td>
<td>2018-01-09</td>
<td>3.81052631579</td>
</tr>

<tr>
<td>深度学习+自然语言处理（NLP）</td>
<td>https://zhuanlan.zhihu.com/c_123183356</td>
<td>刘博</td>
<td>35</td>
<td>2017-08-29</td>
<td>2018-01-08</td>
<td>3.85714285714</td>
</tr>

<tr>
<td>大话机器学习</td>
<td>https://zhuanlan.zhihu.com/dashun</td>
<td>程序</td>
<td>13</td>
<td>2017-11-17</td>
<td>2018-01-09</td>
<td>4.23076923077</td>
</tr>

<tr>
<td>风险控制+机器学习</td>
<td>https://zhuanlan.zhihu.com/c_118716099</td>
<td>狗的生活</td>
<td>34</td>
<td>2017-08-20</td>
<td>2018-01-09</td>
<td>4.23529411765</td>
</tr>

<tr>
<td>天善智能</td>
<td>https://zhuanlan.zhihu.com/tianshan</td>
<td>天善智能</td>
<td>60</td>
<td>2017-04-25</td>
<td>2018-01-08</td>
<td>4.35</td>
</tr>

<tr>
<td>深度学习从入门到放弃</td>
<td>https://zhuanlan.zhihu.com/ahong007</td>
<td>毕骁鹏 陈泰红</td>
<td>62</td>
<td>2017-04-02</td>
<td>2018-01-10</td>
<td>4.58064516129</td>
</tr>

<tr>
<td>转行AI小专栏</td>
<td>https://zhuanlan.zhihu.com/transfer2AI</td>
<td>霍华德</td>
<td>8</td>
<td>2017-12-05</td>
<td>2018-01-11</td>
<td>4.625</td>
</tr>

<tr>
<td>机器学习及NLP</td>
<td>https://zhuanlan.zhihu.com/c_142467262</td>
<td>李俊毅</td>
<td>3</td>
<td>2017-12-28</td>
<td>2018-01-03</td>
<td>4.66666666667</td>
</tr>

<tr>
<td>AI科技大本营</td>
<td>https://zhuanlan.zhihu.com/c_112128011</td>
<td>AI科技大本营</td>
<td>37</td>
<td>2017-07-19</td>
<td>2018-01-10</td>
<td>4.75675675676</td>
</tr>

<tr>
<td>基于深度学习的对话系统</td>
<td>https://zhuanlan.zhihu.com/c_143965981</td>
<td>呜呜哈</td>
<td>7</td>
<td>2017-12-08</td>
<td>2018-01-10</td>
<td>4.85714285714</td>
</tr>

<tr>
<td>学习ML的皮皮虾</td>
<td>https://zhuanlan.zhihu.com/bupt-pris731</td>
<td>顾秀森 baozuyi zc111 Sherlock Shen Godliness.Bo 廖尔冬 Dylan david Yao Lu 苍穹之影 琪琪怪怪 那啥那小谁 西土路10号包工头 王明阳 潇遥丶 不读不读不读 江晚晚96 stonewang dcsyf 战先生 new y 丸子酱Destiny</td>
<td>53</td>
<td>2017-04-28</td>
<td>2018-01-10</td>
<td>4.8679245283</td>
</tr>

<tr>
<td>吴恩达深度学习课程辅导</td>
<td>https://zhuanlan.zhihu.com/aiclass</td>
<td>昂刺鱼人工智能</td>
<td>10</td>
<td>2017-11-21</td>
<td>2018-01-11</td>
<td>5.1</td>
</tr>

<tr>
<td>机器学习家谱</td>
<td>https://zhuanlan.zhihu.com/c_152669739</td>
<td>Xenophon Tony</td>
<td>2</td>
<td>2017-12-31</td>
<td>2018-01-01</td>
<td>5.5</td>
</tr>

<tr>
<td>深度学习与摄影</td>
<td>https://zhuanlan.zhihu.com/c_146817036</td>
<td>龙鹏</td>
<td>7</td>
<td>2017-12-03</td>
<td>2017-12-11</td>
<td>5.57142857143</td>
</tr>

<tr>
<td>每天都要机器学习哦</td>
<td>https://zhuanlan.zhihu.com/leemoo</td>
<td>王乐</td>
<td>17</td>
<td>2017-10-08</td>
<td>2018-01-10</td>
<td>5.58823529412</td>
</tr>

<tr>
<td>机器学习实战</td>
<td>https://zhuanlan.zhihu.com/apachecn-mlia</td>
<td>片刻 ApacheCN</td>
<td>16</td>
<td>2017-10-12</td>
<td>2017-10-19</td>
<td>5.6875</td>
</tr>

<tr>
<td>机器学习算法全栈工程师</td>
<td>https://zhuanlan.zhihu.com/JeemyJohn</td>
<td>章华燕 小白将</td>
<td>16</td>
<td>2017-10-11</td>
<td>2018-01-02</td>
<td>5.75</td>
</tr>

<tr>
<td>机器学习算法与NLP学习笔记</td>
<td>https://zhuanlan.zhihu.com/txshi-algo</td>
<td>TimsonShi</td>
<td>55</td>
<td>2017-02-27</td>
<td>2018-01-03</td>
<td>5.78181818182</td>
</tr>

<tr>
<td>Coursera | 深度学习</td>
<td>https://zhuanlan.zhihu.com/c_147249273</td>
<td>ZJIMPROVE</td>
<td>6</td>
<td>2017-12-07</td>
<td>2017-12-19</td>
<td>5.83333333333</td>
</tr>

<tr>
<td>机器学习神教</td>
<td>https://zhuanlan.zhihu.com/twomeeting</td>
<td>张馨宇</td>
<td>1</td>
<td>2018-01-05</td>
<td>2018-01-05</td>
<td>6.0</td>
</tr>

<tr>
<td>Eyes of Machine</td>
<td>https://zhuanlan.zhihu.com/eyesofmachine</td>
<td>软绵绵的考拉君</td>
<td>4</td>
<td>2017-12-18</td>
<td>2017-12-28</td>
<td>6.0</td>
</tr>

<tr>
<td>知识图谱-给AI装个大脑</td>
<td>https://zhuanlan.zhihu.com/knowledgegraph</td>
<td>SimmerChan</td>
<td>6</td>
<td>2017-12-05</td>
<td>2018-01-07</td>
<td>6.16666666667</td>
</tr>

<tr>
<td>手把手教你实现机器学习算法</td>
<td>https://zhuanlan.zhihu.com/c_133020898</td>
<td>风雪夜归子</td>
<td>14</td>
<td>2017-10-16</td>
<td>2017-12-10</td>
<td>6.21428571429</td>
</tr>

<tr>
<td>MathView of ML</td>
<td>https://zhuanlan.zhihu.com/c_120224762</td>
<td>gegey</td>
<td>23</td>
<td>2017-08-21</td>
<td>2017-12-21</td>
<td>6.21739130435</td>
</tr>

<tr>
<td>在《人工智能》的道路上，越走越远</td>
<td>https://zhuanlan.zhihu.com/c_114562858</td>
<td>咻唯</td>
<td>26</td>
<td>2017-07-30</td>
<td>2017-12-21</td>
<td>6.34615384615</td>
</tr>

<tr>
<td>Python数据采集处理分析挖掘可视化应用实例</td>
<td>https://zhuanlan.zhihu.com/boken</td>
<td>yea yee</td>
<td>60</td>
<td>2016-12-21</td>
<td>2017-12-15</td>
<td>6.43333333333</td>
</tr>

<tr>
<td>智能单元</td>
<td>https://zhuanlan.zhihu.com/intelligentunit</td>
<td>杜客 Flood Sung 魏秀参 猴子 ycszen 甄景贤 YJango Lonely.wm Kun Ni G胖来了 山隹木又 江亦凡 Kay Ke 王留行 陈乐天 一缕阳光</td>
<td>94</td>
<td>2016-05-09</td>
<td>2017-12-31</td>
<td>6.51063829787</td>
</tr>

<tr>
<td>【IT猎头fancyfrees】IT职位招聘/技术交流</td>
<td>https://zhuanlan.zhihu.com/fancyfrees</td>
<td>IT猎头fancyfrees</td>
<td>28</td>
<td>2017-07-12</td>
<td>2018-01-09</td>
<td>6.53571428571</td>
</tr>

<tr>
<td>计算机视觉与深度学习</td>
<td>https://zhuanlan.zhihu.com/sunpeng1996</td>
<td>如今我已剑指天涯</td>
<td>11</td>
<td>2017-10-31</td>
<td>2017-12-28</td>
<td>6.54545454545</td>
</tr>

<tr>
<td>硅谷老实人</td>
<td>https://zhuanlan.zhihu.com/nullptr</td>
<td>立党 到处挖坑蒋玉成 江踏歌 徐国曦 黑化的安琪拉</td>
<td>48</td>
<td>2017-02-28</td>
<td>2017-12-23</td>
<td>6.60416666667</td>
</tr>

<tr>
<td>机器学习炼丹记</td>
<td>https://zhuanlan.zhihu.com/juliuszh</td>
<td>Juliuszh</td>
<td>3</td>
<td>2017-12-22</td>
<td>2017-12-25</td>
<td>6.66666666667</td>
</tr>

<tr>
<td>人工智能学习笔记</td>
<td>https://zhuanlan.zhihu.com/c_80412427</td>
<td>张江</td>
<td>47</td>
<td>2017-03-03</td>
<td>2017-12-22</td>
<td>6.68085106383</td>
</tr>

<tr>
<td>Python 与 机器学习</td>
<td>https://zhuanlan.zhihu.com/carefree0910-pyml</td>
<td>射命丸咲</td>
<td>57</td>
<td>2016-12-20</td>
<td>2017-11-12</td>
<td>6.78947368421</td>
</tr>

<tr>
<td>xTechDay</td>
<td>https://zhuanlan.zhihu.com/xTechDay</td>
<td>[已重置]</td>
<td>44</td>
<td>2017-03-17</td>
<td>2017-04-14</td>
<td>6.81818181818</td>
</tr>

<tr>
<td>强化学习知识大讲堂</td>
<td>https://zhuanlan.zhihu.com/sharerl</td>
<td>天津包子馅儿 杨超 叶强 王小惟 山峰的风 一缕阳光</td>
<td>45</td>
<td>2017-03-01</td>
<td>2018-01-07</td>
<td>7.02222222222</td>
</tr>

<tr>
<td>红色石头的机器学习之路</td>
<td>https://zhuanlan.zhihu.com/Redstone</td>
<td>红色石头</td>
<td>34</td>
<td>2017-05-17</td>
<td>2017-12-14</td>
<td>7.02941176471</td>
</tr>

<tr>
<td>深度学习大讲堂</td>
<td>https://zhuanlan.zhihu.com/dlclass</td>
<td>果果是枚开心果 程程</td>
<td>87</td>
<td>2016-05-09</td>
<td>2018-01-05</td>
<td>7.03448275862</td>
</tr>

<tr>
<td>FingercrossAI</td>
<td>https://zhuanlan.zhihu.com/fingercrossai</td>
<td>徐小贱民</td>
<td>8</td>
<td>2017-11-15</td>
<td>2018-01-05</td>
<td>7.125</td>
</tr>

<tr>
<td>企名片-金融工作系统FinOS，企业数据服务商</td>
<td>https://zhuanlan.zhihu.com/qimingpian</td>
<td>王利</td>
<td>32</td>
<td>2017-05-23</td>
<td>2017-06-20</td>
<td>7.28125</td>
</tr>

<tr>
<td>无痛的机器学习</td>
<td>https://zhuanlan.zhihu.com/hsmyy</td>
<td>冯超 BigQuant</td>
<td>76</td>
<td>2016-07-05</td>
<td>2017-11-22</td>
<td>7.30263157895</td>
</tr>

<tr>
<td>片上神经网络</td>
<td>https://zhuanlan.zhihu.com/DNN-on-Chip</td>
<td>唐杉</td>
<td>35</td>
<td>2017-04-23</td>
<td>2018-01-07</td>
<td>7.51428571429</td>
</tr>

<tr>
<td>深度学习模型</td>
<td>https://zhuanlan.zhihu.com/c_126879345</td>
<td>武维</td>
<td>16</td>
<td>2017-09-12</td>
<td>2018-01-09</td>
<td>7.5625</td>
</tr>

<tr>
<td>各种Learning的随笔</td>
<td>https://zhuanlan.zhihu.com/c_142796140</td>
<td>Frank大魔王</td>
<td>7</td>
<td>2017-11-18</td>
<td>2018-01-05</td>
<td>7.71428571429</td>
</tr>

<tr>
<td>数海拾荒</td>
<td>https://zhuanlan.zhihu.com/datacruiser</td>
<td>Datacruiser</td>
<td>44</td>
<td>2017-02-04</td>
<td>2017-10-26</td>
<td>7.75</td>
</tr>

<tr>
<td>深度学习与我的那些事</td>
<td>https://zhuanlan.zhihu.com/c_115985719</td>
<td>WILL</td>
<td>20</td>
<td>2017-07-31</td>
<td>2018-01-10</td>
<td>8.2</td>
</tr>

<tr>
<td>机器学习之路</td>
<td>https://zhuanlan.zhihu.com/koalatree</td>
<td>大树先生 Lanzhe Guo</td>
<td>13</td>
<td>2017-09-26</td>
<td>2017-12-06</td>
<td>8.23076923077</td>
</tr>

<tr>
<td>Python杂货铺</td>
<td>https://zhuanlan.zhihu.com/hadxu-python</td>
<td>hadxu</td>
<td>18</td>
<td>2017-08-14</td>
<td>2017-12-18</td>
<td>8.33333333333</td>
</tr>

<tr>
<td>新知</td>
<td>https://zhuanlan.zhihu.com/c_113209160</td>
<td>尼猜 kfxw</td>
<td>17</td>
<td>2017-08-17</td>
<td>2018-01-10</td>
<td>8.64705882353</td>
</tr>

<tr>
<td>量化研究每周精选</td>
<td>https://zhuanlan.zhihu.com/c_109014466</td>
<td>BigQuant</td>
<td>22</td>
<td>2017-07-04</td>
<td>2018-01-05</td>
<td>8.68181818182</td>
</tr>

<tr>
<td>慢慢学TensorFlow</td>
<td>https://zhuanlan.zhihu.com/c_76512067</td>
<td>绿萝123</td>
<td>37</td>
<td>2017-02-20</td>
<td>2018-01-08</td>
<td>8.78378378378</td>
</tr>

<tr>
<td>用Sklearn进行机器学习</td>
<td>https://zhuanlan.zhihu.com/c_140910931</td>
<td>彬叔</td>
<td>7</td>
<td>2017-11-10</td>
<td>2017-11-29</td>
<td>8.85714285714</td>
</tr>

<tr>
<td>全球人工智能</td>
<td>https://zhuanlan.zhihu.com/c_81330425</td>
<td>Mike 徐征</td>
<td>35</td>
<td>2017-03-06</td>
<td>2017-03-29</td>
<td>8.88571428571</td>
</tr>

<tr>
<td>G时区@深度学习</td>
<td>https://zhuanlan.zhihu.com/binlearning-dl</td>
<td>G时区</td>
<td>12</td>
<td>2017-09-26</td>
<td>2017-10-25</td>
<td>8.91666666667</td>
</tr>

<tr>
<td>记忆网络-Memory Network</td>
<td>https://zhuanlan.zhihu.com/c_129532277</td>
<td>呜呜哈</td>
<td>12</td>
<td>2017-09-25</td>
<td>2017-11-16</td>
<td>9.0</td>
</tr>

<tr>
<td>每周一篇机器学习论文笔记</td>
<td>https://zhuanlan.zhihu.com/c_137498113</td>
<td>施维而已 liveway66 Xullll 汤圆不椭 山中老年方丈</td>
<td>8</td>
<td>2017-10-31</td>
<td>2018-01-01</td>
<td>9.0</td>
</tr>

<tr>
<td>机器学习随笔</td>
<td>https://zhuanlan.zhihu.com/ML-Algorithm</td>
<td>张老板进工地了</td>
<td>5</td>
<td>2017-11-26</td>
<td>2017-12-24</td>
<td>9.2</td>
</tr>

<tr>
<td>机器学习爱好者</td>
<td>https://zhuanlan.zhihu.com/fengdu78</td>
<td>黄海广 张鑫倩</td>
<td>7</td>
<td>2017-11-07</td>
<td>2017-12-23</td>
<td>9.28571428571</td>
</tr>

<tr>
<td>RUC智能情报站</td>
<td>https://zhuanlan.zhihu.com/RucAIBox</td>
<td>豆豆 白婷 黄Betsy 李军毅 李思晴 张恒DUT 卞书青 株诛 华神 稻稻 慕雨点苍 张文慧</td>
<td>29</td>
<td>2017-04-07</td>
<td>2017-12-17</td>
<td>9.62068965517</td>
</tr>

<tr>
<td>数据说</td>
<td>https://zhuanlan.zhihu.com/aiinsight</td>
<td>阿萨姆</td>
<td>20</td>
<td>2017-06-28</td>
<td>2018-01-04</td>
<td>9.85</td>
</tr>

<tr>
<td>David Silver强化学习公开课中文讲解及实践</td>
<td>https://zhuanlan.zhihu.com/reinforce</td>
<td>叶强</td>
<td>17</td>
<td>2017-07-25</td>
<td>2017-08-22</td>
<td>10.0</td>
</tr>

<tr>
<td>zyy的机器学习与深度学习之路</td>
<td>https://zhuanlan.zhihu.com/zyy-ml-dl</td>
<td>Mr.张</td>
<td>37</td>
<td>2017-01-03</td>
<td>2018-01-01</td>
<td>10.0810810811</td>
</tr>

<tr>
<td>Video Intelligence</td>
<td>https://zhuanlan.zhihu.com/qijiezhao</td>
<td>qjzhao</td>
<td>4</td>
<td>2017-12-01</td>
<td>2018-01-02</td>
<td>10.25</td>
</tr>

<tr>
<td>AI遇见机器学习</td>
<td>https://zhuanlan.zhihu.com/yzhihao</td>
<td>Evan</td>
<td>18</td>
<td>2017-07-09</td>
<td>2018-01-10</td>
<td>10.3333333333</td>
</tr>

<tr>
<td>ML随笔</td>
<td>https://zhuanlan.zhihu.com/c_131499746</td>
<td>战歌指挥官</td>
<td>10</td>
<td>2017-09-27</td>
<td>2018-01-10</td>
<td>10.6</td>
</tr>

<tr>
<td>论文阅读笔记</td>
<td>https://zhuanlan.zhihu.com/paper-reading</td>
<td>KoRe</td>
<td>13</td>
<td>2017-08-26</td>
<td>2018-01-03</td>
<td>10.6153846154</td>
</tr>

<tr>
<td>CS 294 深度强化学习中文笔记</td>
<td>https://zhuanlan.zhihu.com/c_125238795</td>
<td>whoami</td>
<td>12</td>
<td>2017-09-05</td>
<td>2017-12-31</td>
<td>10.6666666667</td>
</tr>

<tr>
<td>第四范式</td>
<td>https://zhuanlan.zhihu.com/4paradigm</td>
<td>第四范式</td>
<td>23</td>
<td>2017-05-10</td>
<td>2017-09-28</td>
<td>10.6956521739</td>
</tr>

<tr>
<td>船长的机器学习海志</td>
<td>https://zhuanlan.zhihu.com/MachineGo</td>
<td>船D长</td>
<td>1</td>
<td>2017-12-31</td>
<td>2017-12-31</td>
<td>11.0</td>
</tr>

<tr>
<td>开始学习机器人</td>
<td>https://zhuanlan.zhihu.com/learn-robotics</td>
<td>Top Liu</td>
<td>42</td>
<td>2016-10-04</td>
<td>2017-12-21</td>
<td>11.0476190476</td>
</tr>

<tr>
<td>Python数据之道</td>
<td>https://zhuanlan.zhihu.com/lemonbit</td>
<td>lemon</td>
<td>22</td>
<td>2017-05-07</td>
<td>2017-11-06</td>
<td>11.3181818182</td>
</tr>

<tr>
<td>莫烦</td>
<td>https://zhuanlan.zhihu.com/morvan</td>
<td>莫烦</td>
<td>32</td>
<td>2017-01-10</td>
<td>2017-11-30</td>
<td>11.4375</td>
</tr>

<tr>
<td>机器学习进阶</td>
<td>https://zhuanlan.zhihu.com/junfenggao</td>
<td>gao jerevon</td>
<td>18</td>
<td>2017-06-16</td>
<td>2017-12-10</td>
<td>11.6111111111</td>
</tr>

<tr>
<td>机器学习和自然语言处理</td>
<td>https://zhuanlan.zhihu.com/wwtnlp</td>
<td>涛笙依旧</td>
<td>15</td>
<td>2017-07-17</td>
<td>2017-08-30</td>
<td>11.8666666667</td>
</tr>

<tr>
<td>Python3机器学习</td>
<td>https://zhuanlan.zhihu.com/ml-jack</td>
<td>Jack-Cui</td>
<td>12</td>
<td>2017-08-21</td>
<td>2017-12-24</td>
<td>11.9166666667</td>
</tr>

<tr>
<td>安全数据与机器学习</td>
<td>https://zhuanlan.zhihu.com/gokakapo</td>
<td>lau phunter</td>
<td>9</td>
<td>2017-09-25</td>
<td>2017-12-13</td>
<td>12.0</td>
</tr>

<tr>
<td>神经网络与强化学习</td>
<td>https://zhuanlan.zhihu.com/c_101836530</td>
<td>剑圣 刘莉莉 王小惟</td>
<td>19</td>
<td>2017-05-26</td>
<td>2017-12-13</td>
<td>12.1052631579</td>
</tr>

<tr>
<td>小石头的码疯窝</td>
<td>https://zhuanlan.zhihu.com/burness-DL</td>
<td>想飞的石头</td>
<td>30</td>
<td>2017-01-03</td>
<td>2018-01-07</td>
<td>12.4333333333</td>
</tr>

<tr>
<td>好玩的编程</td>
<td>https://zhuanlan.zhihu.com/ml123</td>
<td>徐工</td>
<td>25</td>
<td>2017-03-05</td>
<td>2017-07-04</td>
<td>12.48</td>
</tr>

<tr>
<td>一起自然语言理解</td>
<td>https://zhuanlan.zhihu.com/c_140165378</td>
<td>得嘞您内</td>
<td>2</td>
<td>2017-12-17</td>
<td>2017-12-24</td>
<td>12.5</td>
</tr>

<tr>
<td>徐阿衡-自然语言处理</td>
<td>https://zhuanlan.zhihu.com/c_136690664</td>
<td>徐阿衡</td>
<td>5</td>
<td>2017-11-09</td>
<td>2018-01-07</td>
<td>12.6</td>
</tr>

<tr>
<td>强化学习与自然语言处理</td>
<td>https://zhuanlan.zhihu.com/c_147267691</td>
<td>whoami</td>
<td>3</td>
<td>2017-12-04</td>
<td>2017-12-07</td>
<td>12.6666666667</td>
</tr>

<tr>
<td>现金贷中的风险模型浅谈</td>
<td>https://zhuanlan.zhihu.com/c_112188918</td>
<td>张SOMEBODY</td>
<td>14</td>
<td>2017-07-17</td>
<td>2017-12-20</td>
<td>12.7142857143</td>
</tr>

<tr>
<td>草纸</td>
<td>https://zhuanlan.zhihu.com/caopaper</td>
<td>小栗子 TimXP</td>
<td>15</td>
<td>2017-07-02</td>
<td>2017-09-30</td>
<td>12.8666666667</td>
</tr>

<tr>
<td>深度学习234</td>
<td>https://zhuanlan.zhihu.com/deeplearningcc</td>
<td>陈诚</td>
<td>2</td>
<td>2017-12-16</td>
<td>2018-01-02</td>
<td>13.0</td>
</tr>

<tr>
<td>学十林宥嘉&&澡堂陈奕迅的学习笔记</td>
<td>https://zhuanlan.zhihu.com/c_150089709</td>
<td>人来人往</td>
<td>1</td>
<td>2017-12-29</td>
<td>2017-12-29</td>
<td>13.0</td>
</tr>

<tr>
<td>【量化投资与机器学习】公众号团队</td>
<td>https://zhuanlan.zhihu.com/Lhtz-Jqxx</td>
<td>量化投资机器学习 Myron</td>
<td>38</td>
<td>2016-08-20</td>
<td>2018-01-10</td>
<td>13.3947368421</td>
</tr>

<tr>
<td>喵神大人的深度工坊</td>
<td>https://zhuanlan.zhihu.com/codekitty</td>
<td>糖葫芦喵喵</td>
<td>6</td>
<td>2017-10-22</td>
<td>2018-01-05</td>
<td>13.5</td>
</tr>

<tr>
<td>技术杂记</td>
<td>https://zhuanlan.zhihu.com/deeplearning-charlotte</td>
<td>Charlotte</td>
<td>5</td>
<td>2017-11-01</td>
<td>2017-12-01</td>
<td>14.2</td>
</tr>

<tr>
<td>做个深度栗子</td>
<td>https://zhuanlan.zhihu.com/c_129171460</td>
<td>小栗子</td>
<td>2</td>
<td>2017-12-13</td>
<td>2018-01-03</td>
<td>14.5</td>
</tr>

<tr>
<td>晓雷机器学习笔记</td>
<td>https://zhuanlan.zhihu.com/xiaoleimlnote</td>
<td>晓雷</td>
<td>32</td>
<td>2016-09-26</td>
<td>2017-03-04</td>
<td>14.75</td>
</tr>

<tr>
<td>机器学习算法实现系列</td>
<td>https://zhuanlan.zhihu.com/c_134398600</td>
<td>Betten</td>
<td>6</td>
<td>2017-10-14</td>
<td>2018-01-03</td>
<td>14.8333333333</td>
</tr>

<tr>
<td>深度学习从吴恩达开始</td>
<td>https://zhuanlan.zhihu.com/c_146191524</td>
<td>深度碎片 xu liu</td>
<td>8</td>
<td>2017-09-14</td>
<td>2018-01-10</td>
<td>14.875</td>
</tr>

<tr>
<td>机器物语</td>
<td>https://zhuanlan.zhihu.com/c_137276900</td>
<td>李宁</td>
<td>5</td>
<td>2017-10-26</td>
<td>2017-11-02</td>
<td>15.4</td>
</tr>

<tr>
<td>兜哥带你学安全</td>
<td>https://zhuanlan.zhihu.com/douwaf</td>
<td>兜哥</td>
<td>10</td>
<td>2017-08-09</td>
<td>2018-01-08</td>
<td>15.5</td>
</tr>

<tr>
<td>论文笔记</td>
<td>https://zhuanlan.zhihu.com/yangyangfuture</td>
<td>mountain blue</td>
<td>4</td>
<td>2017-11-08</td>
<td>2017-11-28</td>
<td>16.0</td>
</tr>

<tr>
<td>V2AI</td>
<td>https://zhuanlan.zhihu.com/waytoai</td>
<td>poodar.chu</td>
<td>29</td>
<td>2016-09-30</td>
<td>2018-01-10</td>
<td>16.1379310345</td>
</tr>

<tr>
<td>世界那么大我想写代码</td>
<td>https://zhuanlan.zhihu.com/quantumliu</td>
<td>天清 lambda</td>
<td>19</td>
<td>2017-03-09</td>
<td>2017-10-06</td>
<td>16.2105263158</td>
</tr>

<tr>
<td>安立桐乱谈编程</td>
<td>https://zhuanlan.zhihu.com/anlitongstudy</td>
<td>安立桐</td>
<td>17</td>
<td>2017-04-07</td>
<td>2017-12-01</td>
<td>16.4117647059</td>
</tr>

<tr>
<td>遐思录</td>
<td>https://zhuanlan.zhihu.com/baina</td>
<td>杨勇 平衡木 kiukotsu 海雅古慕 喵的熊爪饼 刘聪</td>
<td>35</td>
<td>2016-06-14</td>
<td>2017-12-19</td>
<td>16.4571428571</td>
</tr>

<tr>
<td>人工智障的深度瞎学之路</td>
<td>https://zhuanlan.zhihu.com/chroot</td>
<td>陈云 MagicBubble ZHAHZHI buptscdc</td>
<td>8</td>
<td>2017-08-30</td>
<td>2017-12-28</td>
<td>16.75</td>
</tr>

<tr>
<td>Mathematica机器学习实战</td>
<td>https://zhuanlan.zhihu.com/MathematicaMachineLearning</td>
<td>HyperGroups</td>
<td>8</td>
<td>2017-08-29</td>
<td>2018-01-07</td>
<td>16.875</td>
</tr>

<tr>
<td>Machine Learning Notes</td>
<td>https://zhuanlan.zhihu.com/bcking</td>
<td>柳枫</td>
<td>12</td>
<td>2017-06-21</td>
<td>2017-09-03</td>
<td>17.0</td>
</tr>

<tr>
<td>关于语义分割的分享</td>
<td>https://zhuanlan.zhihu.com/SemanticSegmentation</td>
<td>王佛伟</td>
<td>13</td>
<td>2017-06-01</td>
<td>2017-12-22</td>
<td>17.2307692308</td>
</tr>

<tr>
<td>概率机器人专栏</td>
<td>https://zhuanlan.zhihu.com/c_134934160</td>
<td>Clarify</td>
<td>5</td>
<td>2017-10-16</td>
<td>2017-11-07</td>
<td>17.4</td>
</tr>

<tr>
<td>机器有颗玻璃心</td>
<td>https://zhuanlan.zhihu.com/wjdml</td>
<td>王晋东不在家</td>
<td>33</td>
<td>2016-06-11</td>
<td>2017-12-19</td>
<td>17.5454545455</td>
</tr>

<tr>
<td>机器学习入门（ 台湾大学李宏毅课程笔记 ）</td>
<td>https://zhuanlan.zhihu.com/holeung-ml</td>
<td>良多趣味</td>
<td>8</td>
<td>2017-08-22</td>
<td>2017-09-21</td>
<td>17.75</td>
</tr>

<tr>
<td>MachineLearning</td>
<td>https://zhuanlan.zhihu.com/MachineLearn</td>
<td>CycleUser 光喻</td>
<td>15</td>
<td>2017-04-18</td>
<td>2018-01-01</td>
<td>17.8666666667</td>
</tr>

<tr>
<td>生成对抗（GAN）的数学模型</td>
<td>https://zhuanlan.zhihu.com/c_111001507</td>
<td>王喆 酱油哥 郑哲东 江亦凡</td>
<td>10</td>
<td>2017-07-16</td>
<td>2017-12-12</td>
<td>17.9</td>
</tr>

<tr>
<td>机器学习专栏</td>
<td>https://zhuanlan.zhihu.com/c_114543440</td>
<td>QQ ZHOU</td>
<td>8</td>
<td>2017-08-20</td>
<td>2018-01-05</td>
<td>18.0</td>
</tr>

<tr>
<td>计算机视觉战队</td>
<td>https://zhuanlan.zhihu.com/Edison-G</td>
<td>EdisonGzq 酱油哥</td>
<td>24</td>
<td>2016-10-28</td>
<td>2017-10-31</td>
<td>18.3333333333</td>
</tr>

<tr>
<td>ResysChina</td>
<td>https://zhuanlan.zhihu.com/resyschina</td>
<td>谷文栋 项亮 刑无刀 王守崑 张相於</td>
<td>33</td>
<td>2016-05-14</td>
<td>2017-12-28</td>
<td>18.3939393939</td>
</tr>

<tr>
<td>8层会议室</td>
<td>https://zhuanlan.zhihu.com/8thfloor</td>
<td>孙玉玺 谢泽华 周泽南 董国盛 黑鱼 花花 叶知秋 常庆丰 潘达</td>
<td>15</td>
<td>2017-04-06</td>
<td>2017-11-27</td>
<td>18.6666666667</td>
</tr>

<tr>
<td>极简深度学习-没有最简单只有更简单</td>
<td>https://zhuanlan.zhihu.com/AIEDU</td>
<td>Miruku Zhang</td>
<td>1</td>
<td>2017-12-23</td>
<td>2017-12-23</td>
<td>19.0</td>
</tr>

<tr>
<td>机智过人</td>
<td>https://zhuanlan.zhihu.com/jizhiguoren</td>
<td>张盼锋</td>
<td>8</td>
<td>2017-08-12</td>
<td>2017-11-21</td>
<td>19.0</td>
</tr>

<tr>
<td>Video Analysis 论文笔记</td>
<td>https://zhuanlan.zhihu.com/wzmsltw</td>
<td>林天威</td>
<td>14</td>
<td>2017-04-19</td>
<td>2017-12-29</td>
<td>19.0714285714</td>
</tr>

<tr>
<td>单目深度估计</td>
<td>https://zhuanlan.zhihu.com/MonocularDepthEstimation</td>
<td>究竟灰</td>
<td>6</td>
<td>2017-09-18</td>
<td>2017-12-06</td>
<td>19.1666666667</td>
</tr>

<tr>
<td>深度炼丹日常</td>
<td>https://zhuanlan.zhihu.com/pbypby</td>
<td>pby5</td>
<td>8</td>
<td>2017-08-10</td>
<td>2017-11-27</td>
<td>19.25</td>
</tr>

<tr>
<td>程序员——深度学习之路</td>
<td>https://zhuanlan.zhihu.com/neujiasj-jiazi</td>
<td>贾书军</td>
<td>13</td>
<td>2017-05-03</td>
<td>2018-01-05</td>
<td>19.4615384615</td>
</tr>

<tr>
<td>AIvsBI</td>
<td>https://zhuanlan.zhihu.com/lxwcel</td>
<td>AlphaYong</td>
<td>4</td>
<td>2017-10-24</td>
<td>2017-11-07</td>
<td>19.75</td>
</tr>

<tr>
<td>超智能体</td>
<td>https://zhuanlan.zhihu.com/YJango</td>
<td>YJango</td>
<td>23</td>
<td>2016-10-12</td>
<td>2017-12-23</td>
<td>19.8260869565</td>
</tr>

<tr>
<td>写给妹子的深度学习教程</td>
<td>https://zhuanlan.zhihu.com/dlgirls</td>
<td>花花</td>
<td>8</td>
<td>2017-08-05</td>
<td>2017-08-29</td>
<td>19.875</td>
</tr>

<tr>
<td>机器学习&深度学习--学术水准的理解</td>
<td>https://zhuanlan.zhihu.com/AIlearn</td>
<td>刘锐 唐路路</td>
<td>6</td>
<td>2017-09-12</td>
<td>2017-11-07</td>
<td>20.1666666667</td>
</tr>

<tr>
<td>Gryffindor</td>
<td>https://zhuanlan.zhihu.com/blueblood</td>
<td>见鹿</td>
<td>32</td>
<td>2016-04-05</td>
<td>2017-12-29</td>
<td>20.1875</td>
</tr>

<tr>
<td>深度学习从入门到出门</td>
<td>https://zhuanlan.zhihu.com/drl-robotics</td>
<td>Jessica lei tai</td>
<td>2</td>
<td>2017-11-30</td>
<td>2017-11-30</td>
<td>21.0</td>
</tr>

<tr>
<td>学术兴趣小组</td>
<td>https://zhuanlan.zhihu.com/academic-interests</td>
<td>Gapeng 安捷</td>
<td>15</td>
<td>2017-02-24</td>
<td>2018-01-04</td>
<td>21.4</td>
</tr>

<tr>
<td>Keras花式工具箱</td>
<td>https://zhuanlan.zhihu.com/fancykeras</td>
<td>Professor ho</td>
<td>4</td>
<td>2017-10-17</td>
<td>2018-01-06</td>
<td>21.5</td>
</tr>

<tr>
<td>凡人机器学习</td>
<td>https://zhuanlan.zhihu.com/garvin</td>
<td>Garvin Li</td>
<td>5</td>
<td>2017-09-25</td>
<td>2017-10-17</td>
<td>21.6</td>
</tr>

<tr>
<td>Microsoft认知工具集(CNTK)</td>
<td>https://zhuanlan.zhihu.com/msrcntk</td>
<td>王万霖</td>
<td>8</td>
<td>2017-07-22</td>
<td>2017-11-05</td>
<td>21.625</td>
</tr>

<tr>
<td>揭开知识库问答KB-QA的面纱</td>
<td>https://zhuanlan.zhihu.com/kb-qa</td>
<td>Losin 李枝蔚</td>
<td>14</td>
<td>2017-03-13</td>
<td>2017-06-20</td>
<td>21.7142857143</td>
</tr>

<tr>
<td>SDU_DeepLearning</td>
<td>https://zhuanlan.zhihu.com/sdudl</td>
<td>杜存宵 沈冬冬</td>
<td>5</td>
<td>2017-09-24</td>
<td>2017-12-12</td>
<td>21.8</td>
</tr>

<tr>
<td>马天猫的CS学习之旅</td>
<td>https://zhuanlan.zhihu.com/deeplearningcat</td>
<td>马天猫Masn</td>
<td>10</td>
<td>2017-06-07</td>
<td>2017-08-28</td>
<td>21.8</td>
</tr>

<tr>
<td>DL学习</td>
<td>https://zhuanlan.zhihu.com/focus-xin</td>
<td>赵欣</td>
<td>4</td>
<td>2017-10-14</td>
<td>2017-12-06</td>
<td>22.25</td>
</tr>

<tr>
<td>马索萌的编程乐园</td>
<td>https://zhuanlan.zhihu.com/c_112935541</td>
<td>马索萌</td>
<td>7</td>
<td>2017-08-07</td>
<td>2018-01-07</td>
<td>22.4285714286</td>
</tr>

<tr>
<td>不懂机器学习的架构师不是好CTO</td>
<td>https://zhuanlan.zhihu.com/architect-and-ml</td>
<td>文西</td>
<td>8</td>
<td>2017-07-11</td>
<td>2017-12-22</td>
<td>23.0</td>
</tr>

<tr>
<td>小强学AI</td>
<td>https://zhuanlan.zhihu.com/ai-life</td>
<td>李锋</td>
<td>13</td>
<td>2017-03-13</td>
<td>2017-04-13</td>
<td>23.3846153846</td>
</tr>

<tr>
<td>深度炼丹成长记</td>
<td>https://zhuanlan.zhihu.com/dlalchemy</td>
<td>顾秀森</td>
<td>11</td>
<td>2017-04-28</td>
<td>2017-12-03</td>
<td>23.4545454545</td>
</tr>

<tr>
<td>深度炼丹</td>
<td>https://zhuanlan.zhihu.com/python-ml</td>
<td>JackonYang Sherlock</td>
<td>15</td>
<td>2017-01-22</td>
<td>2017-12-31</td>
<td>23.6</td>
</tr>

<tr>
<td>职场人才学</td>
<td>https://zhuanlan.zhihu.com/people-insights</td>
<td>ANDii</td>
<td>18</td>
<td>2016-11-09</td>
<td>2017-01-23</td>
<td>23.7777777778</td>
</tr>

<tr>
<td>强化学习分享交流</td>
<td>https://zhuanlan.zhihu.com/hallean</td>
<td>hallean</td>
<td>13</td>
<td>2017-03-06</td>
<td>2017-06-26</td>
<td>23.9230769231</td>
</tr>

<tr>
<td>NLP初涉</td>
<td>https://zhuanlan.zhihu.com/c_87436989</td>
<td>饮水机小包</td>
<td>12</td>
<td>2017-03-29</td>
<td>2017-11-28</td>
<td>24.0</td>
</tr>

<tr>
<td>深度学习与计算机视觉</td>
<td>https://zhuanlan.zhihu.com/c_93469304</td>
<td>张雨石</td>
<td>1</td>
<td>2017-12-18</td>
<td>2017-12-18</td>
<td>24.0</td>
</tr>

<tr>
<td>夕小瑶的科技屋</td>
<td>https://zhuanlan.zhihu.com/xixiaoyao</td>
<td>夕小瑶Elsa</td>
<td>14</td>
<td>2017-02-06</td>
<td>2017-12-30</td>
<td>24.2142857143</td>
</tr>

<tr>
<td>机器学习每日一记</td>
<td>https://zhuanlan.zhihu.com/jiaopan</td>
<td>阿弎</td>
<td>3</td>
<td>2017-10-30</td>
<td>2017-12-18</td>
<td>24.3333333333</td>
</tr>

<tr>
<td>PMCAFF产品社区</td>
<td>https://zhuanlan.zhihu.com/pmcaff</td>
<td>阿德</td>
<td>38</td>
<td>2015-06-29</td>
<td>2017-07-18</td>
<td>24.3947368421</td>
</tr>

<tr>
<td>计算语言学</td>
<td>https://zhuanlan.zhihu.com/cl2017</td>
<td>张逸宸 乐正</td>
<td>8</td>
<td>2017-06-26</td>
<td>2017-10-22</td>
<td>24.875</td>
</tr>

<tr>
<td>深度神经网络论文阅读</td>
<td>https://zhuanlan.zhihu.com/deep-learning-paper-reading</td>
<td>十万泼皮</td>
<td>8</td>
<td>2017-06-25</td>
<td>2017-09-11</td>
<td>25.0</td>
</tr>

<tr>
<td>深度学习与ASIC</td>
<td>https://zhuanlan.zhihu.com/c_125883294</td>
<td>子非鱼</td>
<td>5</td>
<td>2017-09-08</td>
<td>2017-12-29</td>
<td>25.0</td>
</tr>

<tr>
<td>RT的论文笔记以及其他乱七八糟的东西</td>
<td>https://zhuanlan.zhihu.com/c_73407294</td>
<td>罗若天</td>
<td>14</td>
<td>2017-01-20</td>
<td>2018-01-06</td>
<td>25.4285714286</td>
</tr>

<tr>
<td>机器不学习</td>
<td>https://zhuanlan.zhihu.com/zhaoyeyu</td>
<td>天雨粟</td>
<td>9</td>
<td>2017-05-25</td>
<td>2017-08-05</td>
<td>25.6666666667</td>
</tr>

<tr>
<td>竹间智能-AI</td>
<td>https://zhuanlan.zhihu.com/emotibot</td>
<td>竹间智能 Emotibot</td>
<td>7</td>
<td>2017-07-11</td>
<td>2017-11-20</td>
<td>26.2857142857</td>
</tr>

<tr>
<td>大规模机器学习</td>
<td>https://zhuanlan.zhihu.com/largescale-ml</td>
<td>杨军</td>
<td>9</td>
<td>2017-05-19</td>
<td>2017-12-16</td>
<td>26.3333333333</td>
</tr>

<tr>
<td>Python数据分析</td>
<td>https://zhuanlan.zhihu.com/c_99646580</td>
<td>南寻</td>
<td>7</td>
<td>2017-07-10</td>
<td>2017-12-20</td>
<td>26.4285714286</td>
</tr>

<tr>
<td>Something about AI</td>
<td>https://zhuanlan.zhihu.com/c_84661256</td>
<td>起名什么的最烦啦</td>
<td>11</td>
<td>2017-03-24</td>
<td>2017-08-21</td>
<td>26.6363636364</td>
</tr>

<tr>
<td>MXNet与Gluon的黑科技工具箱</td>
<td>https://zhuanlan.zhihu.com/c_136290272</td>
<td>SCP-173</td>
<td>3</td>
<td>2017-10-23</td>
<td>2017-10-29</td>
<td>26.6666666667</td>
</tr>

<tr>
<td>机器学习杂记</td>
<td>https://zhuanlan.zhihu.com/neocortex</td>
<td>滕建超</td>
<td>19</td>
<td>2016-08-22</td>
<td>2017-03-04</td>
<td>26.6842105263</td>
</tr>

<tr>
<td>智能进化</td>
<td>https://zhuanlan.zhihu.com/intelligent-evolution</td>
<td>名师出高徒</td>
<td>7</td>
<td>2017-07-08</td>
<td>2017-09-11</td>
<td>26.7142857143</td>
</tr>

<tr>
<td>阿里智能服务官方技术</td>
<td>https://zhuanlan.zhihu.com/ali-iic</td>
<td>阿里服务小 AI</td>
<td>1</td>
<td>2017-12-15</td>
<td>2017-12-15</td>
<td>27.0</td>
</tr>

<tr>
<td>数字编程</td>
<td>https://zhuanlan.zhihu.com/codingmath</td>
<td>李飞腾</td>
<td>18</td>
<td>2016-09-06</td>
<td>2017-12-20</td>
<td>27.3333333333</td>
</tr>

<tr>
<td>钟少的自留地</td>
<td>https://zhuanlan.zhihu.com/WilliamZhong</td>
<td>钟少</td>
<td>6</td>
<td>2017-07-31</td>
<td>2017-12-23</td>
<td>27.3333333333</td>
</tr>

<tr>
<td>人工智能AI</td>
<td>https://zhuanlan.zhihu.com/AI-ArtificialIntelligence</td>
<td>Kai Zhao</td>
<td>11</td>
<td>2017-03-15</td>
<td>2017-11-14</td>
<td>27.4545454545</td>
</tr>

<tr>
<td>DL(Deep Learning)小记</td>
<td>https://zhuanlan.zhihu.com/Charles-Wang</td>
<td>Charles Wang</td>
<td>14</td>
<td>2016-12-15</td>
<td>2017-06-12</td>
<td>28.0</td>
</tr>

<tr>
<td>UAI人工智能</td>
<td>https://zhuanlan.zhihu.com/uai-rocks</td>
<td>Xiaohu Zhu</td>
<td>8</td>
<td>2017-06-01</td>
<td>2017-11-13</td>
<td>28.0</td>
</tr>

<tr>
<td>机器学习基础（Notes阅读）</td>
<td>https://zhuanlan.zhihu.com/c_102113428</td>
<td>大野人007</td>
<td>8</td>
<td>2017-05-31</td>
<td>2017-09-10</td>
<td>28.125</td>
</tr>

<tr>
<td>计算机视觉&自然语言处理论文笔记</td>
<td>https://zhuanlan.zhihu.com/warrenLiu</td>
<td>Warren liu</td>
<td>7</td>
<td>2017-06-27</td>
<td>2017-11-03</td>
<td>28.2857142857</td>
</tr>

<tr>
<td>NLP基础调研</td>
<td>https://zhuanlan.zhihu.com/c_66319515</td>
<td>叶舞冬阳</td>
<td>13</td>
<td>2017-01-08</td>
<td>2017-07-08</td>
<td>28.3076923077</td>
</tr>

<tr>
<td>通俗理解统计学习、深度学习、强化学习</td>
<td>https://zhuanlan.zhihu.com/c_127364494</td>
<td>James Zhang</td>
<td>4</td>
<td>2017-09-18</td>
<td>2017-12-03</td>
<td>28.75</td>
</tr>

<tr>
<td>键盘数据侠</td>
<td>https://zhuanlan.zhihu.com/c_104225745</td>
<td>zhenhang.sun</td>
<td>13</td>
<td>2016-12-30</td>
<td>2018-01-07</td>
<td>29.0</td>
</tr>

<tr>
<td>当推荐系统遇上深度学习</td>
<td>https://zhuanlan.zhihu.com/DLwithRS</td>
<td>somTian</td>
<td>8</td>
<td>2017-05-23</td>
<td>2017-09-17</td>
<td>29.125</td>
</tr>

<tr>
<td>非凸优化学习之路</td>
<td>https://zhuanlan.zhihu.com/optimization</td>
<td>未名 蠢蠢蠢的马瑟</td>
<td>7</td>
<td>2017-06-20</td>
<td>2017-12-24</td>
<td>29.2857142857</td>
</tr>

<tr>
<td>机器人的知识学习(robot knowledge)</td>
<td>https://zhuanlan.zhihu.com/robotknowledge</td>
<td>刘锐 周旭</td>
<td>4</td>
<td>2017-09-15</td>
<td>2017-10-25</td>
<td>29.5</td>
</tr>

<tr>
<td>爱生活－爱挖掘</td>
<td>https://zhuanlan.zhihu.com/jxlijunhao</td>
<td>质数</td>
<td>4</td>
<td>2017-09-15</td>
<td>2017-10-27</td>
<td>29.5</td>
</tr>

<tr>
<td>XavierLin的炼丹房</td>
<td>https://zhuanlan.zhihu.com/XavierLin</td>
<td>林梅林</td>
<td>8</td>
<td>2017-05-20</td>
<td>2017-10-31</td>
<td>29.5</td>
</tr>

<tr>
<td>机器学习 & 金融量化分析</td>
<td>https://zhuanlan.zhihu.com/jjscience</td>
<td>江嘉键</td>
<td>22</td>
<td>2016-04-02</td>
<td>2017-11-09</td>
<td>29.5</td>
</tr>

<tr>
<td>人工智能杂谈</td>
<td>https://zhuanlan.zhihu.com/allofai</td>
<td>Zhanxing Zhu</td>
<td>5</td>
<td>2017-08-16</td>
<td>2017-11-06</td>
<td>29.6</td>
</tr>

<tr>
<td>Russell Lab</td>
<td>https://zhuanlan.zhihu.com/russellcloud</td>
<td>魏鸿鑫</td>
<td>9</td>
<td>2017-04-17</td>
<td>2018-01-11</td>
<td>29.8888888889</td>
</tr>

<tr>
<td>深度学习技术研究</td>
<td>https://zhuanlan.zhihu.com/DeepLearningSelfDriving</td>
<td>程世东</td>
<td>4</td>
<td>2017-09-13</td>
<td>2017-12-31</td>
<td>30.0</td>
</tr>

<tr>
<td>用PyTorch进行自然语言处理</td>
<td>https://zhuanlan.zhihu.com/qiangnlp</td>
<td>叶强</td>
<td>5</td>
<td>2017-08-11</td>
<td>2017-08-28</td>
<td>30.6</td>
</tr>

<tr>
<td>行人重识别</td>
<td>https://zhuanlan.zhihu.com/personReid</td>
<td>郑哲东 孙奕帆 酱油哥 Simon John Xinqian Gu</td>
<td>9</td>
<td>2017-04-09</td>
<td>2018-01-03</td>
<td>30.7777777778</td>
</tr>

<tr>
<td>AI Insight</td>
<td>https://zhuanlan.zhihu.com/ai-insight</td>
<td>何之源</td>
<td>14</td>
<td>2016-11-05</td>
<td>2017-11-05</td>
<td>30.8571428571</td>
</tr>

<tr>
<td>GAN + 文本生成 + 读博干货</td>
<td>https://zhuanlan.zhihu.com/c_126470847</td>
<td>胡杨 Nango 明楠</td>
<td>4</td>
<td>2017-09-08</td>
<td>2017-12-02</td>
<td>31.25</td>
</tr>

<tr>
<td>误入机器学习的码农</td>
<td>https://zhuanlan.zhihu.com/c_65697563</td>
<td>吴海波</td>
<td>8</td>
<td>2017-05-03</td>
<td>2018-01-04</td>
<td>31.625</td>
</tr>

<tr>
<td>计算机视觉的心得分享</td>
<td>https://zhuanlan.zhihu.com/c_128846268</td>
<td>Xf Mao</td>
<td>3</td>
<td>2017-10-08</td>
<td>2017-10-29</td>
<td>31.6666666667</td>
</tr>

<tr>
<td>深度学习调参实验室</td>
<td>https://zhuanlan.zhihu.com/qianxiaosi</td>
<td>浅小思</td>
<td>7</td>
<td>2017-06-02</td>
<td>2017-07-20</td>
<td>31.8571428571</td>
</tr>

<tr>
<td>深度学习专栏</td>
<td>https://zhuanlan.zhihu.com/c_88759330</td>
<td>FLY.DL</td>
<td>2</td>
<td>2017-11-08</td>
<td>2017-11-12</td>
<td>32.0</td>
</tr>

<tr>
<td>深度学习-----学习笔记</td>
<td>https://zhuanlan.zhihu.com/DLsense</td>
<td>白冰</td>
<td>4</td>
<td>2017-09-04</td>
<td>2017-09-08</td>
<td>32.25</td>
</tr>

<tr>
<td>魔王们的暗黑炼金卷轴</td>
<td>https://zhuanlan.zhihu.com/moquant</td>
<td>黑猫Q形态 子元 侯亮</td>
<td>8</td>
<td>2017-04-25</td>
<td>2017-12-17</td>
<td>32.625</td>
</tr>

<tr>
<td>大牛讲堂</td>
<td>https://zhuanlan.zhihu.com/daniujiangtang</td>
<td>地平线机器人技术</td>
<td>9</td>
<td>2017-03-23</td>
<td>2017-09-13</td>
<td>32.6666666667</td>
</tr>

<tr>
<td>诗、远方和AI</td>
<td>https://zhuanlan.zhihu.com/road2ai</td>
<td>Jeffrey</td>
<td>10</td>
<td>2017-02-14</td>
<td>2017-03-08</td>
<td>33.1</td>
</tr>

<tr>
<td>有意思的数据挖掘</td>
<td>https://zhuanlan.zhihu.com/data-mining</td>
<td>felix</td>
<td>9</td>
<td>2017-03-11</td>
<td>2017-09-19</td>
<td>34.0</td>
</tr>

<tr>
<td>人工智能笔记</td>
<td>https://zhuanlan.zhihu.com/ainote</td>
<td>MAZE</td>
<td>8</td>
<td>2017-04-11</td>
<td>2017-12-21</td>
<td>34.375</td>
</tr>

<tr>
<td>过拟合的玄学</td>
<td>https://zhuanlan.zhihu.com/c_137978572</td>
<td>he010103</td>
<td>2</td>
<td>2017-11-01</td>
<td>2017-11-17</td>
<td>35.5</td>
</tr>

<tr>
<td>机器学习由浅入深以及信号处理</td>
<td>https://zhuanlan.zhihu.com/MLvsSP</td>
<td>chisy Liu</td>
<td>6</td>
<td>2017-06-09</td>
<td>2017-06-26</td>
<td>36.0</td>
</tr>

<tr>
<td>菜鸡的啄米日常</td>
<td>https://zhuanlan.zhihu.com/chicken-life</td>
<td>BigMoyan</td>
<td>17</td>
<td>2016-05-09</td>
<td>2017-04-21</td>
<td>36.0</td>
</tr>

<tr>
<td>Deep Learning Digest</td>
<td>https://zhuanlan.zhihu.com/deeplearningdigest</td>
<td>Franklin</td>
<td>5</td>
<td>2017-07-15</td>
<td>2017-07-21</td>
<td>36.0</td>
</tr>

<tr>
<td>挖掘知乎里有趣的东西</td>
<td>https://zhuanlan.zhihu.com/grapeot</td>
<td>grapeot Kumakuma</td>
<td>28</td>
<td>2015-03-31</td>
<td>2017-12-28</td>
<td>36.3214285714</td>
</tr>

<tr>
<td>前沿机器视觉</td>
<td>https://zhuanlan.zhihu.com/c_129797621</td>
<td>小胖鱼</td>
<td>3</td>
<td>2017-09-22</td>
<td>2017-10-02</td>
<td>37.0</td>
</tr>

<tr>
<td>樱园的玻尔兹曼机</td>
<td>https://zhuanlan.zhihu.com/Boltzmannmachine</td>
<td>曾冠奇</td>
<td>7</td>
<td>2017-04-23</td>
<td>2017-07-11</td>
<td>37.5714285714</td>
</tr>

<tr>
<td>deep learning</td>
<td>https://zhuanlan.zhihu.com/c_108748033</td>
<td>gao jerevon</td>
<td>5</td>
<td>2017-07-07</td>
<td>2017-08-18</td>
<td>37.6</td>
</tr>

<tr>
<td>人工智能应用系列</td>
<td>https://zhuanlan.zhihu.com/ai4application</td>
<td>罗韵 安捷</td>
<td>8</td>
<td>2017-03-13</td>
<td>2018-01-05</td>
<td>38.0</td>
</tr>

<tr>
<td>何声欢的专栏</td>
<td>https://zhuanlan.zhihu.com/heshenghuan</td>
<td>何声欢</td>
<td>4</td>
<td>2017-08-11</td>
<td>2017-11-07</td>
<td>38.25</td>
</tr>

<tr>
<td>程序员深度学习笔记</td>
<td>https://zhuanlan.zhihu.com/deepLearning-from-programmer-view</td>
<td>王尧</td>
<td>7</td>
<td>2017-04-16</td>
<td>2017-11-11</td>
<td>38.5714285714</td>
</tr>

<tr>
<td>人工智能从入门到逆天杀神(AI-Man)</td>
<td>https://zhuanlan.zhihu.com/ai-man</td>
<td>桔了个仔 金天</td>
<td>6</td>
<td>2017-05-20</td>
<td>2017-11-24</td>
<td>39.3333333333</td>
</tr>

<tr>
<td>机器学习与人工智能</td>
<td>https://zhuanlan.zhihu.com/ml4ai</td>
<td>DeepFutureTech</td>
<td>8</td>
<td>2017-03-01</td>
<td>2017-10-08</td>
<td>39.5</td>
</tr>

<tr>
<td>知识图谱和智能问答</td>
<td>https://zhuanlan.zhihu.com/kg-qa</td>
<td>漆桂林 量子胖比特</td>
<td>4</td>
<td>2017-08-03</td>
<td>2017-11-07</td>
<td>40.25</td>
</tr>

<tr>
<td>Study of Object Detection and Tracking</td>
<td>https://zhuanlan.zhihu.com/c_105173048</td>
<td>飞彦</td>
<td>5</td>
<td>2017-06-22</td>
<td>2017-11-20</td>
<td>40.6</td>
</tr>

<tr>
<td>写给大家看的机器学习书</td>
<td>https://zhuanlan.zhihu.com/machine-learning-book</td>
<td>八汰</td>
<td>8</td>
<td>2017-02-20</td>
<td>2017-11-06</td>
<td>40.625</td>
</tr>

<tr>
<td>数据冷知识</td>
<td>https://zhuanlan.zhihu.com/c_129890466</td>
<td>敬清贺</td>
<td>2</td>
<td>2017-10-21</td>
<td>2017-10-30</td>
<td>41.0</td>
</tr>

<tr>
<td>机器学习笔记</td>
<td>https://zhuanlan.zhihu.com/c_120229701</td>
<td>子楠 PENG woodyhui 宋小伟 知予 余帅 Michael Yuan Wenliang 岭大王</td>
<td>14</td>
<td>2016-06-12</td>
<td>2017-12-31</td>
<td>41.2857142857</td>
</tr>

<tr>
<td>legblog</td>
<td>https://zhuanlan.zhihu.com/legblog</td>
<td>ZHAHZHI</td>
<td>2</td>
<td>2017-10-20</td>
<td>2017-11-10</td>
<td>41.5</td>
</tr>

<tr>
<td>直观梳理深度学习</td>
<td>https://zhuanlan.zhihu.com/c_145288300</td>
<td>Hao Zhang</td>
<td>1</td>
<td>2017-11-30</td>
<td>2017-11-30</td>
<td>42.0</td>
</tr>

<tr>
<td>人工智能与固件开发</td>
<td>https://zhuanlan.zhihu.com/mlfirmware</td>
<td>老狼</td>
<td>7</td>
<td>2017-03-21</td>
<td>2017-09-15</td>
<td>42.2857142857</td>
</tr>

<tr>
<td>CoolMoon</td>
<td>https://zhuanlan.zhihu.com/c_125027820</td>
<td>Tyler</td>
<td>3</td>
<td>2017-09-06</td>
<td>2018-01-10</td>
<td>42.3333333333</td>
</tr>

<tr>
<td>趣AI</td>
<td>https://zhuanlan.zhihu.com/qu-ai</td>
<td>晓雷</td>
<td>7</td>
<td>2017-03-19</td>
<td>2017-03-23</td>
<td>42.5714285714</td>
</tr>

<tr>
<td>高斯世界下的Machine Learning</td>
<td>https://zhuanlan.zhihu.com/gpml2016</td>
<td>蓦风星吟</td>
<td>9</td>
<td>2016-12-19</td>
<td>2017-11-27</td>
<td>43.1111111111</td>
</tr>

<tr>
<td>机器学习回顾总结</td>
<td>https://zhuanlan.zhihu.com/c_104934358</td>
<td>chlend</td>
<td>5</td>
<td>2017-06-08</td>
<td>2017-07-31</td>
<td>43.4</td>
</tr>

<tr>
<td>机器人眼中的数学</td>
<td>https://zhuanlan.zhihu.com/warden</td>
<td>李阳</td>
<td>7</td>
<td>2017-03-07</td>
<td>2017-10-18</td>
<td>44.2857142857</td>
</tr>

<tr>
<td>Knowledge Finder</td>
<td>https://zhuanlan.zhihu.com/text-summarization</td>
<td>苍穹之影</td>
<td>5</td>
<td>2017-06-03</td>
<td>2017-11-26</td>
<td>44.4</td>
</tr>

<tr>
<td>Deep Robotic Learning</td>
<td>https://zhuanlan.zhihu.com/deeproboticlearning</td>
<td>远方的梦</td>
<td>3</td>
<td>2017-08-30</td>
<td>2017-11-18</td>
<td>44.6666666667</td>
</tr>

<tr>
<td>机器爱学习</td>
<td>https://zhuanlan.zhihu.com/adventure</td>
<td>瑟木</td>
<td>3</td>
<td>2017-08-29</td>
<td>2017-11-22</td>
<td>45.0</td>
</tr>

<tr>
<td>小白机器学习</td>
<td>https://zhuanlan.zhihu.com/learnML</td>
<td>张三</td>
<td>9</td>
<td>2016-11-28</td>
<td>2017-08-05</td>
<td>45.4444444444</td>
</tr>

<tr>
<td>利用sklearn学习《统计学习方法》</td>
<td>https://zhuanlan.zhihu.com/c_109911171</td>
<td>Norlan</td>
<td>5</td>
<td>2017-05-28</td>
<td>2017-08-12</td>
<td>45.6</td>
</tr>

<tr>
<td>信号处理与机器学习</td>
<td>https://zhuanlan.zhihu.com/aresmiki</td>
<td>aresmiki</td>
<td>9</td>
<td>2016-11-20</td>
<td>2017-05-23</td>
<td>46.3333333333</td>
</tr>

<tr>
<td>深度学习:从入门到放弃</td>
<td>https://zhuanlan.zhihu.com/startdl</td>
<td>余俊</td>
<td>11</td>
<td>2016-08-18</td>
<td>2018-01-01</td>
<td>46.4545454545</td>
</tr>

<tr>
<td>机器学习和金融风控</td>
<td>https://zhuanlan.zhihu.com/liutengfei</td>
<td>LIU Tengfei</td>
<td>4</td>
<td>2017-07-09</td>
<td>2017-12-08</td>
<td>46.5</td>
</tr>

<tr>
<td>Learning Transfer</td>
<td>https://zhuanlan.zhihu.com/domain-adaptation</td>
<td>DomainAdaptation</td>
<td>6</td>
<td>2017-04-02</td>
<td>2017-11-11</td>
<td>47.3333333333</td>
</tr>

<tr>
<td>午夜末班车~12点后的你都在做什么</td>
<td>https://zhuanlan.zhihu.com/mmmuscle</td>
<td>mmmuscle</td>
<td>4</td>
<td>2017-07-05</td>
<td>2017-07-20</td>
<td>47.5</td>
</tr>

<tr>
<td>createamind-强人工智能探索</td>
<td>https://zhuanlan.zhihu.com/createamind</td>
<td>张德祥</td>
<td>15</td>
<td>2016-01-27</td>
<td>2017-11-29</td>
<td>47.6666666667</td>
</tr>

<tr>
<td>深度增强学习在机器人中的应用</td>
<td>https://zhuanlan.zhihu.com/c_143780402</td>
<td>段晋军</td>
<td>1</td>
<td>2017-11-24</td>
<td>2017-11-24</td>
<td>48.0</td>
</tr>

<tr>
<td>理论与机器学习</td>
<td>https://zhuanlan.zhihu.com/theoretical-machine-learning</td>
<td>袁洋</td>
<td>4</td>
<td>2017-07-01</td>
<td>2017-09-14</td>
<td>48.5</td>
</tr>

<tr>
<td>欲穷千里目</td>
<td>https://zhuanlan.zhihu.com/furthersight</td>
<td>魏秀参 高如如</td>
<td>12</td>
<td>2016-06-06</td>
<td>2017-12-20</td>
<td>48.6666666667</td>
</tr>

<tr>
<td>神经科学和人工智能</td>
<td>https://zhuanlan.zhihu.com/c_111334166</td>
<td>Harold Yue 李枝蔚</td>
<td>4</td>
<td>2017-06-30</td>
<td>2017-11-29</td>
<td>48.75</td>
</tr>

<tr>
<td>人工智能转型季</td>
<td>https://zhuanlan.zhihu.com/c_119554832</td>
<td>付饶</td>
<td>3</td>
<td>2017-08-16</td>
<td>2017-08-27</td>
<td>49.3333333333</td>
</tr>

<tr>
<td>Tensorflow自习室</td>
<td>https://zhuanlan.zhihu.com/c_123328743</td>
<td>张宸</td>
<td>1</td>
<td>2017-11-22</td>
<td>2017-11-22</td>
<td>50.0</td>
</tr>

<tr>
<td>深度学习笔记(NLP)</td>
<td>https://zhuanlan.zhihu.com/vortex</td>
<td>vortex</td>
<td>1</td>
<td>2017-11-22</td>
<td>2017-11-22</td>
<td>50.0</td>
</tr>

<tr>
<td>深度思考</td>
<td>https://zhuanlan.zhihu.com/yidianqx</td>
<td>剑明</td>
<td>3</td>
<td>2017-08-13</td>
<td>2017-12-09</td>
<td>50.3333333333</td>
</tr>

<tr>
<td>深度瞎学</td>
<td>https://zhuanlan.zhihu.com/c_143273356</td>
<td>Masonic</td>
<td>1</td>
<td>2017-11-21</td>
<td>2017-11-21</td>
<td>51.0</td>
</tr>

<tr>
<td>DestinedAI</td>
<td>https://zhuanlan.zhihu.com/destinedai</td>
<td>江龙泉</td>
<td>1</td>
<td>2017-11-21</td>
<td>2017-11-21</td>
<td>51.0</td>
</tr>

<tr>
<td>碧空的cv之旅</td>
<td>https://zhuanlan.zhihu.com/bikong2</td>
<td>bikong2</td>
<td>4</td>
<td>2017-06-16</td>
<td>2017-08-17</td>
<td>52.25</td>
</tr>

<tr>
<td>SYSU空间大数据分析</td>
<td>https://zhuanlan.zhihu.com/sysu-bigdata</td>
<td>尧大大</td>
<td>7</td>
<td>2017-01-08</td>
<td>2017-08-26</td>
<td>52.5714285714</td>
</tr>

<tr>
<td>pytorch-tutorials</td>
<td>https://zhuanlan.zhihu.com/tfygg-dl</td>
<td>飞彦</td>
<td>4</td>
<td>2017-06-13</td>
<td>2017-06-18</td>
<td>53.0</td>
</tr>

<tr>
<td>Hello 陈然！</td>
<td>https://zhuanlan.zhihu.com/chenran</td>
<td>陈然 严肃</td>
<td>30</td>
<td>2013-08-30</td>
<td>2017-12-22</td>
<td>53.1666666667</td>
</tr>

<tr>
<td>数据科学（Python/R/Julia）</td>
<td>https://zhuanlan.zhihu.com/tukey</td>
<td>Tukey</td>
<td>2</td>
<td>2017-09-25</td>
<td>2017-11-09</td>
<td>54.0</td>
</tr>

<tr>
<td>花花的闲言碎语</td>
<td>https://zhuanlan.zhihu.com/notebg</td>
<td>花花</td>
<td>3</td>
<td>2017-08-01</td>
<td>2017-12-07</td>
<td>54.3333333333</td>
</tr>

<tr>
<td>机器学习/强化学习/OpenCV</td>
<td>https://zhuanlan.zhihu.com/yohanna</td>
<td>Yohanna</td>
<td>11</td>
<td>2016-05-19</td>
<td>2017-07-28</td>
<td>54.7272727273</td>
</tr>

<tr>
<td>Machine Learning Notebook</td>
<td>https://zhuanlan.zhihu.com/machine-learning-notebook</td>
<td>QRcoding</td>
<td>3</td>
<td>2017-07-30</td>
<td>2017-11-11</td>
<td>55.0</td>
</tr>

<tr>
<td>随机漫步</td>
<td>https://zhuanlan.zhihu.com/c_80021505</td>
<td>water</td>
<td>2</td>
<td>2017-09-21</td>
<td>2018-01-05</td>
<td>56.0</td>
</tr>

<tr>
<td>从零记录机器学习</td>
<td>https://zhuanlan.zhihu.com/yxlml</td>
<td>Uqrayi</td>
<td>4</td>
<td>2017-05-29</td>
<td>2017-08-10</td>
<td>56.75</td>
</tr>

<tr>
<td>伐木NLP</td>
<td>https://zhuanlan.zhihu.com/nlp-farming</td>
<td>李浩</td>
<td>7</td>
<td>2016-12-09</td>
<td>2017-08-15</td>
<td>56.8571428571</td>
</tr>

<tr>
<td>七月的炼丹日常</td>
<td>https://zhuanlan.zhihu.com/c_122616931</td>
<td>七月</td>
<td>6</td>
<td>2017-02-02</td>
<td>2017-11-06</td>
<td>57.1666666667</td>
</tr>

<tr>
<td>深度学习算法研发之路</td>
<td>https://zhuanlan.zhihu.com/c_127157667</td>
<td>magic</td>
<td>2</td>
<td>2017-09-18</td>
<td>2017-09-18</td>
<td>57.5</td>
</tr>

<tr>
<td>Deep Learning Dairy</td>
<td>https://zhuanlan.zhihu.com/uuisstrong</td>
<td>pdbsettrace</td>
<td>1</td>
<td>2017-11-14</td>
<td>2017-11-14</td>
<td>58.0</td>
</tr>

<tr>
<td>机器人学习之路</td>
<td>https://zhuanlan.zhihu.com/learning-Robotics</td>
<td>卓求</td>
<td>5</td>
<td>2017-03-26</td>
<td>2018-01-10</td>
<td>58.2</td>
</tr>

<tr>
<td>机器学习极简主义</td>
<td>https://zhuanlan.zhihu.com/ml-simple</td>
<td>元峰</td>
<td>7</td>
<td>2016-11-28</td>
<td>2017-09-06</td>
<td>58.4285714286</td>
</tr>

<tr>
<td>数据科学与脑洞</td>
<td>https://zhuanlan.zhihu.com/white-bird</td>
<td>YING zz</td>
<td>2</td>
<td>2017-09-16</td>
<td>2017-10-08</td>
<td>58.5</td>
</tr>

<tr>
<td>DLC实验室</td>
<td>https://zhuanlan.zhihu.com/dlcode</td>
<td>ycszen</td>
<td>5</td>
<td>2017-03-24</td>
<td>2017-06-20</td>
<td>58.6</td>
</tr>

<tr>
<td>Learning to Drive</td>
<td>https://zhuanlan.zhihu.com/drl-driving</td>
<td>s7ev3n</td>
<td>1</td>
<td>2017-11-13</td>
<td>2017-11-13</td>
<td>59.0</td>
</tr>

<tr>
<td>神经网络--从入门到放弃</td>
<td>https://zhuanlan.zhihu.com/ligaoyi</td>
<td>沉迷学习的糕糕</td>
<td>3</td>
<td>2017-07-15</td>
<td>2017-07-31</td>
<td>60.0</td>
</tr>

<tr>
<td>深度学习与自然语言处理学习相关</td>
<td>https://zhuanlan.zhihu.com/nlpdl</td>
<td>吴洋</td>
<td>2</td>
<td>2017-09-11</td>
<td>2017-09-27</td>
<td>61.0</td>
</tr>

<tr>
<td>深度学习炼丹师</td>
<td>https://zhuanlan.zhihu.com/zhangbingyang</td>
<td>张冰洋</td>
<td>6</td>
<td>2017-01-05</td>
<td>2017-12-01</td>
<td>61.8333333333</td>
</tr>

<tr>
<td>Winsty的技术碎碎念</td>
<td>https://zhuanlan.zhihu.com/winsty</td>
<td>Naiyan Wang</td>
<td>2</td>
<td>2017-09-09</td>
<td>2017-10-19</td>
<td>62.0</td>
</tr>

<tr>
<td>ML@Scale</td>
<td>https://zhuanlan.zhihu.com/mlscale</td>
<td>张昊</td>
<td>2</td>
<td>2017-09-07</td>
<td>2017-11-16</td>
<td>63.0</td>
</tr>

<tr>
<td>机器学习教程</td>
<td>https://zhuanlan.zhihu.com/caorongyu</td>
<td>曹荣禹</td>
<td>4</td>
<td>2017-05-03</td>
<td>2017-12-04</td>
<td>63.25</td>
</tr>

<tr>
<td>深度学习</td>
<td>https://zhuanlan.zhihu.com/c_101308172</td>
<td>覃秉丰 燎原火 Walkers zchky</td>
<td>3</td>
<td>2017-07-04</td>
<td>2018-01-10</td>
<td>63.6666666667</td>
</tr>

<tr>
<td>量子计算与机器学习</td>
<td>https://zhuanlan.zhihu.com/c_124162493</td>
<td>金小龙</td>
<td>2</td>
<td>2017-09-05</td>
<td>2017-09-06</td>
<td>64.0</td>
</tr>

<tr>
<td>深度学习力</td>
<td>https://zhuanlan.zhihu.com/c_79640596</td>
<td>张轩铭</td>
<td>5</td>
<td>2017-02-24</td>
<td>2017-04-12</td>
<td>64.2</td>
</tr>

<tr>
<td>Statistics and SAS</td>
<td>https://zhuanlan.zhihu.com/-data-analysis</td>
<td>Mingjian Tian</td>
<td>10</td>
<td>2016-04-08</td>
<td>2017-09-10</td>
<td>64.3</td>
</tr>

<tr>
<td>TensorFlow从0到N</td>
<td>https://zhuanlan.zhihu.com/TensorFlowZeroToN</td>
<td>黑猿大叔</td>
<td>1</td>
<td>2017-11-07</td>
<td>2017-11-07</td>
<td>65.0</td>
</tr>

<tr>
<td>人工智能+机器学习+深度学习技术文章精选</td>
<td>https://zhuanlan.zhihu.com/c_86691882</td>
<td>优雅的程序员 App小公主</td>
<td>4</td>
<td>2017-04-25</td>
<td>2017-12-05</td>
<td>65.25</td>
</tr>

<tr>
<td>给小白的机器学习自学指南</td>
<td>https://zhuanlan.zhihu.com/MLForBeginners</td>
<td>华先森</td>
<td>2</td>
<td>2017-09-01</td>
<td>2017-09-03</td>
<td>66.0</td>
</tr>

<tr>
<td>过时的机器学习</td>
<td>https://zhuanlan.zhihu.com/gsdjqxx</td>
<td>ohm-FY</td>
<td>7</td>
<td>2016-09-27</td>
<td>2017-05-30</td>
<td>67.2857142857</td>
</tr>

<tr>
<td>灵魂机器</td>
<td>https://zhuanlan.zhihu.com/soulmachine</td>
<td>灵魂机器</td>
<td>7</td>
<td>2016-09-26</td>
<td>2017-04-25</td>
<td>67.4285714286</td>
</tr>

<tr>
<td>Machine Learning学习笔记</td>
<td>https://zhuanlan.zhihu.com/c_139039059</td>
<td>app Hael C</td>
<td>2</td>
<td>2017-08-28</td>
<td>2017-11-09</td>
<td>68.0</td>
</tr>

<tr>
<td>两分钟深度学习demo</td>
<td>https://zhuanlan.zhihu.com/gomxnet</td>
<td>lau phunter</td>
<td>6</td>
<td>2016-11-29</td>
<td>2017-09-06</td>
<td>68.0</td>
</tr>

<tr>
<td>无痛学习吧</td>
<td>https://zhuanlan.zhihu.com/painless8</td>
<td>刘新豪</td>
<td>7</td>
<td>2016-09-17</td>
<td>2016-10-29</td>
<td>68.7142857143</td>
</tr>

<tr>
<td>深度学习论文笔记</td>
<td>https://zhuanlan.zhihu.com/keithyin</td>
<td>y1n</td>
<td>4</td>
<td>2017-04-10</td>
<td>2017-06-30</td>
<td>69.0</td>
</tr>

<tr>
<td>脚本小子</td>
<td>https://zhuanlan.zhihu.com/c_120817953</td>
<td>Howie Zhao</td>
<td>2</td>
<td>2017-08-26</td>
<td>2017-09-20</td>
<td>69.0</td>
</tr>

<tr>
<td>山人.七-深度学习</td>
<td>https://zhuanlan.zhihu.com/shanren7</td>
<td>狗头山人七</td>
<td>5</td>
<td>2017-01-28</td>
<td>2017-02-06</td>
<td>69.6</td>
</tr>

<tr>
<td>泛化智能</td>
<td>https://zhuanlan.zhihu.com/giaitech</td>
<td>王汉洋</td>
<td>2</td>
<td>2017-08-23</td>
<td>2017-10-13</td>
<td>70.5</td>
</tr>

<tr>
<td>我爱机器学习</td>
<td>https://zhuanlan.zhihu.com/52mlnet</td>
<td>我爱机器学习</td>
<td>7</td>
<td>2016-08-19</td>
<td>2016-11-15</td>
<td>72.8571428571</td>
</tr>

<tr>
<td>机器学习实践</td>
<td>https://zhuanlan.zhihu.com/c_95758629</td>
<td>HYLL</td>
<td>4</td>
<td>2017-03-14</td>
<td>2017-05-14</td>
<td>75.75</td>
</tr>

<tr>
<td>AI带路党</td>
<td>https://zhuanlan.zhihu.com/ai-leader</td>
<td>郑华滨 刘思聪 吴晓晖</td>
<td>6</td>
<td>2016-10-08</td>
<td>2017-07-31</td>
<td>76.6666666667</td>
</tr>

<tr>
<td>我读过的NLP神经网络的论文解析</td>
<td>https://zhuanlan.zhihu.com/LarryYan</td>
<td>斐斐晏</td>
<td>3</td>
<td>2017-05-23</td>
<td>2017-08-09</td>
<td>77.6666666667</td>
</tr>

<tr>
<td>机器学习学习笔记</td>
<td>https://zhuanlan.zhihu.com/Xiong-Machine-Learning</td>
<td>公子我</td>
<td>4</td>
<td>2017-03-03</td>
<td>2017-03-25</td>
<td>78.5</td>
</tr>

<tr>
<td>炼丹实验室</td>
<td>https://zhuanlan.zhihu.com/easyml</td>
<td>萧瑟</td>
<td>8</td>
<td>2016-04-18</td>
<td>2017-04-06</td>
<td>79.125</td>
</tr>

<tr>
<td>深度学习笔记</td>
<td>https://zhuanlan.zhihu.com/limbosnote</td>
<td>Limbo 朦胧轻歌 吴明昊 Yu H</td>
<td>4</td>
<td>2017-02-28</td>
<td>2017-12-05</td>
<td>79.25</td>
</tr>

<tr>
<td>自然语言处理及算法</td>
<td>https://zhuanlan.zhihu.com/young-doctor</td>
<td>XXYY</td>
<td>2</td>
<td>2017-08-03</td>
<td>2017-08-04</td>
<td>80.5</td>
</tr>

<tr>
<td>Learning Machine</td>
<td>https://zhuanlan.zhihu.com/c_92047554</td>
<td>张潇捷</td>
<td>3</td>
<td>2017-05-12</td>
<td>2017-09-16</td>
<td>81.3333333333</td>
</tr>

<tr>
<td>数据科学民工</td>
<td>https://zhuanlan.zhihu.com/ppjai</td>
<td>wpppj</td>
<td>2</td>
<td>2017-08-01</td>
<td>2017-11-01</td>
<td>81.5</td>
</tr>

<tr>
<td>Python数据分析与挖掘</td>
<td>https://zhuanlan.zhihu.com/pyuse</td>
<td>李马宁</td>
<td>4</td>
<td>2017-02-16</td>
<td>2017-04-16</td>
<td>82.25</td>
</tr>

<tr>
<td>xlvector</td>
<td>https://zhuanlan.zhihu.com/xlvector</td>
<td>项亮</td>
<td>7</td>
<td>2016-06-13</td>
<td>2016-07-26</td>
<td>82.4285714286</td>
</tr>

<tr>
<td>集秀园</td>
<td>https://zhuanlan.zhihu.com/jarjar</td>
<td>红塔山</td>
<td>4</td>
<td>2017-02-15</td>
<td>2017-10-23</td>
<td>82.5</td>
</tr>

<tr>
<td>强化学习专栏</td>
<td>https://zhuanlan.zhihu.com/c_135831684</td>
<td>曾冠奇</td>
<td>1</td>
<td>2017-10-20</td>
<td>2017-10-20</td>
<td>83.0</td>
</tr>

<tr>
<td>院长日常</td>
<td>https://zhuanlan.zhihu.com/yuanzhangrichang</td>
<td>王岳王院长</td>
<td>3</td>
<td>2017-05-05</td>
<td>2017-10-26</td>
<td>83.6666666667</td>
</tr>

<tr>
<td>许韩VS许韩</td>
<td>https://zhuanlan.zhihu.com/xuhanvsxuhan</td>
<td>许韩</td>
<td>4</td>
<td>2017-02-09</td>
<td>2017-06-12</td>
<td>84.0</td>
</tr>

<tr>
<td>机器学习开发</td>
<td>https://zhuanlan.zhihu.com/c_61786941</td>
<td>TY Sun</td>
<td>5</td>
<td>2016-11-17</td>
<td>2017-11-12</td>
<td>84.0</td>
</tr>

<tr>
<td>Dense-Pixel Deep Learning</td>
<td>https://zhuanlan.zhihu.com/jiangqh</td>
<td>Jiang</td>
<td>3</td>
<td>2017-05-04</td>
<td>2017-07-27</td>
<td>84.0</td>
</tr>

<tr>
<td>机器学习道术器</td>
<td>https://zhuanlan.zhihu.com/machine-leanring</td>
<td>Shelley Lee</td>
<td>1</td>
<td>2017-10-18</td>
<td>2017-10-18</td>
<td>85.0</td>
</tr>

<tr>
<td>智能驾驶 机器学习 人工智能</td>
<td>https://zhuanlan.zhihu.com/c_127983768</td>
<td>陈浅DR</td>
<td>1</td>
<td>2017-10-18</td>
<td>2017-10-18</td>
<td>85.0</td>
</tr>

<tr>
<td>MLの玄学姿勢</td>
<td>https://zhuanlan.zhihu.com/x-ray</td>
<td>兔子老大</td>
<td>3</td>
<td>2017-04-23</td>
<td>2017-07-22</td>
<td>87.6666666667</td>
</tr>

<tr>
<td>深度学习计算框架</td>
<td>https://zhuanlan.zhihu.com/deeplearningframework</td>
<td>殷康</td>
<td>1</td>
<td>2017-10-13</td>
<td>2017-10-13</td>
<td>90.0</td>
</tr>

<tr>
<td>杨培文的文章</td>
<td>https://zhuanlan.zhihu.com/yangpw</td>
<td>杨培文</td>
<td>5</td>
<td>2016-10-16</td>
<td>2017-11-06</td>
<td>90.4</td>
</tr>

<tr>
<td>分布式机器学习系统</td>
<td>https://zhuanlan.zhihu.com/c_127078572</td>
<td>carbon zhang</td>
<td>1</td>
<td>2017-10-10</td>
<td>2017-10-10</td>
<td>93.0</td>
</tr>

<tr>
<td>机器学习技法</td>
<td>https://zhuanlan.zhihu.com/ml-techniques</td>
<td>天一柯南</td>
<td>1</td>
<td>2017-10-09</td>
<td>2017-10-09</td>
<td>94.0</td>
</tr>

<tr>
<td>PRML</td>
<td>https://zhuanlan.zhihu.com/prml-paper-reading</td>
<td>郑梓豪</td>
<td>15</td>
<td>2014-03-01</td>
<td>2017-01-07</td>
<td>94.1333333333</td>
</tr>

<tr>
<td>深度学习实践笔记</td>
<td>https://zhuanlan.zhihu.com/c_88204917</td>
<td>郑一轩</td>
<td>3</td>
<td>2017-04-01</td>
<td>2017-04-03</td>
<td>95.0</td>
</tr>

<tr>
<td>深度强化学习基础</td>
<td>https://zhuanlan.zhihu.com/ikerpeng</td>
<td>iker peng</td>
<td>5</td>
<td>2016-09-21</td>
<td>2017-11-22</td>
<td>95.4</td>
</tr>

<tr>
<td>深海遨游</td>
<td>https://zhuanlan.zhihu.com/deeplearning-surfing</td>
<td>清凇</td>
<td>4</td>
<td>2016-12-13</td>
<td>2017-03-26</td>
<td>98.5</td>
</tr>

<tr>
<td>自然语言居酒屋</td>
<td>https://zhuanlan.zhihu.com/nlp-izakaya</td>
<td>斤木</td>
<td>6</td>
<td>2016-05-30</td>
<td>2017-03-17</td>
<td>98.5</td>
</tr>

<tr>
<td>机器学习与算法</td>
<td>https://zhuanlan.zhihu.com/dragonfive</td>
<td>dragon five</td>
<td>2</td>
<td>2017-06-26</td>
<td>2017-09-26</td>
<td>99.5</td>
</tr>

<tr>
<td>一个水管工写点札记的地儿</td>
<td>https://zhuanlan.zhihu.com/ympsea</td>
<td>lazyp</td>
<td>1</td>
<td>2017-10-03</td>
<td>2017-10-03</td>
<td>100.0</td>
</tr>

<tr>
<td>travelsea的深度学习专栏</td>
<td>https://zhuanlan.zhihu.com/gwdlcv</td>
<td>taigw</td>
<td>3</td>
<td>2017-03-16</td>
<td>2017-11-13</td>
<td>100.333333333</td>
</tr>

<tr>
<td>苦海无涯，Python是岸</td>
<td>https://zhuanlan.zhihu.com/CHIWEIYUYZ</td>
<td>赤潍屿</td>
<td>2</td>
<td>2017-06-22</td>
<td>2017-07-20</td>
<td>101.5</td>
</tr>

<tr>
<td>ThinkStats - 我所理解的数据</td>
<td>https://zhuanlan.zhihu.com/understand</td>
<td>链球选手</td>
<td>5</td>
<td>2016-08-19</td>
<td>2016-12-10</td>
<td>102.0</td>
</tr>

<tr>
<td>什么值得爬</td>
<td>https://zhuanlan.zhihu.com/c_80099524</td>
<td>乔本大叔</td>
<td>3</td>
<td>2017-03-10</td>
<td>2018-01-05</td>
<td>102.333333333</td>
</tr>

<tr>
<td>自然语言处理</td>
<td>https://zhuanlan.zhihu.com/wpdida</td>
<td>zhugehun FeanLau</td>
<td>2</td>
<td>2017-06-15</td>
<td>2017-07-28</td>
<td>105.0</td>
</tr>

<tr>
<td>晴空一鹤</td>
<td>https://zhuanlan.zhihu.com/crane</td>
<td>张天亮</td>
<td>4</td>
<td>2016-11-17</td>
<td>2017-07-25</td>
<td>105.0</td>
</tr>

<tr>
<td>AutoVision</td>
<td>https://zhuanlan.zhihu.com/cyh24</td>
<td>仙道菜</td>
<td>5</td>
<td>2016-07-12</td>
<td>2016-07-12</td>
<td>109.6</td>
</tr>

<tr>
<td>Human Learning</td>
<td>https://zhuanlan.zhihu.com/AbsTF</td>
<td>Linghao Zhang</td>
<td>8</td>
<td>2015-08-15</td>
<td>2017-05-04</td>
<td>110.0</td>
</tr>

<tr>
<td>NLP日知录</td>
<td>https://zhuanlan.zhihu.com/ai-nlp</td>
<td>刘知远</td>
<td>4</td>
<td>2016-10-23</td>
<td>2018-01-08</td>
<td>111.25</td>
</tr>

<tr>
<td>AI搬砖工</td>
<td>https://zhuanlan.zhihu.com/liujshi</td>
<td>刘俊是</td>
<td>2</td>
<td>2017-06-02</td>
<td>2017-08-17</td>
<td>111.5</td>
</tr>

<tr>
<td>MoreTech</td>
<td>https://zhuanlan.zhihu.com/bugcreater</td>
<td>BugCreater</td>
<td>2</td>
<td>2017-05-31</td>
<td>2017-06-13</td>
<td>112.5</td>
</tr>

<tr>
<td>深度强化学习实战</td>
<td>https://zhuanlan.zhihu.com/lightaime</td>
<td>我爱吃三文鱼</td>
<td>1</td>
<td>2017-09-20</td>
<td>2017-09-20</td>
<td>113.0</td>
</tr>

<tr>
<td>舆观</td>
<td>https://zhuanlan.zhihu.com/dtade</td>
<td>舆观</td>
<td>1</td>
<td>2017-09-19</td>
<td>2017-09-19</td>
<td>114.0</td>
</tr>

<tr>
<td>机器学习从放弃到精通</td>
<td>https://zhuanlan.zhihu.com/masterml</td>
<td>桔了个仔</td>
<td>2</td>
<td>2017-05-20</td>
<td>2017-09-19</td>
<td>118.0</td>
</tr>

<tr>
<td>机器学习与石油</td>
<td>https://zhuanlan.zhihu.com/oglosers</td>
<td>大马猴爱吃瓜</td>
<td>1</td>
<td>2017-09-14</td>
<td>2017-09-14</td>
<td>119.0</td>
</tr>

<tr>
<td>数学与机器学习：Miniatures</td>
<td>https://zhuanlan.zhihu.com/ltbyron</td>
<td>李弢</td>
<td>3</td>
<td>2017-01-17</td>
<td>2017-03-01</td>
<td>119.666666667</td>
</tr>

<tr>
<td>遥感与机器学习</td>
<td>https://zhuanlan.zhihu.com/c_67013896</td>
<td>Drei</td>
<td>3</td>
<td>2017-01-09</td>
<td>2017-06-08</td>
<td>122.333333333</td>
</tr>

<tr>
<td>机器学习与模式识别入门</td>
<td>https://zhuanlan.zhihu.com/prml2016</td>
<td>涛涛涛</td>
<td>3</td>
<td>2016-12-30</td>
<td>2016-12-30</td>
<td>125.666666667</td>
</tr>

<tr>
<td>炼丹师的笔记本</td>
<td>https://zhuanlan.zhihu.com/syzhang</td>
<td>张松阳</td>
<td>4</td>
<td>2016-07-25</td>
<td>2017-12-24</td>
<td>133.75</td>
</tr>

<tr>
<td>机器学习提高班</td>
<td>https://zhuanlan.zhihu.com/yangnaisen</td>
<td>深度学生</td>
<td>4</td>
<td>2016-07-19</td>
<td>2017-09-24</td>
<td>135.25</td>
</tr>

<tr>
<td>当机器人遇上了学习</td>
<td>https://zhuanlan.zhihu.com/robotics-learning</td>
<td>江山 ChingKitWong</td>
<td>4</td>
<td>2016-07-19</td>
<td>2016-08-11</td>
<td>135.25</td>
</tr>

<tr>
<td>机器学习与数据挖掘</td>
<td>https://zhuanlan.zhihu.com/c_94980632</td>
<td>Eric Leo 侯文擎</td>
<td>3</td>
<td>2016-11-27</td>
<td>2017-11-21</td>
<td>136.666666667</td>
</tr>

<tr>
<td>机器学习算法</td>
<td>https://zhuanlan.zhihu.com/c_54294646</td>
<td>大Echo</td>
<td>1</td>
<td>2017-08-26</td>
<td>2017-08-26</td>
<td>138.0</td>
</tr>

<tr>
<td>Vector's Field 向量场</td>
<td>https://zhuanlan.zhihu.com/vector-field</td>
<td>vector</td>
<td>1</td>
<td>2017-08-25</td>
<td>2017-08-25</td>
<td>139.0</td>
</tr>

<tr>
<td>自学machine learning</td>
<td>https://zhuanlan.zhihu.com/c_89162134</td>
<td>夏路</td>
<td>2</td>
<td>2017-04-04</td>
<td>2017-04-04</td>
<td>141.0</td>
</tr>

<tr>
<td>Deep Learning</td>
<td>https://zhuanlan.zhihu.com/c_127979988</td>
<td>orangeprince DeepThinking</td>
<td>1</td>
<td>2017-08-19</td>
<td>2017-10-05</td>
<td>145.0</td>
</tr>

<tr>
<td>Tensorflow Basics Tutorial with Python</td>
<td>https://zhuanlan.zhihu.com/yoodoo-Tensorflow-Basics</td>
<td>yoodoo</td>
<td>2</td>
<td>2017-03-11</td>
<td>2017-04-06</td>
<td>153.0</td>
</tr>

<tr>
<td>Lawbda半生记</td>
<td>https://zhuanlan.zhihu.com/thug-life</td>
<td>胡莱人形</td>
<td>2</td>
<td>2017-03-05</td>
<td>2017-04-23</td>
<td>156.0</td>
</tr>

<tr>
<td>机器鼓励师手册</td>
<td>https://zhuanlan.zhihu.com/Stark</td>
<td>Stark Einstein</td>
<td>4</td>
<td>2016-04-26</td>
<td>2016-11-15</td>
<td>156.25</td>
</tr>

<tr>
<td>我的草稿——深度学习与视觉</td>
<td>https://zhuanlan.zhihu.com/c_115254772</td>
<td>刘宇鸣</td>
<td>1</td>
<td>2017-08-06</td>
<td>2017-08-06</td>
<td>158.0</td>
</tr>

<tr>
<td>人工智能之机器学习</td>
<td>https://zhuanlan.zhihu.com/c_115808207</td>
<td>王小雷</td>
<td>1</td>
<td>2017-08-02</td>
<td>2017-08-02</td>
<td>162.0</td>
</tr>

<tr>
<td>Machine Learning 学习笔记</td>
<td>https://zhuanlan.zhihu.com/c_115973526</td>
<td>Jay Wang</td>
<td>1</td>
<td>2017-07-31</td>
<td>2017-07-31</td>
<td>164.0</td>
</tr>

<tr>
<td>Learning Machine Rebuilt</td>
<td>https://zhuanlan.zhihu.com/lmrebuilt</td>
<td>豆豆叶</td>
<td>3</td>
<td>2016-08-29</td>
<td>2017-12-23</td>
<td>166.666666667</td>
</tr>

<tr>
<td>FindHao的机器学习魔法书</td>
<td>https://zhuanlan.zhihu.com/findhao-machinelearning</td>
<td>Find Hao</td>
<td>2</td>
<td>2017-02-08</td>
<td>2017-02-08</td>
<td>168.5</td>
</tr>

<tr>
<td>Photogrammetric Computer Vision</td>
<td>https://zhuanlan.zhihu.com/DL-PCV</td>
<td>木木哥</td>
<td>3</td>
<td>2016-08-03</td>
<td>2017-01-24</td>
<td>175.333333333</td>
</tr>

<tr>
<td>机器学习和模拟联合国</td>
<td>https://zhuanlan.zhihu.com/AllenCai</td>
<td>Allen Cai</td>
<td>5</td>
<td>2015-08-17</td>
<td>2015-10-29</td>
<td>175.6</td>
</tr>

<tr>
<td>深度知者</td>
<td>https://zhuanlan.zhihu.com/deepknower</td>
<td>徐潇然</td>
<td>2</td>
<td>2017-01-22</td>
<td>2017-10-02</td>
<td>177.0</td>
</tr>

<tr>
<td>机器学习的应用与发展</td>
<td>https://zhuanlan.zhihu.com/deep-learning</td>
<td>王晓光</td>
<td>2</td>
<td>2017-01-17</td>
<td>2017-05-19</td>
<td>179.5</td>
</tr>

<tr>
<td>技术的商业边界</td>
<td>https://zhuanlan.zhihu.com/jishubianjie</td>
<td>李明骏</td>
<td>2</td>
<td>2017-01-12</td>
<td>2017-03-30</td>
<td>182.0</td>
</tr>

<tr>
<td>DaveBobo的深度学习编程研究</td>
<td>https://zhuanlan.zhihu.com/c_109136323</td>
<td>DaveBobo</td>
<td>1</td>
<td>2017-07-12</td>
<td>2017-07-12</td>
<td>183.0</td>
</tr>

<tr>
<td>AI+安全试路人</td>
<td>https://zhuanlan.zhihu.com/taoanwang</td>
<td>小超超</td>
<td>1</td>
<td>2017-06-02</td>
<td>2017-06-02</td>
<td>223.0</td>
</tr>

<tr>
<td>机器学习个人笔记</td>
<td>https://zhuanlan.zhihu.com/awsomestuff</td>
<td>刘轩</td>
<td>1</td>
<td>2017-05-31</td>
<td>2017-05-31</td>
<td>225.0</td>
</tr>

<tr>
<td>移动端机器学习</td>
<td>https://zhuanlan.zhihu.com/Embedded-Machine-Learning</td>
<td>小包</td>
<td>1</td>
<td>2017-05-25</td>
<td>2017-05-25</td>
<td>231.0</td>
</tr>

<tr>
<td>深度算法</td>
<td>https://zhuanlan.zhihu.com/deepmentor</td>
<td>赵德丽</td>
<td>1</td>
<td>2017-05-23</td>
<td>2017-05-23</td>
<td>233.0</td>
</tr>

<tr>
<td>农村老伯学AI</td>
<td>https://zhuanlan.zhihu.com/zhenghaofei</td>
<td>Zhenghao Fei</td>
<td>2</td>
<td>2016-10-02</td>
<td>2016-12-22</td>
<td>233.0</td>
</tr>

<tr>
<td>对抗网络学习和发现</td>
<td>https://zhuanlan.zhihu.com/c_100457146</td>
<td>张骞晖</td>
<td>1</td>
<td>2017-05-20</td>
<td>2017-05-20</td>
<td>236.0</td>
</tr>

<tr>
<td>笨鸟的修炼</td>
<td>https://zhuanlan.zhihu.com/run-penguin</td>
<td>狂奔的企鹅</td>
<td>1</td>
<td>2017-05-16</td>
<td>2017-05-16</td>
<td>240.0</td>
</tr>

<tr>
<td>深度学习＆自然语言处理</td>
<td>https://zhuanlan.zhihu.com/DL4NLP</td>
<td>邱锡鹏 伟大隆重</td>
<td>2</td>
<td>2016-09-10</td>
<td>2017-05-23</td>
<td>244.0</td>
</tr>

<tr>
<td>物理与人工智能</td>
<td>https://zhuanlan.zhihu.com/c_96384501</td>
<td>纳米酱</td>
<td>1</td>
<td>2017-05-12</td>
<td>2017-05-12</td>
<td>244.0</td>
</tr>

<tr>
<td>用技术改变世界</td>
<td>https://zhuanlan.zhihu.com/liwenzhe</td>
<td>李文哲</td>
<td>3</td>
<td>2015-12-05</td>
<td>2016-11-23</td>
<td>256.0</td>
</tr>

<tr>
<td>机器学习与人工智能技术介绍与理解</td>
<td>https://zhuanlan.zhihu.com/vivounicorn</td>
<td>张磊</td>
<td>1</td>
<td>2017-04-27</td>
<td>2017-04-27</td>
<td>259.0</td>
</tr>

<tr>
<td>力学渣的机器学习笔记</td>
<td>https://zhuanlan.zhihu.com/c_93675165</td>
<td>力学渣</td>
<td>1</td>
<td>2017-04-24</td>
<td>2017-04-24</td>
<td>262.0</td>
</tr>

<tr>
<td>机器学习</td>
<td>https://zhuanlan.zhihu.com/machinelearning-deep</td>
<td>牧瀬 紅莉栖 倚楼 吕英斌 generaladolp qiaoDong</td>
<td>1</td>
<td>2017-04-24</td>
<td>2017-11-17</td>
<td>262.0</td>
</tr>

<tr>
<td>白话TensorFlow</td>
<td>https://zhuanlan.zhihu.com/c_91810432</td>
<td>LoYr</td>
<td>1</td>
<td>2017-04-19</td>
<td>2017-04-19</td>
<td>267.0</td>
</tr>

<tr>
<td>机器学习随想录</td>
<td>https://zhuanlan.zhihu.com/c_35601954</td>
<td>何钦尧</td>
<td>2</td>
<td>2016-07-24</td>
<td>2016-12-31</td>
<td>268.0</td>
</tr>

<tr>
<td>蓝猫的杂货铺</td>
<td>https://zhuanlan.zhihu.com/lanmao</td>
<td>bayesLr</td>
<td>3</td>
<td>2015-08-09</td>
<td>2017-01-30</td>
<td>295.333333333</td>
</tr>

<tr>
<td>Deep Learning Notes</td>
<td>https://zhuanlan.zhihu.com/c_74751706</td>
<td>Horan</td>
<td>1</td>
<td>2017-03-19</td>
<td>2017-03-19</td>
<td>298.0</td>
</tr>

<tr>
<td>饮马渭水</td>
<td>https://zhuanlan.zhihu.com/RoyTao</td>
<td>最帅的大厨</td>
<td>1</td>
<td>2017-03-06</td>
<td>2017-03-06</td>
<td>311.0</td>
</tr>

<tr>
<td>Binary Makes World</td>
<td>https://zhuanlan.zhihu.com/binary</td>
<td>xBinary</td>
<td>1</td>
<td>2017-03-06</td>
<td>2017-03-06</td>
<td>311.0</td>
</tr>

<tr>
<td>Understanding Deep Learning</td>
<td>https://zhuanlan.zhihu.com/c_81046807</td>
<td>bily lee</td>
<td>1</td>
<td>2017-03-04</td>
<td>2017-03-04</td>
<td>313.0</td>
</tr>

<tr>
<td>机器学习——从入门到放弃</td>
<td>https://zhuanlan.zhihu.com/cldpml</td>
<td>许九祀</td>
<td>1</td>
<td>2017-03-03</td>
<td>2017-03-03</td>
<td>314.0</td>
</tr>

<tr>
<td>立冬领域</td>
<td>https://zhuanlan.zhihu.com/lidong</td>
<td>立冬</td>
<td>1</td>
<td>2017-02-28</td>
<td>2017-02-28</td>
<td>317.0</td>
</tr>

<tr>
<td>人人都可以做深度学习应用</td>
<td>https://zhuanlan.zhihu.com/hansionxu</td>
<td>徐汉彬</td>
<td>1</td>
<td>2017-02-22</td>
<td>2017-02-22</td>
<td>323.0</td>
</tr>

<tr>
<td>稍微有点理论的机器学习笔记</td>
<td>https://zhuanlan.zhihu.com/mltheory</td>
<td>陈舒</td>
<td>1</td>
<td>2017-02-20</td>
<td>2017-02-20</td>
<td>325.0</td>
</tr>

<tr>
<td>Machine Learning with Python</td>
<td>https://zhuanlan.zhihu.com/DataForce</td>
<td>陈雷</td>
<td>1</td>
<td>2017-02-20</td>
<td>2017-02-20</td>
<td>325.0</td>
</tr>

<tr>
<td>机器人理财术</td>
<td>https://zhuanlan.zhihu.com/gotrading</td>
<td>林培勝</td>
<td>1</td>
<td>2017-02-15</td>
<td>2017-02-15</td>
<td>330.0</td>
</tr>

<tr>
<td>Logic vs NLP</td>
<td>https://zhuanlan.zhihu.com/c_73517338</td>
<td>Dead Pan</td>
<td>1</td>
<td>2017-01-21</td>
<td>2017-01-21</td>
<td>355.0</td>
</tr>

<tr>
<td>NLP深度学习项目实践集</td>
<td>https://zhuanlan.zhihu.com/nlpapp</td>
<td>陈俊文</td>
<td>1</td>
<td>2017-01-06</td>
<td>2017-01-06</td>
<td>370.0</td>
</tr>

<tr>
<td>深度疯子</td>
<td>https://zhuanlan.zhihu.com/deeplunatic</td>
<td>徐潇然</td>
<td>1</td>
<td>2017-01-05</td>
<td>2017-01-05</td>
<td>371.0</td>
</tr>

<tr>
<td>死磕“深度学习”</td>
<td>https://zhuanlan.zhihu.com/dl-ml</td>
<td>陈川</td>
<td>1</td>
<td>2016-12-21</td>
<td>2016-12-21</td>
<td>386.0</td>
</tr>

<tr>
<td>沉吟至今</td>
<td>https://zhuanlan.zhihu.com/duangexing</td>
<td>程引</td>
<td>1</td>
<td>2016-11-11</td>
<td>2016-11-11</td>
<td>426.0</td>
</tr>

<tr>
<td>深度学习与自然语言处理</td>
<td>https://zhuanlan.zhihu.com/nevermore-nlp</td>
<td>刘通 咸口锅包肉</td>
<td>1</td>
<td>2016-10-21</td>
<td>2017-12-13</td>
<td>447.0</td>
</tr>

<tr>
<td>EtaLi机器学习报告</td>
<td>https://zhuanlan.zhihu.com/ml-etali</td>
<td>li Eta</td>
<td>1</td>
<td>2016-09-11</td>
<td>2016-09-11</td>
<td>487.0</td>
</tr>

<tr>
<td>机器也学习</td>
<td>https://zhuanlan.zhihu.com/machinelearning</td>
<td>老饕</td>
<td>2</td>
<td>2015-05-06</td>
<td>2017-02-23</td>
<td>490.5</td>
</tr>

<tr>
<td>NLPer新手练习场</td>
<td>https://zhuanlan.zhihu.com/NLPBlog-WuYu</td>
<td>吴俣</td>
<td>1</td>
<td>2016-08-24</td>
<td>2016-08-24</td>
<td>505.0</td>
</tr>

<tr>
<td>【Machine Learning】</td>
<td>https://zhuanlan.zhihu.com/system</td>
<td>许九祀</td>
<td>2</td>
<td>2014-04-30</td>
<td>2017-03-09</td>
<td>676.0</td>
</tr>

<tr>
<td>Windweller's Studio</td>
<td>https://zhuanlan.zhihu.com/wstudio</td>
<td>紫杉</td>
<td>1</td>
<td>2015-11-09</td>
<td>2015-11-09</td>
<td>794.0</td>
</tr>

</table>