# 学完血赚！最强人工智能数据挖掘实战【Python金融量化分析】，非常适合新手！即练即会！！！ - P26：26-策略效果演示与指标分析 - 迪哥小助手 - BV1URsfeqEQ5

我们想法什么样？我们想法它是横着来是吧？就是横着去写每个股票名字啊，第一个股票，然后第二个股票，然后第三个股票，然后第四个股票我们一般怎么样？我们一般大家是不是都喜欢这样啊，就是竖着去写。哎。

我说第一个股票，然后它的一个财务的一个营收哎怎么怎么样？第二个股票营收怎么怎么样，第三个股票，第四个股票是不是咱把它稍微改一改。😊。



![](img/f27a335fe32a02fa7b36af76cbd9963c_1.png)

这个咱们来改一改呃，这块我说我在执行这个结果的时候，然后我说把最后的一个结果稍微的给它去变一下吧。呃，来把这个东西稍微改一改。对这个跟 frame做什么，其实只需要对它做一个转制是不是就可以了。然后呢。

咱们来看一下吧，就是打印一下它的一个转制的一个结果。先来试试啊这个结果对不对？然后对的话，咱再往下走。啊，转制一下转制完之后啊，其实这一步咱还没完。在befo trading的时候啊。

我们最终要的目的是什么？哎，不是说打印出来给你看一看吧，是把那什么那10个找到手吧。所以说这块就是呃我们最终想要得到的这一块我是再写一下吧。最终我说我们想要得到的结果。

应该是对它先做一个转制来看转制的结果。😊。

![](img/f27a335fe32a02fa7b36af76cbd9963c_3.png)

转借结果，你看就是竖着的，就是这个东西，就是一个股票名字。然后后面是它实际的一个指标吧。那第一个第一个就是一个index，一个缩引，后面就是一个实际的一个值是吧？行了。

那此时我们只需要把索引拿到手就行吧，你看有没有什么变化。呃，看起来就是对这间隔太短了，看不出来什么变化。行，咱不管了，一会儿策略个分析吧。在这里我说我把它的一个index拿到手。



![](img/f27a335fe32a02fa7b36af76cbd9963c_5.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_6.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_7.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_8.png)

呃，这个是我想要的一个股票名字，然后我把股票名字给它重新的设置一下。在这个contex context当中啊，我说呃把它当做是一会儿啊我要返回的一个结果，或者说你就把它存到我的一个contex当中。

这一块儿这个就是咱们要的这个就是会员三00当中选了一个10个啊，随便只要个名字得了。好了，这是我们现在哎这个打印咱一会儿也不需要了，打印堆东西没什么用。行了，这是我们的一个笔赋 trading饼。

我们在做交易之前，已经能够把这些个筛选工作给做完了吧。那接下来就是一个hand bar啊，这里就是呃我们要实际的做一些事情了，这里咱就不pass了，咱来写。😊。



![](img/f27a335fe32a02fa7b36af76cbd9963c_10.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_11.png)

啊，往下一点。

![](img/f27a335fe32a02fa7b36af76cbd9963c_13.png)

再往下一点吧，放中间里头好了，我们来写吧。第一步要干什么？首先我们要去做一个判断吧，判断什么当前啊哎呀我这个contest当中，或者说当前啊我是否是持有一些股票，这里给大家看这个API。



![](img/f27a335fe32a02fa7b36af76cbd9963c_15.png)

先看这个API，然后咱们再参考API去写啊。其实啊就是给大家准备的所有的这些例子都是一点点翻的API翻出来的。API当中可解释的东西其实蛮多的。找一找那个contest那东西，我找一下。



![](img/f27a335fe32a02fa7b36af76cbd9963c_17.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_18.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_19.png)

Contexス。啊，我不是在这里在这里。

![](img/f27a335fe32a02fa7b36af76cbd9963c_21.png)

在这个找一找它的一个cont。

![](img/f27a335fe32a02fa7b36af76cbd9963c_23.png)

这是行情股票，这是它的一些数据啊，没亚数据还是改那个里边改这里边我其实有这个contex来找一找。

