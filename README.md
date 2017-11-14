## 2017.07.14（周五）早上
这是我第一篇`MarkDown`

今天任务
1. 调整C1参数
2. 想办法解决背景误差的问题

## 2017.07.15（周六）早上
重新转回notepad++上编写

今天周报改到下午2：30，思考一下解决掩膜的问题，游泳的事移到明天

现有的问题必须去直面，不能以放松逃避，已有问题是因为阈值选择的问题导致关键区域的过多问题

现在处理方式是重新加入BJND项，争取今天实现BJND的项目

## 2017.07.15（周六）中午
**大体思路：**
1. 加入BJND项
2. 修复左右视点亮度不一致而被误判区域
3. 修复因绘制方法重复而导致的大范围不一致

*思想调整：*
最近陷入了一阵浓浓的对前途不确定的迷茫中，需要拨开云雾见太阳才可，不要自暴自弃，自我堕落，碰到困难应该想要去克服，不要逃避

## 2017.07.17（周一）上午
今天计划两项任务：
1. 批处理文件的完成
2. 加入BJND项

## 2017.07.17（周一）上午
已经完成了批处理的任务，实现了每一个图片组分别保存结果，并将最后结果输出至txt文档

接下来实现BJND项

## 2017.07.17（周一）下午
睡醒了，感觉身体自我修复了下，接下来实现BJND

## 2017.07.17（周一）晚上
今天基本实现BJND，但是晚上突然发现上午的批处理任务中视点深度转视差没有考虑，马上解决了，但是其他6组映射失败，明天再来解决

明日任务，检测BJND有效性，测一下几个参数

## 2017.07.18（周二）上午
已经推测到昨天的批处理任务失败应该是四组图片组视差没有除以4造成的，马上实现

## 2017.07.18（周二）上午
已经完成批处理任务，但是发现了问题，有大量的中间的结构性空洞，思考是我没有考虑HL的因素，这一部分必须排除，无聊先看看拟合程度

## 2017.07.18（周二）下午
统计完成，发现加入BJND项总体性能有略微提升，在实现过程中，发现我公共空洞没有去掉，思考一下如何去掉

映射过去的空洞没考虑，计划今晚前解决，先整理已有工程的申明空间，在掩膜空间上下功夫

## 2017.07.18（周二）下午
已添加完成，正在统计，c1=0.1，待会儿测一下c1=0.2

## 2017.07.19（周三）上午
完成昨日下午的任务

完成了昨日下午的任务，发现排除重复空洞后，性能有大幅提升，但最终结果仍然不好，发现两个问题
1. 统计数据中，每组最后一个CBA值总会偏上去(View3,View4)
2. 数据较差的几组掩膜有问题

所以接下来先去看看掩膜的问题

## 2017.07.19（周三）晚上
修复掩膜后发现结果变差了，说明我的现在的掩膜修复算法有问题（不能排除映射两个像素的偏差）

下一步骤，针对性地对某几个图片组修复一下，提高一下总体质量，今天收工了

## 2017.07.20（周四）上午
沿着昨天晚上的计划走一走

## 2017.07.20（周四）晚上
今天跑了一组数据，解决了一个本来以为是编译器的问题，终于结果的PLCC上80了，不容易，还是值得肯定的

有一个需要确定下来，我的目标不是发论文，而是提出一种有效的衡量虚拟视点质量的评价指标

————2017.07.20深夜

明天继续来看尾巴总是要上升的原因(View3,View4组CBA值总会上升)
可能理由
1. 关键点增长的数目不足

## 2017.07.21（周五）上午
检查其他几组尾巴上涨的情况

发现并不是关键点增长数目不足的问题

下一步可以结合好的几组数据，进行针对性的优化，然后全局化

## 2017.07.21（周五）晚上
写完周报，收工

## 2017.07.24（周一）上午
今日计划：
1. 继续关键掩膜优化工作（晚上来做吧）
2. 找一篇3D质量评价文献（易实现）
3. 翻译垂直虚拟视点绘制文章
4. 下载C语言课件（已完成）

## 2017.07.24（周一）傍晚
工作4已完成
今晚就尝试工作1

关于工作1的思考：
首先认为JUNG的思路是正确的，那么就是说1.Aloe的拟合值低的问题就是可以解决的，那么我就想从掩膜区域入手，因为计算SSIM值部分应该是没有问题的，先看一下掩膜区域哪些可以改进

## 2017.07.25（周二）上午
继续昨晚的分析与思考，完成工作1

## 2017.07.25（周二）下午
修改至1/4，扩展至两个像素，然后实现下txt到exel转换，方便快捷的方式，然后实现下一次实现全组的PLCC、SROCC、RMSE值

## 2017.07.25（周二）晚上
将批处理改造地更智能了，进一步缩短了时间，方便了工作
处理了1/2，1/3，1/4，发现1/3效果最佳，这一部分还有最后一步工作可以做

