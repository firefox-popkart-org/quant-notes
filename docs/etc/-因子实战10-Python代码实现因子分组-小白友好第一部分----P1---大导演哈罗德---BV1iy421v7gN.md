# 【因子实战10】Python代码实现因子分组（小白友好第一部分） - P1 - 大导演哈罗德 - BV1iy421v7gN

好我是大导演哈罗德，欢迎回到我的量化频道，然后这一期呢我们先来看一个函数。

![](img/296410e2b5aeb10713745a2b0158888b_1.png)

首先同样的方法，我们这一期来把我们的这个呃。

![](img/296410e2b5aeb10713745a2b0158888b_3.png)

就是因子回测包的这个代码的一个非常重要的。

![](img/296410e2b5aeb10713745a2b0158888b_5.png)

也就是这个group return它是怎么来的，但是在此之前呢，有一个factor group这个数据集是怎么样啊。



![](img/296410e2b5aeb10713745a2b0158888b_7.png)

从最开始的这样的，我们这个第一拼因子的一个monthly的一个值。

![](img/296410e2b5aeb10713745a2b0158888b_9.png)

到我的一个monthly的一个分组，所以说大家看我们这期输入的一个数据集。

![](img/296410e2b5aeb10713745a2b0158888b_11.png)

是这个数据集，也就是每一个因子每个月对每个股票的一个值。

![](img/296410e2b5aeb10713745a2b0158888b_13.png)

我现在要做的是，对每个月的这些值进行一个分解，我要把它每个月分成五组，然后我要返回的呢就是这个值不再是值了，而是大家想想返回什么比较合适，而是12345，因为我要把它分成五组。

所以如果你分成12345之后，我去对应它的收益率的时候，我就更好去对应了，现在的话呢就不太好去做，那其实如果做这件事情，大家会觉得好像听起来很简单，因为你其实如果有一个函数。



![](img/296410e2b5aeb10713745a2b0158888b_15.png)

它可以直接把它自动的呃，就弄好不就好了吗，但是如果的确我觉得肯定可以有这个函数，Python一个非常好的方式方面呢就是它可以封装。



![](img/296410e2b5aeb10713745a2b0158888b_17.png)

大家就可以把这个函数封装起来，但是也是我为什么上节课就是把这个过程啊。

![](img/296410e2b5aeb10713745a2b0158888b_19.png)

直接呢就给大家呃，没有给大家展示。

![](img/296410e2b5aeb10713745a2b0158888b_21.png)

但是后台呢就有人私信给哈罗德，就说嗯那你其实呃没有把你的听众定位清晰，你的听众呢更多的就是一些对量化感兴趣，但是呢嗯可能有一些编程经验，或者是可能有一些金融经验。



![](img/296410e2b5aeb10713745a2b0158888b_23.png)

半懂不懂量化的，那如果是对于这些同学来讲，那他没有看到中间那个代码写的过程。

![](img/296410e2b5aeb10713745a2b0158888b_25.png)

我认为还是呃比较不能理解这个整个代码。

![](img/296410e2b5aeb10713745a2b0158888b_27.png)

它是怎么样从这样的一个数据集，变成一个我们最后想要的数据集。

![](img/296410e2b5aeb10713745a2b0158888b_29.png)

首先呢我这节课，所以说我这节课想要做的事情，就是一步一步带着大家去把这个代码写完，那可能呢因为时间会比较长，我会去把它分成三四节课的样子，然后一点一点的大家走起来，然后大家也可以在看我的视频的同时。

去做一下自己因子的这样的一个呃，实现跟着一个空的这个notebook。

![](img/296410e2b5aeb10713745a2b0158888b_31.png)

然后我觉得在这个过程中，大家还是会很有收获的，我首先呢先把我的这个CPLOT给他disable掉。

![](img/296410e2b5aeb10713745a2b0158888b_33.png)

为什么，因为我想一点一点的给大家展现出，这个代码是怎么写的，而不是要去用它来告诉我，首先我想给大家看一个函数叫stack。



![](img/296410e2b5aeb10713745a2b0158888b_35.png)

首先大家再看一下，我这个还呃这个数据极限长什么样。

