# 清华博士带你学习python金融量化投资分析与股票交易【附项目实战】 - P66：68下单函数1 - python大师姐 - BV1BYyDYbEmW

OK好好，同学们，那我们接下来给大家写，就是怎么样下蛋嗯，现场写代码还是有点紧张，喝口水压人心，难免手一抖，好下单函数，我们说聚宽上给了四个下单函数，Order order，Target。

Order value，order target value啊，那这四个其实都可以，就是它们是一回事，这是我们的order，无非是这个传的是买的股数，order value传的是钱对吧。

那你其实无非就是什么呢，我把钱先算成我能买多少股，然后再买这些股对吧，然后那个order target是买到多少，买到多少股，那我就算一下我现在有多少股，然后再一减，然后就买多少股或者卖多少股对吧。

就这个意思，所以其实这几个这这四个函数，我们可以设计一个共同的函数，就共同的底层的这个这个下单函数，然后在这基础上再做一些，就是让那四个函数来调这个函数，懂了吗好那你有啥不明白的。

就是四个函数不能差不多嘛，我不要一样的代码写四遍了，我设置一个就是买卖函数，那我传可能传买卖多少，然后其他的再调查不就可以了吗，嗯了解就不要写四遍了，好那这个下单的时候，买卖的时候想到需要什么。

我们传进来的股票代码传进来的还有一个什么，这个一般来说是股数就是你买多少股对吧，那这个过程中，我们目的肯定是要去维护这个我们的仓位信息，就是账户信息就在这个里边，我买了之后。

我钱是不是减少我的这个catch对吧，钱是不是要给他减掉，对对吧，然后我的股票是不是要给他加进来，我买了那些股票，我就要把这股票放到我的position里面啊，这是这个，那相应的我们需要哪些信息呢。

我们是不是需要今天的股票价格嗯。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_1.png)

那今天的股票价格这个东西我们还没有写对吧，我们现在只有获取历史数据的函数。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_3.png)

那获取今天股票价格函数，我们可以写一个啊，给我们现在函数用，比如叫get to de，你怎么知道一般命名不都这样的，好传一个参数啊，是什么呢，是这个股票代码嗯，那今天的时间我们context点这。

context点DT是不是已经有了嗯，把它转换成，F把它转换成字符串，好把它叫做，比如叫today，就是今天的日期好，那同样我们要获取今天的价格，其实就是我去CSV这一行。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_5.png)

把这一天对应的这一行给他返回出去，对吧嗯好那跟之前的这个诶。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_7.png)

跟之前的这个它的写法一样啊，比如说我们try看看本地有没有F等于open，security加点CSV。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_9.png)

R啊，DF等于pd点read cs csv f时间啊啊不是时间。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_11.png)

这个读法一样，index c o l等于date，然后pass date等于pass，data等于date，然后这个时候我们是不是要把今天的选出来，所以点lock行选今天today是拼错了嗯。

DIAY列全选就可以。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_13.png)

然后把这个DF给它返回回去啊，其实这不是DF，这应该是一个series，因为我选定一行了啊，所以这不叫点叫data吧，叫叫叫data吧，好那就把它返回过去啊，啊那同理，如果说这个时候没有。

如果说这个本地没有啊。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_15.png)

except我们就啊data等于to share。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_17.png)

点get k data security。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_19.png)

开始时间和结束时间都是他today对，然后我们选出来第零行就可以了。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_21.png)

![](img/f68668d8ff469e27e02aec9f61ce6ef6_22.png)

获取今天的列权限啊，好这是我们的获取今天的数据。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_24.png)

我们来测试一下我标线是啥意思，说我这个空格太少了。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_26.png)

P1P8哎呀，毛病太多，这有啥意思，这个要写具体的我就不写了，这还i err一样是five not放在error对，fil not found erros啊，这样就没了，毛病太多唉。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_28.png)

行写吧，听他的来测试一下，没有感觉很好看，测试一下，get tadata data嗯，那这么传还是6。13185对，只能传他熟悉的6013181。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_30.png)

看哪报错了。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_32.png)

这报错了，说什么没有今天的价格哦。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_34.png)

我知道为什么了，因为现在这个DT刚开始。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_36.png)

我设置的是开始日期对吧。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_38.png)

嗯这个开始日期实际上你看他刚我传的是什么。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_40.png)

