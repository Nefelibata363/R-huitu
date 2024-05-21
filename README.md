## [![Book build status](https://github.com/XiangyunHuang/msg/workflows/Render-Book/badge.svg?event=push)](https://github.com/XiangyunHuang/msg/actions?workflow=Render-Book)

## 现代统计图形

本仓库作为 [《现代统计图形》](https://bookdown.org/xiangyun/msg/) 书稿源码的托管地址

## Modern Statistical Graphics

This is code and text behind the [Modern Statistical Graphics](https://bookdown.org/xiangyun/msg/).

## 授权 LICENSE

<a rel="license" href="https://creativecommons.org/licenses/by-nc-sa/2.5/cn/"><img src="https://i.creativecommons.org/l/by-nc-sa/2.5/cn/88x31.png" alt="知识共享许可协议" style="border-width:0"/></a>

本作品采用<a rel="license" href="https://creativecommons.org/licenses/by-nc-sa/2.5/cn/">知识共享署名-非商业性使用-相同方式共享 2.5 中国大陆许可协议</a>进行许可。

------------------------------------------------------------------------

## 益辉答读者问

### 1. 统计图形在对信息高度浓缩的同时，怎么做到既美观，又简约？或者作图的美观性和传递信息的严谨性是怎样相辅相成的？是否在博弈？

美观通常是主观评价，所以这个问题不太容易回答。比如我个人崇尚极简主义，我认为简约本身就很美观，但也一定有很多人喜欢华丽或其它风格。统计图形要做到简约的话，说到底就是突出你想展现的主要信息，尽量淡化、隐去甚至去掉次要信息。下图是我若干年前看到的一幅动图，一步步展示了如何简化一幅繁杂的条形图，可供参考：

![data-ink](https://user-images.githubusercontent.com/12031874/131237513-474122a3-2ffd-4004-a4b2-f1105b2baf53.gif)

美观和严谨应该是互不冲突的，或者说二者并没有一定的关联。图形是一种信息编码方式，而且通常是对数值进行编码，只要读者在用眼睛解码时大概能正确解读和感知出真实的数据，那我觉得就算严谨了。严谨的图看起来可能好看，也可能不好看。比如对偏度很大的数据，无论画什么分布图（直方图、箱线图等），我觉得应该都不会“美观”，直方图会是一两根很高的柱子加上一长条扁平的尾巴、箱线图会是一个瘪瘪的箱子加一些离群点，但这些图形都是严谨的。再比如三维透视图通常看起来好看，尤其是点缀上光源效果之后，看上去很逼真，但三维图形在人眼中的解码比二维平面图形低效，三维空间中每个元素都需要向三个平面投影才能解读它的数值，而且三维透视图也很容易造成视觉欺骗，所以美观的图也可能不严谨。

### 2. R和各大包更新了那么多代，内容会不会过时？

这个问题我在序言中回答过。本书尽量兼顾图形“道”与“术”，其中“道”的部分应该没那么容易过时。“术”的部分依赖于具体的工具，比如 R 和 R 包。R 的基础图形系统可以说在二十年间变化都比较少，但 R 包（比如 ggplot2）的变化确实会相对快一些。如果你注重稳定、希望十年前的作图代码还可以继续用，不妨可以试试基础图形系统。基础图形系统与 ggplot2 的区别我在序言中也有提到。

### 3. 现在一般用Python了，R的语法生疏了，怎么更好地读这本书呢？

这取决于你是否还有意愿把 R 捡起来。如果有，那么可以找个快速入门教程先复习一下基本概念和语法；如果没有，那么可以忽略书中具体的代码实现，其中相当一部分图形应该都是可以在别的语言中重现的。

### 4. 学习R语言需要数学基础吗？

如果不涉及到建模分析的话，那么几乎不需要数学基础，会数数的数学水平应该就够。

### 5. ggplot2 vs R基础绘图系统（哪个更胜一筹？）

各有所长。书的序言中有提到。归根结底，是抽象快捷和细节控制二者之间的平衡和取舍问题。

### 6. 统计图形的艺术性和功能性如何辩证看待？

艺术？艺术就是爆炸（迪达拉），还是永恒（赤砂蝎）？……我个人倾向于功能性优先（即永恒）。如果有人信奉艺术就是爆炸的美学，那我觉得可以关注一下纽约时报的可视化项目，它们有时候很有艺术性。另外有个做可视化的网站叫布丁，我个人觉得它的艺术性非常惊艳，供参考：<https://pudding.cool>

### 7. 真的一图胜千言吗？图形承载多大的信息量才合适，或者，清楚明白才是王道?

一图胜千言这话当然不绝对，有些“言”简练清晰有力，恐怕图也胜不了。比如左转中的一句“晋侯复假道于虞以伐虢”，和画一幅地图相比，恐怕还是文字会赢（地图很难体现文字中的“复”字）。有些数据要是用文字描述起来会很啰嗦，而画图出来则一目了然，这时候才容易一图胜千言。书中第一章提到的拿破仑行军图就是这样的例子。

难说图形承载多大的信息量合适，因为这有点涉及到主观判断。有读者喜欢信息简洁，有读者喜欢看尽量多的细节。我觉得也不一定非得一幅图里塞下所有信息，可以同一批数据用几幅图来分别展现不同的重点，比如有的图展现分布形状，有的图展现相关关系，有的图展现建模结果。

另外，也可以考虑使用交互式图形。在初始图形上显示相对简单的信息，留给读者交互探索的余地。要是读者想看更多细节，他可以自己去拖去点，哪里不会点哪里。

### 8. 对于高维数据的可视化，有没有很漂亮的表达方式？或者可否举一些精彩的例子呢？

高维数据最终还是要落到平面上来表达，所以通常都得降维。有些降维方式很巧妙，比如书中提到的调和曲线图（图 6.14）将高维数据表达成一条曲线，让曲线之间的距离正好能代表样本之间的欧氏距离。类似的还有多维标度法（Multidimensional scaling），它把高维数据表达在平面上的散点里，使得每两点之间的距离尽量跟它们真实的欧氏距离成正比。

如果不想降维，那也有办法，比如书中提到的平行坐标图（图 6.13）。我的博士导师们和合作者早年间曾开发了一个跨时代的软件工具叫 GGobi，只可惜后来后继无人、快要失传了，这个软件专注于高维数据可视化和交互式图形，其中它的高维可视化就是将高维数据不断用新的投影矩阵投到平面上，出来的动画效果就像是在持续扭转一个高维“数据球”，让你看到数据的不同侧面。背后涉及到的数学技术有投影寻踪（多诗意的名字，Projection pursuit）等等。

### 9. 撇开各种图形类型和工具，您认为画好一张统计图形，最重要的素质和要求是什么？

这个问题听起来像一道考试题，我不知道我是否有资格回答。论素质，我觉得还是要用心吧（参见我在序言中提到的“生命的别名就是心”）：用心处理数据，首先数据别搞错了；用心选用合适的图形元素表达关键的信息。论要求，我觉得让读者很快能解读出数据的特征，就算是很好的图形了；如果一幅图读起来有探案的效果、充满着惊奇，那就更好了。

### 10. 请问使用shiny显示实时图形应用会越来越多吗，技术难度会降低吗？

我个人感觉那种实时、交互式的图形会越来越多，但它们应该很难在可视化领域占据主导地位。在可预见的未来里，我觉得静态图形还会是主导。一方面，我觉得出版业应该不至于太快消亡，应该也有很多人倾向于读静态报告；另一方面，实时的动态图形真正读起来也比较耗费脑力，我觉得人脑承受不了这种信息量，就算动态图形成了主流，结果很可能会是多数人都审美疲劳或信息疲劳，变成“视而不见”。当然，这些只是我的猜测。

技术难度一定会降低的。

### 11. 您好，我买了这本新书。然后尝试了一下代码，发现: 输出的图表中，不显示汉字，请问这种情况该如何解决？

这种技术性问题不妨到论坛上问：<https://d.cosx.org> 但请按论坛的规矩发帖，提供相应的系统信息。

### 12. 想问问大佬这本书的定位是怎样的，以及阅读这本书的方法？

本书的前言回答了这个问题。

### 13. 这本书14年前就在网上开源啦，图灵出的书和网上内容相比，主要有哪些变化？

本书的后记里部分回答了这个问题。更详细的对比参见：<https://msg2020.pzhao.org>

### 14. 有哪些值得推荐的数据可视化工具？

这个问题听起来像个知乎问题，有点笼统。我从没在知乎上回答过问题，这个问题我也不知从何答起。什么“值得推荐”取决于“推荐了之后想拿它去做什么”。本书介绍的主要是 R，有点偏统计。现在江湖上的 JavaScript 酷炫可视化库也铺天盖地，我觉得也可以稍微关注一下，具体哪家强我就不点名了（我不是这方面的专家，而且我掌握的信息可能已经落后时代几年了）。

### 15. 本书对R语言的要求是什么样的？

可以初学者，也可以是熟悉 R 语言的程度。前言中有提到，依据对 R 掌握的不同等级，这本书可以有不同的读法。

### 16. Science/Nature的编辑偏好什么样的统计图形？

这个我不了解。最多只能提供一个数据点，就是魏太云开发的 corrplot 包在《科学》《自然》杂志上露面多次了；如果它有代表性的话，那我觉得图形还是清晰明了就可以了，估计那些编辑应该不至于会偏爱某一种或几种特定的统计图形，否则这种杂志就太封闭了。

### 17. 如何锻炼或者如何学习将数据图形化的能力；数据可视化的学习路径是什么有哪些途径获得实操项目？

可以从第一章中的名作开始学习，其实那些图并没有什么复杂之处：两条线、一群点、几块饼、一条带而已，但都清楚展现出了问题（尤其霍乱传染图和南丁格尔玫瑰图）。

关于实操项目，本书第 3 章介绍了十个实例，都是从新闻时事或者作者自己关心的问题里发展出来的。回答你自己关心的问题，往往是最好的研究和学习动力。

### 18. 我听说有一些统计的假设检验是针对异常值和离群点的。请问在实务中，是对数据先做异常值的假设检验，抛去统计上显著的异常值之后，用剩余的数据做统计图形更好，还是先把所有数据用统计图形展示，通过观察再去除异常值更好呢？谢谢

我觉得异常值在统计分析里可能都是被冤枉了。有句话叫：我不是异常值，我只是还没找到我的分布而已！要不要剔除所谓的异常值，得首先看异常值是正确还是错误的数据。要是本来就是错误数据，通过分析或画图发现了，那剔除掉没什么可说的。如果它是真实的正确数据，我觉得还是谨慎处理。

有异常值的图形往往不那么“好看”，但你得自问，是选择好看，还是选择真实？当然，我也并不觉得这二者互斥。只要空间和版面允许，完全可以画两幅图，一幅包含异常值，一幅不包含。不包含异常值的图形有助于看清剩下的数据的特征。

### 19. 统计绘图当中，不少GUI软件貌似在不少情况下效率更高:代码 vs GUI

本书的 2.2 小节中谈到了这个问题。如果是一次性的作图、作后即焚，而你感觉图形界面软件好用，那用一次也无妨。如果是注重图形的可重复性，那么用代码作图更方便；比如要是将来发现数据变了，那代码只需要重跑一遍即可，而哪里不会点哪里的图形界面软件就需要你再全程点一遍。