![](img/296410e2b5aeb10713745a2b0158888b_37.png)

他现在是这样的，但是呢我觉得在写函数的时候，这是我的一个习惯。

![](img/296410e2b5aeb10713745a2b0158888b_39.png)

也是我会推荐大家去掌握的一个习惯，就是我们要一个月一个月的去做一个事情，我们想想我们的结果，我们从结果出发，结果呢是想把每个月的这样的一个因子值，转化成01234或者12345，我们把它打一个标签。



![](img/296410e2b5aeb10713745a2b0158888b_41.png)

它到底是属于第一组呢，还是属于第五组，如果是这样的一个情况，大家想对于这个数据集这个data frame。



![](img/296410e2b5aeb10713745a2b0158888b_43.png)

它是一个这样的一个143×5000。

![](img/296410e2b5aeb10713745a2b0158888b_45.png)

543的这样一个，我们说它是个matrix，但是我现在呢是想要把它进行。

![](img/296410e2b5aeb10713745a2b0158888b_47.png)

每个月进行一个因子值的处理，首先我们来看一下这个stack函数。

![](img/296410e2b5aeb10713745a2b0158888b_49.png)

哎呀这个stack函数做的是什么，大家会发现它呢去把这个一张饼相当于摊开了。

![](img/296410e2b5aeb10713745a2b0158888b_51.png)

也就是如果我们先来看看，它能不能进行一个数据的索引哦，它能它的第一个值呢就是这个，也就是说我的日期是第一个日期。



![](img/296410e2b5aeb10713745a2b0158888b_53.png)

也就是我第一个月月底的第一股票的第一个值，然后呢他呢就像是把这个成绩给摊开。

![](img/296410e2b5aeb10713745a2b0158888b_55.png)

所以我呢就可以把这个数据一个一个啊去进行。

![](img/296410e2b5aeb10713745a2b0158888b_57.png)

我想要的一个处理，首先这里面呢我先去定义一个值。

![](img/296410e2b5aeb10713745a2b0158888b_59.png)

也就是我最后想去获得的一个data是什么，大家如果用这个pd data frame。

![](img/296410e2b5aeb10713745a2b0158888b_61.png)

来把它先做一个从头到尾的一个命名，那首先index应该是什么index呢。

![](img/296410e2b5aeb10713745a2b0158888b_63.png)

我觉得呢他就可能要有不同，不不止一个index。

![](img/296410e2b5aeb10713745a2b0158888b_65.png)

像这个呃stack，它本身的index，如果大家把它打印下。

![](img/296410e2b5aeb10713745a2b0158888b_67.png)

大家会发现它是一个moi index，为什么有moi index，因为它每个index第一个index是时间。



![](img/296410e2b5aeb10713745a2b0158888b_69.png)

第二个index呢就是这个股票的代码，所以如果我们把这个moti index给它提取过来。

![](img/296410e2b5aeb10713745a2b0158888b_71.png)

我们学着他这个moti index来做一个处理的话，我们呢就是把这个from product去，把他之前的两个index给它做一个整合。



![](img/296410e2b5aeb10713745a2b0158888b_73.png)

那是哪两个index进行一个整合呢。

![](img/296410e2b5aeb10713745a2b0158888b_75.png)

那也就是d e p monthly，它的一个index和大家想想是什么。

![](img/296410e2b5aeb10713745a2b0158888b_77.png)

他的一个index，它的index jack数列了。

![](img/296410e2b5aeb10713745a2b0158888b_79.png)

那这个我们叫做什么，在data frame里叫做它的columns。

![](img/296410e2b5aeb10713745a2b0158888b_81.png)

所以说这样的话，我们就把第一批的columns，作为他的第二个啊index，那这样的话那我们就有了我的这个哦，我忘运用这个PNAS这个包，所以说这个函数是调不出来的，必须前面有个包才能把这个函数调出来。

然后他也给了我一个提示，然后OK这样我们已经有了啊，这个这个这个这个两个index。

![](img/296410e2b5aeb10713745a2b0158888b_83.png)

那两个index我们总要有给他们有一个名字吧。

![](img/296410e2b5aeb10713745a2b0158888b_85.png)