我传的是这个呃，1月1号，1月1号不是一个交易日对吧。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_42.png)

所以这个start date传进来之后，然后我在这该在这个today是1月1号，这个1月1号我去这找，然后没有这一天做，所以所以给报了一个错，对对吧啊。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_44.png)

这个时候也可以做，你在except一个什么这个except一个km。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_46.png)

然后你可以返回个NN，但是实际上我们啊用的时候是。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_48.png)

不会出现这个问题，因为我们DT刚开始啊，这个会一会儿我们再修改，因为不应该是start date，应该是start date，后一个交易日对应该是一对吧，应该是他的交易日。

所以这个地方我们来找到一个bug，我们一会再改好，To，嗯start date，后一个交易日好。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_50.png)

那我就稍微现在先不这么改，先怎么样呢，我们把started改一下，改成10号。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_52.png)

他还放假吗，他可能是个周末哎呀7号。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_54.png)

![](img/f68668d8ff469e27e02aec9f61ce6ef6_55.png)

嗯哎没报错，打印一下，好拿到了这一天的数据，这个any name的这个这是个编号，不用管它，Open close high low volume，这都拿到了好。

那我的这个get to the data就可以，就是我在比如说下单函数里，调用这个这个这个这个函数，那我就可以什么呀，我就可以直接获取到今天的价格，那我们一般以开盘价作为今天价格的模拟啊。

呃实际上就是我们在这个它的距宽在线平台上，大部分平台都是开盘，可能加一个叫做滑点，就所谓滑点是啥呢，就是说你买卖股票的价格，跟这个价格实际上会有差别，就不一定是你拿这个价格买。

因为你一天任何时间都可能买到这个，所以这个价格他做了一个华仔，相当于是32块钱，他这是会波动，比如说他他会这个变成34块钱买的，然后30块钱卖的就变成这种啊，但是我们不做化简之前。

我们就直接拿开盘价来作为，就假设你每天买的都是买卖，都是以开盘价买来的，好我们写一个带下划线的order，就表示这是一个这就是稍微隐藏一下，就是说这是会被其他人调的这么一个函数啊，它我们来获取通过呃。

有一传一个TADA塔键，就是把这个东西，把这个get tada塔的这个结果放到这儿，然后传什么security，还有什么amount，钱表示买的股，操作的股票和操作股票的数量嗯。

这个order函数其实挺有意思的，但是考虑的事情比较多啊，比如说你先要考虑什么呢，先要考虑他的钱是不是够嗯，如果，context点cash，这是你的钱，如果说你的钱不够，你就买不了了吧，你现在没钱了。

你还要下单，那就是不可能对吧，好看一下，它减去amount乘以价格，对不对，价格是啥价格，比如说我们这来一个P等于today data，对不对好，如果它减去amount乘以P小于零，我们就怎么样。

这时候说明说明钱不够，我是不是买股票要花这些钱，对啊对吧。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_57.png)

然后你就这么点钱，那就不够，那不够怎么办，我就给你打印一个不够呗。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_59.png)

现金不足啊，那其实我们还可以做一个什么事，就是说比如说哎我这个时候我还剩，可能还购买120股的，那我下了一个二百二百股的一个单，那这个时候我可以提醒他现金不足，同时我可以说我帮你调整成100股。

你不是能买100股吗，那你就买100好吧，那调整成调整成什么呢，我们来一个amount啊，这个值就要给它覆盖掉了，among等于什么呢，等于说我先看一下我的这个钱能卖多少股，能卖多少股。

是不是context点开始除以P啊，嗯对吧，如果说把它哎不是，如果就是把它转成可能是小数对吧，变成整数，它是不是能买这些股。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_61.png)

对不对，先不要考虑那个手的事啊，先不要考虑那个易手的事，我们是不是能买的结果对不对，所以这个时候我可以说现金不足啊，一，调整为，这些是不是就可以了嗯，好，嘶这是说现金不足的问题，那好多同学可能说了，哎。

我这个包括说你用户传递的这个amount，可能是比如说120，包括说你这调整之后的，你的amount可能是123，那这些其实都是不能交易的，因为说什么呢，除非你全部卖出。

否则的话你的交易数量必须是100的整数，100对吧，再，所以我们这判断如果amount不是100的倍数，就是除以100取余不得零，那这个时候我们是不是还要调整啊，那这个时候怎么调整。