## 2017.07.26（周三）上午
继续改进中值滤波方法（即在不同的情况下应用不同的中值滤波方法），考虑加入不同亮度的因素

发现最大的问题是映射不准确的问题，这个问题解决了，我估计最后效果都可能上0.9

## 2017.07.28（周五）上午
昨天没有记录日记，完成了bookarrival的视点校正，进入了1/2像素精度，效果有很大提升
今天继续完善，进度要加快了

## 2017.07.31（周一）上午
今天完成其余6组实验数据的修正，发给老彭

## 2017.07.31（周一）晚上
完成了预定指标，实现了双目非对称性失真的算法部分

## 2017.08.01（周二）早上
今日任务，实现bosc的算法，统计到我的里面来

## 2017.08.02（周三）早上
看完bosc的论文，尽可能实现，注意留意文章中的小点

## 2017.08.03（周四）早上
Finish the job started yesterday.

## 2017.08.03（周四）晚上
---
实验结果有了突破性进展，在上一阶段双目差异性失真特征基础上，又考虑了单视点内容角度的特征（对单视点关键性区域求取其平均结构相似度），然后通过对两个特征的联合考虑（即相乘），现有效果是

 Tables | Value 
--------|----------
 PLCC   | 0.910459 
 SROCC  | 0.9001 
 RMSE   | 8.950392 
 
---
 
## 2017.08.04（周五）下午
昨天晚上有些激动，所以没有更新 *daily* ，今天思路仍然漂浮着，打算先做些题目冷静以下，然后开始整理思路，争取今天晚上8点前把思路整理出来

## 2017.08.08（周二）上午
其实现今的任务是很艰巨的，要在一两周内完成论文的撰写工作，然后有两个重要的时间点，9月份要开题（之前要看完Z-warpping，并且初步开始工作了），明年3、4月份前必须完成第二个工作了，第三个工作也开始了。
---
现阶段主要任务就是完成论文的撰写，这周周报是要报告的

## 2017.08.09（周三）下午
不计一切代价开始论文的撰写工作，不要再把时间花费在兴趣项目上了，要回归主业，不然可能会站不稳，要赶紧扩大现阶段成果，就是这样。
计划今晚参考以往的周报，搭建起草框架，死命令，必须完成！！！

## 2017.08.14（周一）下午
今天在家里办公，实现了家里电脑的Win10系统及相关软件的安装，本次因为考虑到家里还是比较少待的，所以就不分区装双系统了，打算下午拆一下鼠标和键盘，量一下编码器的长度，还有键盘的误码问题，晚上的时候写写论文吧，顺带以本篇小日志测试一下新的*GIT DESKTOP*是否正常。

## 2017.08.15（周二）上午
成功pull回来本篇文档，来学校的任务很明确，就是完成论文的撰写，今天先完成我的方法部分。

## 2017.08.16（周三）下午
应该可以马上写完算法的第一部分了，刷了一些水题，刷到了24，接下去水题难刷了，对于红皮书看了3个月还没什么进展有些恼火，最多两天把它看完，还有matlab神经网络的书，速度速度，先写完论文。

## 2017.08.17（周四）下午
今天小小总结一下，论文还是进展缓慢
完成了*adobe master collection cs 6*中的*Photoshop*和*Premiere*的汉化，并同步百度云网盘
刷了将近30道水题，排名瞬间到了20，这股劲终于得到缓解了，接下来看红皮书，主攻方向（C++（尤其是类的部分）、数据结构、算法）

接下来在论文上面好好下功夫

## 2017.08.18（周五）晚上
终于把我的方法的第一部分写完了，还没有插图，写论文真的也是一件很累人的事情，不过好在终于是静下心来了，一切都会好起来的。

## 2017.09.05（周二）上午
今天从家里回来，新的学期开始了，首先应该完成政治的调研报告

## 2017.09.05（周二）中午
上午如期完成了政治的调研报告，发给组员最后审查，没有问题下午2点发给老师致歉，下午工作1：00开始，继续写论文，争取这周写完

## 2017.09.05（周二）晚上
事实证明，白天是可以效率很高的，导致晚饭就会很饿，脑力劳动消耗掉了吧，保持这个效率，晚上来了两个我不太喜欢的人，些许影响了我的心情，打算接下来晚上要多多锻炼了，一个优秀的*码农*是必须要有良好的体格的，2333

## 2017.09.06（周三）上午
昨天终于把该死的双目竞争失真特征的算法流程图画完了，今天争取把我的算法部分搞定

## 2017.09.06（周三）下午
今天下午突发情况，老彭交代接待了新研一的入座，大概花费了2个小时时间，也没有太大想要写文章的念头
补充一点：上午完成了校园行驶证的办理，大概花费1个半小时，期间有一些波折，院办及110此类行政机构完全按规章办事，非常死板，不过这也不怨她们，只能习惯这一点了
下午的剩下1个半小时，我打算看看红皮书，写写论文，看看*tensorflow*吧，就是这样了