![](img/f27a335fe32a02fa7b36af76cbd9963c_25.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_26.png)

交易相关的哎，咱们之前咱们一会儿也要去用啊。然后这呢cont4哎找到了这块，其实我们需要这个就是呃咱们的一些组合的信息了。我直接啊把这个复制过来，咱们来写啊这块就是我要看一下我当前我的一个账户当中啊。

我的一些信息的情况。然后这块有一个指标叫做一个position。咱们来看一看呃，这块。

![](img/f27a335fe32a02fa7b36af76cbd9963c_28.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_29.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_30.png)

啊，这块就是他有一个咱们点进去。

![](img/f27a335fe32a02fa7b36af76cbd9963c_32.png)

点开之后呢，它有一些属性啊，咱来看一看，我们一会用这个就是一个positionposition。你看啊它说的是一个呃包含所有仓位的字典，相当于就是这里边描述的是你现在手里有哪些个东西吧，你都买啥东西了。

是不是好了，那咱来写一下吧？首先第一步呃，把这个contexs找到手，我刚是不是复制了一下。😊。

![](img/f27a335fe32a02fa7b36af76cbd9963c_34.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_35.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_36.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_37.png)

康泰斯来这里。把它我说我先复制过来，先看看我手里有啥东西吧，这个关掉。好了，在这里我说我先去把做判断了。呃，我看我手里有什么东西，都手里东西的什么来着？position吧，是吧？

因为position当中描述的是呃你的一个所有仓位的一个字典，所以说咱把它先拿到手，那既然啊它是一个字典。😊。



![](img/f27a335fe32a02fa7b36af76cbd9963c_39.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_40.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_41.png)

那肯定是一个点kis当中存的是你所有的东西吧。那好了，我说我先做一个判断吧。如果说呀在你的字典当中啊，你这个所有买的东西，那都是空的那是不是说你现在手里啥也没有啊？好了，先做一个判断。

如果现在啊都是为空的时候。如果呢为空的时候我要干什么？那我说我现在哎是不是呃就不等于0，就是现在我是一个不为空的时候，不为空的时候，咱们是不是要去卖一些东西了啊？因为只有第一次的时候。

咱们是去把所就是买这么1只股票，然后后续啊就从第二天开始，咱们都是要去不断做判断吧。因为后续后续的时候就都不为空了。只要不为空的时候，我们就要去卖出一些东西吧。

咱要看一看我手里有的和现在哎这个股票池当中给我筛演出来的是不是一样吧。那好了，我说我现在要去便利一下了，便利我手里有这些东西。😊。



![](img/f27a335fe32a02fa7b36af76cbd9963c_43.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_44.png)

便利啊，我的一个所有咱手里有的那就是这个ki吧。这个ki当中保存的就是咱所有有的这些个就是买买买了这些股票是吧？好了，如果说。如果说呀当前这个股票，那没在咱当前指定的我的这个股票池当中股票池啊。

这里我看一下哎，这块呢咱是不是指定好一个名字了。好了，我说我做一个判断吧。如果说呀你没在我当前的这个股票池当中，呃，我看一下这个股票池当中，然后我就是给他要去卖掉吧，来看一看吧，卖怎么写。



![](img/f27a335fe32a02fa7b36af76cbd9963c_46.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_47.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_48.png)

API当中啊啊，这里它会给你有详细的一个介绍，在上面，这是交易相关的吧。交易相关的啊其实有挺多东西去做啊。咱有一个呃比较方便的，就是这个函数啊，order我们的一个present值。

相当于啊你贴个百分数就行了。点进去给大家看一看。

![](img/f27a335fe32a02fa7b36af76cbd9963c_50.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_51.png)

这里呢需要你主要啊就是传有两个参数。第一个参数啊就是卖谁。第二个参数就是呃你希望经过你交易完之后，然后它的一个就是占你现在的一个百分比。那比如这样，你说你现在经过了一个交易，境外交易之后，你要写个零。