先把amount改成什么，改成比如说我的amount是。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_63.png)

比如说给大家举个例子，这可能比较抽象啊，比如说我现在有这个amount是2345，他能买多少呢，23对，二三得二三，怎么算，取模运算，取模出来不45吗，所以应该是什么啊。

amount除以100是不是23。45对，把它转成整数是多少，23，然后呢in再乘以100吧，不就2300了吗，对不对，这这不就对了，所以amount应该调整成这个，然后这个时候再打印一下，说什么呢。

说这个啊不是100的倍数，已调整为百分号D，对不对，好这个时候其实我们可以看一下这个amount，如果是正的话，表示买对吧，如果是负的的话，有问题吗，负的负的话表示卖对吧，你正和负都要考虑，那负的的话。

这这半部分有问题吧，这半部分没问题对吧，这半部分肯定不会小于零，这肯定是正的对吧，正的加正的这个东西是负的吗，负的是减负的，就是正的，所以正的加正的肯定是正的，这个不可能小于零，就肯定不会说有这种情况。

没有问题对吧好，这个呢如果是负的的话，比如说你比如说我想amount等于，如果用户传进来，amount等于负的123。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_65.png)

这是不是不等于零啊，那amount除以100是多少，负的100，就如果用户想卖123股，那他现在应该是我给它调整成卖100股对吧，嗯啊那这个时候amount是-100，23÷100是-1。23。

变成int之后，我之前说过int是向零取整，所以他相当于把小数把点跟后边东西都去掉，所以他变成了一啊，-1×100就是-100，所以他要最后卖100股也是可以的，OK吧嗯好。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_67.png)

这是说这个啊，卖的情况也没有问题，那除了是不是100的倍数，这还有其他的还有什么要考虑的吗，买了股票不能写，其实在100的倍数里，这还有一点我刚才说了，说你要全仓卖出的时候，是可以不是100的倍数的。

但是这个有个问题是什么呢，就是说你买的时候都是一百一百的买，对不对，你要卖的时候，如果说没有其他因素的话，肯定是100位数对吧，但是我们之前说过有分红分红的话，有分红的话。

他就会比如说十股可能给你分一股，15，每十股分红一股，那你这样的话就可能你不是100的倍数啊，所以其实我们这考虑不考虑也行，如果说你要考虑的话，你就这样写，if amount是不是等于负的。

我现在有的数量，因为只有是卖的时候嘛对吧，A m o u u n t among，只有是负数的时候，并且这个负数正好等于我现在持有security的数量，的时候，是不是才OK，所以如果它不等于，什么呢。

Food context，点positions security，如果它不等于它，就说明不是全场百数，那这个时候就需要调整成100，就是如果视察你就不用调整了，就这个就else就是什么都不干好。

这一说填的是100的倍数，除此之外，你说还有什么，你觉得还有什么条件需要考虑，嗯卖出的股票不能大于你手中，对对对，你像你像我们现在考虑买了对吧，考虑买钱不够，你要是传卖的话，你有可能股票股。

你有可能你现在就100股，你说传进来，你想买200股，那是不行的，对吧好，所以你这考虑什么呢，是不是context点positions security，这是不是我现在有的数量，对不对。

amount是不是应该是卖的数量，所以我这样写啊，它如果小于负的amount没有空格啊，有空格都行，啧amount是如果说是amount是正数的话，它肯定是个负数对，然后它肯定是个正数。

正数不可能小于负数，所以这个时候如果among是正的，这个if永远不会执行，对不对，那咱举个例子啊，比如说我们现在有啊，有有300股好吧，如果说among的我是要买买的话，肯定右边的话肯定会是负的对吧。

买的话是它本身这有这这个负号，是这个负号啊，老八呢比如说我买200股啊，300肯定不会小于200，小于-200对吧，所以这个永远不会执行，只有当什么呢，只有当你amount是负的时候。

amount如果是负的，那你加个负号是验证的，比如说你想卖，你想卖400多，那你相当于你这传进来是-400对吧，这加个负号变成400了，好这个时候是不是左边小于右边。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_69.png)

那这个时候我是不是应该调整了，对给你调整成300对吧，嗯好，所以这个时候我要调整成什么呢，我要把amount嗯调整成负的，就是你有多少，你本来说你现在有300股，你想卖450，对不起没有。