所以我们用这个names，来把我这个index来做一个命名。

![](img/296410e2b5aeb10713745a2b0158888b_87.png)

那很明显第一个呢就是时间，第二个呢我把它定义为asset。

![](img/296410e2b5aeb10713745a2b0158888b_89.png)

为什么叫asset，asset呢，就是它的一个。

![](img/296410e2b5aeb10713745a2b0158888b_91.png)

相当于股票股票就是一种i sad，然后这也就是一个命名，不是重点，OK大家会发现我这样的话呢，就相当于我我怎么说呢，我重启。



![](img/296410e2b5aeb10713745a2b0158888b_93.png)

我把这个我最后想得到的一个值和这个的stack。

![](img/296410e2b5aeb10713745a2b0158888b_95.png)

大家会发现这个是我现在有的这个值，我把它stack一下。

![](img/296410e2b5aeb10713745a2b0158888b_97.png)

它是一个什么样子，如果我去把它用data frame来给装一下，它也会是一个类似的这样的一个结构。

![](img/296410e2b5aeb10713745a2b0158888b_99.png)

那我现在想要的是什么，我现在把想把这个因子值拼接上去。

![](img/296410e2b5aeb10713745a2b0158888b_101.png)

这样的话大家会发现它是一一对应的对吧，这是我最后想得到的一个data，然后下一步我要做的是什么。

![](img/296410e2b5aeb10713745a2b0158888b_103.png)

也就是我刚刚做的这个第一P点stack。

![](img/296410e2b5aeb10713745a2b0158888b_105.png)

大家想想这样的话他会得到一个什么样的结果，他们就会把这个因子值对应着他的这个index。

![](img/296410e2b5aeb10713745a2b0158888b_107.png)

给它拼接上去，这也就是其实我觉得是pandas的一个好处，也是一个坏处，它的好处就是在于它非常的智能，它有很多奇奇奇怪怪的函数，可以让你去做很多的有趣的设计，但它的坏处就是在于它可以，它就会让你去啊。

这个这个很混乱，因为你不知道这个函数万一可以这么用，万一可以，那没有，但我发现其实我这样做做错了，为什么呢。



![](img/296410e2b5aeb10713745a2b0158888b_109.png)

因为我直接把它复制出来，所以说他现在不是一个data frame的形式了，所以其实这里面呢我应该要有一个命名，那这个值应该命名成什么呢，如果大家跟得上我的思路的话。



![](img/296410e2b5aeb10713745a2b0158888b_111.png)

大家可以随时暂停，然后自己想想，这里面应该是个factor啊，就是我刚刚的那个factor之位。

![](img/296410e2b5aeb10713745a2b0158888b_113.png)

应该把factor这一列定义为他的这个stack，而不是把整个数据集用完它。

![](img/296410e2b5aeb10713745a2b0158888b_115.png)

OK那根据这样的话，你看看这两个是我们的index，然后呢这就是我的一个factor。

![](img/296410e2b5aeb10713745a2b0158888b_117.png)

然后大家也会发现哦，也是跟我们想的一样，你像这每个股票我想要包含。

![](img/296410e2b5aeb10713745a2b0158888b_119.png)

可是他不可能每天都有这个因子值，那如果没有，这些因子值的这个股票我应该怎么办呢。

![](img/296410e2b5aeb10713745a2b0158888b_121.png)

那也就是一个很简单的一个，如果听到这里。

![](img/296410e2b5aeb10713745a2b0158888b_123.png)

大家应该对这些函数都应该是比较熟悉了，就是drop。

![](img/296410e2b5aeb10713745a2b0158888b_125.png)

然后所用的一个subset是等于什么呢。

![](img/296410e2b5aeb10713745a2b0158888b_127.png)

因为如果你光照不到的话，他应该会把整行全是那样的，才会把它照，也有可能不是这个的话，就就会发现，其实我我我也不可能，所有的函数应该怎么做都能记住，但是我知道每次我该用什么函数的时候。

我我我我知道要去哪里找。

![](img/296410e2b5aeb10713745a2b0158888b_129.png)

我觉得这个呢也是我们整个呃想要写代码。

![](img/296410e2b5aeb10713745a2b0158888b_131.png)