什么意思，那写个零的意思，就是全卖吧。你看这边写了，就是投资组合占现在的一个总和啊，这是一个百分比。如果一呢那你就是把它买满零呢就是全卖了啊，这样一个意思。行吧，我把它有个东西直接复制过来吧。



![](img/f27a335fe32a02fa7b36af76cbd9963c_53.png)

复制过来，然后咱们要进行个交易了。然后它的一个ID就是我的一个股票。然后右边这个第二参数，咱们现在要干什么来着？是卖还是买啊？你不在我的交易池当中。哎，那我是不是不在我筛选的结果当中，你不咋地呀。

那我是不是就卖了，卖完之后你就空了，那是不是占零占0%就行了。这个是我的一个卖操作。好了，那其实啊不光我们得有卖操作，还得有什么，还得有买操作是吧？每天好了咱们这里在写啊在啊这块还是一个便利操作。😊。

复制过来吧。好了，遍利一下咱们的一个股票，在呃这块就不用这个了，编利什么，遍利我的股票池吧，然后把这个复制过来。😊，遍利，咱们现在筛选的这个池子。那接下来我是不是说要去买了，卖完了。

那是不是剩下的就该买了呀？好了，咱来看一下吧，怎样去买，还是这个函数啊，我直接的给它复制过来就行了。然后去买我当前股票，但是买多少呢？这个策略啊就是大家可以自己定，你可以根据它的一个咱们不是说了吗。

有财务数据，你可以跟它的一个财务数据，它的一个涨幅设置一个百分比，那是不是也行了，或者说咱们公咱们简单点吧，那就是平均啊平均一价得了，每一个都占到一个整体的一部分。然后我看一下contex当中。

然后咱们之前哦直接把这个复制过来行了，我的一个。😊。

![](img/f27a335fe32a02fa7b36af76cbd9963c_55.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_56.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_57.png)

3百。一共多少个？那咱们这一笔上整体啊一个浪值相当于什么？我做了一个平均买的一个操作吧。好了，咱们也不管买多少，就平均买就得了。下面这个给它删掉行了，然后最后我来检查一下啊，最后一个pass没问题。

行了，这个咱们基本大家检完了，然后先来运行一下吧，看一下它这一个结果啊，看没有什么问题。😊。

![](img/f27a335fe32a02fa7b36af76cbd9963c_59.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_60.png)

呃，看这个结果，一会儿咱们来给大家说一说啊，就是这个结果当中啊包含的哎这些个信息啊，它都是什么意思？

![](img/f27a335fe32a02fa7b36af76cbd9963c_62.png)

哎呦，看这都咋咋这么恐怖呢？直接我看到负的30%多。可能因为咱们这个时间的选择呀，稍微的呃可能这个东西就是跟时间是有关的啊，一会儿咱们来去换换时间，再来看结果。😊。



![](img/f27a335fe32a02fa7b36af76cbd9963c_64.png)

![](img/f27a335fe32a02fa7b36af76cbd9963c_65.png)

哎，行了，刚才吓死我了，刚才可能就是刚开始的时候可能比较赔吧，这个回测的年化收益比这个基准年化收益都要都怎么样，都看着更可怕，是不是？行，咱来看这个结果。那现在我说我设计了一个策略，先从整体来看吧。

这些指标是不是主要给大家说了啊，有些指标咱现在不用的，咱们等到时候后续咱们说策略用的时候给大家解释啊，就先看前色得了。😊，看指标，其实你就主要看什么你的一个回撤，就是我们设计的策略啊，它的一个效果。

以及呢你跟着这个指数走的时候啊，就啥也不玩的时候，它的一个效果看起来反正都是赔了，是不是？但是我们的策略能让你怎么样少赔一点吧？然后最大回撤区间占略有点占的还行吧，不是特别大，占了17点多啊。

这是咱们基本的一个指标。那下普率那肯定是一个负的。因为这都已经赔了，咱的单位风险肯定不值得，是不是？😊，好了，这是一个收益的一概况啊，咱们大概画出这样一个结果。然后呢，右边啊还有这样一个交易详情。

我对大家点进来，咱们简单的看一看。

![](img/f27a335fe32a02fa7b36af76cbd9963c_67.png)