那你就只能是把现在这些组数所有卖出去啊，而且说你因为全仓卖出，所以你也不用考虑，说他后边你再要调整成100的倍数，不用了，全仓卖出嘛，嗯对吧好这我们再打印一下，啊叫做比说那些卖出股票。

不能不能超过当前持持仓的数量，已调整为，对不对。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_71.png)

嗯好啊，除此之外还有吗，还有限制吧，还有其他的就是用户输入的不对的地方，还是可以限制，其实还有一个就是什么呢，有可能有可能今天不卖，不是就不不是不是交易日。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_73.png)

肯定是交易日，因为我们什么，我们选出来的这个data range。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_75.png)

就已经是所有交易日了，但是不是交易日，交易日的时候，所有的股票都能买到，有可能这只股票今天停牌了，就被证监会查了，或者其他原因，他不卖，就其他股票都卖，就他但他可能不卖，那这个时候什么呢。

我们只要看一下今天的这个东西，是不是一个空的，就可以了啊。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_77.png)

就是看这获取今天的数据吗，我们之前是不是说过。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_79.png)

你之前是不是说过哪个问题啊，就刚才那个问题吗，我这传0101传进来的时候。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_81.png)

是不是这会报了一个错，对吧对对吧，所以这个时候我们可以这样搞。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_83.png)

正好现在就相当于非交易日和停牌是一个意思，所以我这样except，Key k l error，就是你找不到什么，找不到这个东西，对不对，你找不到这个东西，Except key error。

然后那我就这个时候我的data就等于什么，可以等于一个空的data for a series吧，对不对，可以对吧，那这个时候data就是它就是空的，所以说如果我到时候我在order里。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_85.png)

我判断如果这个data是空的的话，说明今天要么是非交易日，要么是停牌了。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_87.png)

对吧嗯好就在这最开始的时候我也加可以判断，如果在特today data a是空的啊，是空的的话，你可以就是可以，我们的这个pandas可以点empty，你也可以什么你也可以长度，是零的时候。

我们这儿打印一下什么呢，今日停牌，可以吧，那这个时候其实直接可以直接可以返回了。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_89.png)

就是其他都停牌的，你买和卖其他的后边就完全没必要执行了。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_91.png)

对不对，好，这是一些一些特殊情况，对还有吗，没了吧，那我暂时没有查了，就这些啊，这下挺有意思的，就是你要考虑完整，你考虑不完整的话，很有可能你的得分就是错的好，那然后接下来。

我们就要就要真正的去买或者卖了对吧，那啊买还是卖，我们要什么，我们要这个判断一下，首先更新两个东西，第一个东西是什么，我们要更新这个持仓的情况对吧，我要算本来我可能有哪些股票。

现在如果呃如果没有这些股票，我怎么办，对不对，哎如果说没有这些股票，我是不是零股，如果说有这些股票，我得给他加上这些股票，对不对，好，所以点POSITI是不是一个字典。

我想获取是不是security本来有多少苦，对不对，对不对，如果就是security本来有多少股，加上我的买的这个amount是不是就可以了，是不是就是我新的现在的数量对对，但是有一个什么问题。

我的security很有可能没有，就是我刚开始我是不是字典是空的，啊，对啊，我没有这个键，对不对，那怎么办呢，点get，默认值default等于零对吧。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_93.png)

get不到，就是这样，然后加上我的amount变成了一个什么，比如说我叫new among好。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_95.png)

这是我相当于是这个改完之后，我这个股票新的数量是这个对吧，嗯那我把它写到我的这个呃，写到我的这个什么里，这个这个啊其实不用VUE明白吗，直接写到我的context，点positions这个字典里啊。

对吧，然后接下来这是我更新的什么更新的持仓信息，然后接下来是不是要更新我的钱信息了，对啊，那更新我的钱的时候，我要判断什么，我这是买还是卖嘛，然后我要相应的这个其实不用判断，买是直接就可以啊。

我的cash，怎么办，是要加等于还是要减等于一个什么东西呢，如果说我的amount是正的的话，是不是买我的看看是不是减，所以我这写减减去什么amount乘以P。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_97.png)

![](img/f68668d8ff469e27e02aec9f61ce6ef6_98.png)