## 2017.09.06（周三）傍晚
水逆，很焦躁，想敲疯狂敲代码来宣泄，来吧，学python，ok, *Challenge Accepted*

## 2017.09.06（周三）晚上
我突发奇想，想要做一个打字游戏（类似小时候玩的最原始的警察抓小偷），我发现我的手放在键盘上就拿不下来了，插空学一下QT

## 2017.09.06（周三）深夜
学了一个晚上的*Python*，初步入了门，发现其与*Matlab*一样作为解释性语言的优势，又融合了很多*C*语言中的优势，确实是一个不错的开发工具，其数据类型非常灵活，甚至可以变量自己对自己强制类型转换，今天看了选择、循环

选择
``` python
if:
	...
elif:
	...
else:
	...
```

循环
``` python
while n <= 100:
	sum += n
	n += 1
```

``` python
for i in names
	print(names[i])
```

明天需要完成算法撰写的部分，预计上午完成，另外数学建模工作马上开始了，抽出一点时间把*Matlab*看了，好了现在是晚上9点，锻炼去了，做一个高持久的码农，2333

## 2017.09.07（周四）上午
又一个不懂礼貌的傻家伙来了，无所谓，今天上午的任务是尽快完成我的算法部分

## 2017.09.07（周四）上午
今天上午突发很多杂事，开了一小时的新生见面会，然后帮助两个博士配网装系统，实际时间只有零碎的一个小时左右，无法完成预定计划，原计划算法部分中午继续赶工完成

## 2017.09.08（周五）上午
今天上午两项任务，一是完成我的算法部分，二是政治论文修改意见分工

## 2017.09.08（周五）上午
成功完成了预定的计划，准备开始撰写实验结果部分

## 2017.09.08（周五）下午
开开心心地刷了3小时的题目，看了一下排名，已经是2012级第2了，总排名17，距离12级第一86题，加油吧，这就是我下一步的目标
另一方面，着手开始写实验结果部分。

## 2017.09.09（周六）上午
交了25的教师节礼物，今天任务：
1、下午1点去听一下建模
2、上网了解一下数学建模常用模型
3、开始实验结果部分撰写

## 2017.09.09（周六）上午
补充：修改策略：
看常用模型短时间内无法提升，转而看近4年的题目，届时直接找相似题目

## 2017.09.10（周日）晚上
一个优秀的老师就是在学生心里种下一棵棵知识的种子，接下来的任务：
1、完成论文的撰写工作（下一周必须完成）
2、熟悉*Matlab*建模常用算法

## 2017.09.11（周一）晚上
今天停电加各种杂事，下午没有工作，晚上刷题2道，第二道26维空间的真心调得很累，不过终于是解决了，接下来要考虑写论文

## 2017.09.13（周三）中文
可以做一个练手的ps软件外加以前的打字练习软件

## 2017.09.15（周五）上午
终于完成了政治的暑期报告，投出去了，论文的修改还有大概一天左右的工作量，继续完成，建模的事情要抓紧了，今天冲刺看一下

## 2017.09.21（周四）晚上
建模工作已经完成，论文工作应尽快完成

## 2017.09.30（周六）中午
完成论文的修改工作，发给彭 抄送陈
速览完成开题报告的要求

## 2017.10.10（周二）上午
**突然发现未来就在我的手中，天高任鸟飞，海阔任鱼跃！！！**

## 2017.10.23（周一）上午
改进文章，给老彭修改，开始深度图修复的文献搜索

## 2017.10.26（周四）上午
每一天都过得无比清楚，近期计划：
1、和老彭商量论文投哪
2、看课题二文献
3、完成朱的实验

## 2017.10.30（周一）下午
1、尽快和陈芬商谈好论文投出的事宜
2、准备课题二的文献
3、帮助完成CAD的侧角度
4、完成朱的实验

## 2017.11.03（周五）上午
近期主要任务完成亮度均衡化探索

## 2017.11.05（周日）中午
在1小时内完成周报内容，补交彭宗举，抄送陈芬。

## 2017.11.06（周一）上午
尽力完成第二篇工作的内容。

## 2017.11.09（周四）上午
近期两件工作：
1、直方图匹配opencv实现
2、*web of science*入门及亮度域处理文献搜索

## 2017.11.13（周一）晚上
本周核心工作：阅读文献，整理思路

现已完成：焦任直、胡天佑、汪辉、郭明松、王来花的相关工作整理

接下来：整理出阅读顺序，分清内容和框架（现在正在转变方向，大量阅读是基础）

## 2017.11.14（周二）晚上
**新思路** ***多视点视频的前景剔除算法***

另外考虑做一个YUV类，读视频，处理帧的小程序