对不对嗯，P是我之前的价格。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_100.png)

对好，如果amount是卖的话，也没有问题，如果我MONT卖，这是不是负的，负的是乘一个它这这这这是一个这是一个负数，那这还有一个减负，负得正就加了对吧，所以这个是更新了我的什么，更新了我的签签好。

那最后还有一点别忘了是什么呢，说如果我的security更新之后的，security的这个持仓数量变成零了，怎么办，变成零了，要把它删掉，因为不然的话会有问题。

我们接下来我们之前是可能通过这个POSITI，这个一个security是不是in positions，来判断它是不是在是不是持仓，所以变成零了，要及时删掉啊，那就这样判断一下。

如果context点positions security等于零，那就怎么样，我就把它删掉啊，把不是把整个的删掉啊，是把这个东西删掉，就是把security这一这这一条删掉嗯好啊。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_102.png)

这是我的什么，这是我的order购买策略函数。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_104.png)

好，我们来简单的测试一下，当然这是一个底层的这个写法，我们上面还要写四层，而他要写四个函数，就是那个order order target那几个。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_106.png)

但是我们先测试一下，比如说啊因为只能买哎，第一个参数是t today data对吧。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_108.png)

特data塔就要传那个get特data这个函数进去，这个函数的结果啊，然后第二个参数security601318。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_110.png)

我觉得平安银行应该给我赞助费。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_112.png)

这做了他多少广告，给他股票打了多少广告，第三个。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_114.png)

他说个mount，比如说我们先来个100股，好这没有啥，然后这个时候我们来看一下什么呢，我们来看一下我的context，点positions。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_116.png)

Get the data，需要一个参数啊，对需要security参数，这要传进去，这是报的什么错啊。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_118.png)

key error哦，我知道了，你知道了吗，你不知道，我不知道为啥呢，因为600348没有，我这之前是不是跟这一样，这我用变成get了。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_120.png)

这没有变，有可能他没有对吧，还有之前还有这种信息吗，还有这种情况，我发布这。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_122.png)

这这也有对，所以我要把它都变了，都变成这个嗯，再点get一下。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_124.png)

你检查一下还有没有其他问题，好像没有了啊，可以运行一下再看看。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_126.png)

Get take no keyword，Argument。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_128.png)

内心错误，这什么情况，什么情况，龙在家想一想，security default等于零，直接写个零就行了，不用写default是吗，嗯嗯你确定吗，嗯对，其实我觉得都一样啊，那这我觉得这样对还是一样的呀。

应该没有什么，但是他哎那刚才是什么情况，不知道写错了吗，那不应该他们三个都一样的，为啥他报错别的不报错呢，嗯也可能这个是渠道玄学玄学玄学啊，好可以看到这个position是不是有100了。

嗯好我们再测一下别的，比如说我这想买125还是，你看不是100的，就一天是100对吧，比如说哎我这个地方想试下各种各样的问题，比如我想刚开始我们没有仓位者，我卖100嗯，看他看的提示啊。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_130.png)

你看你果然又出问题了，出问题说明我没有分析到这什么问题呢，又是这个问题啊，这这这这这是之前一样的问题，这个问题就是反的比较低级，好一条能为零零就没买没卖没卖呗，到最后这也没变对吧，这没有问题对吧。

还有什么，比如说来多买一点，咔咔咔咔咔，买这么多钱肯定不够，因为我就10万块钱，对不是100单位时候调整为3000啊，现金不足，先调整到3070，然后调整为3000，买了3000。

然后钱估计也没剩多少了，还是这些其他的呃啊。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_132.png)

比如说我们先先买完了之后，我们再卖一下，卖多少呢，比如说卖三果，你看调整为零。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_134.png)

最后也没有卖对，然后最后再打印一下，它打印一下零，卖完之后的池塘，好卖300，好卖了300克270对吧，卖3000，来3000哎就没了对吧，卖完之后就没了啊，这说明我们的这个东西。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_136.png)

这个代码还很比较正常啊，这是我们这个呃order函数。

![](img/f68668d8ff469e27e02aec9f61ce6ef6_138.png)

相当于是稍微底层一点的啊，那我们接下来会给它上面再封装四个，就是封装我们那四个order order target的那四个。



![](img/f68668d8ff469e27e02aec9f61ce6ef6_140.png)