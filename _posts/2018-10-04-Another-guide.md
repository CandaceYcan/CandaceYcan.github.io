---
layout:     post
title:      小白教程：Github+私人域名搭建个人博客 
subtitle:   Another Guide to This Blog
date:       2018-10-04
author:     易渔/Candace Y.
header-img: 
catalog: true
tags:
    - Blog
    - 指南/guide
    
---

##重要
请把本文和本文中提到的文章全部看完一遍后再动手操作。

##前言
本人是个不懂代码、略懂英语的文科生。凭着浅薄的英语知识辨读了几个代码库，然后依据前人的模板捣鼓出了现在的博客：[易渔爱翻译](https://ifanyi.xyz/)。尤其请看一下这个[本站指南](https://ifanyi.xyz/2018/09/18/A-guide/)，里面有介绍了网站的一些功能和来历。如果你觉得这个博客还不错，请继续往下翻。

噢，还有一点要说一下：我搭建博客的过程中完全没有用到github的桌面版，也没有安装ruby之类的（虽然调查过、研究过安装方法），因为我的电脑既老旧又低端，没法安装这些东东。也就是说，我全部都是在github的网页上操作的。这样就免去了学习ruby或git的代码语言这样的麻烦了，只是效率有点低，因为有服务器延时之类的问题。


##整体步骤概括一下就是：
1.在github.com上注册，然后创建一个新的repository。**~完成注册后~~，~~登录进去~~，~~找到~~create~ ~new~ ~repository~~，~~点击~~，~~然后根据提示来就行了~~。~**

2.看教程，一步步操作。[教程见这里提到的文章，全部看完后再操作](https://github.com/CandaceYcan/CandaceYcan.github.io/blob/master/README.md)。~教程里面也有提到自购域名然后解析，这些先不用管。没有自己的域名的话，就先用github的域名，这种域名的格式是[你的域名.github.io]，比如我的github域名是CandaceYcan.github.io，在没买自己的独立域名时，我就先用的这个打造网站的。~

3.看完各种教程，建出了自己的网站后，回望一下走过的直路或弯路，如果确定要在个人网站这条路上继续走下去，而且对独立域名很执著，那么可以**去买自己的域名了**。至于在哪儿买，我最初关注的是阿里云，因为看前面的教程时发现有人买得挺便宜。问题是，在这里买得实名、得备案，感觉好麻烦啊。查找了解了一番后发现，可以在国外的域名注册商那里买域名，这样就不用实名、备案之类的了。很巧的是，看到有人推荐**[namesilo](namesilo.com)**，它支持支付宝支付，这点相当方便。也有人分享注册流程和优惠码，凭优惠码可以省1美元。

4.解析域名。成功完成这一步后，就能通过你自己的域名来访问第一二步创建的域名为username.github.io的个人网站了。 

#####我的解析方法：
1.在Github上的名称为username.github.io的这个库中找到CNAME文件（没有的话就创建一个），在里面输入你买的个人域名，注意不带http或者www哦，你买的时候是什么就是什么，比如你买的是aaaab.abc，那么这个文件里就输入aaaab.abc，不加http或www。

2. 在**namesilo**中，点击[Manage My Domains](https://www.namesilo.com/account_domains.php)，找到你要用的域名，在右侧找蓝色小球的图标，鼠标放在上面会提示“**Manage DNS for this domain**”，点击它，在出现的页面找**DNS Templates**（如下图），下面有很多主流空间的解析模板，找到Github，点击后面的Apply Template，会弹出一个窗口，告诉你DNS的变动，点确定(Add)。
![DNS.jpg](https://upload-images.jianshu.io/upload_images/1343920-92243c1e2ab1ca9e.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

3.页面跳转后，会在新页面看到一个表格，里面的第二列有四个A，一个CNAME。在CNAME这一行的末尾，点击那个铅笔图标，就是Edit那一列的，然后会出现新页面，把里面的Address / Value换成你在前面步骤上创建的Github域名，即username.github.io，比如我自己的是candaceycan.github.io。如下图：
![CNAME.jpg](https://upload-images.jianshu.io/upload_images/1343920-5e39bf68b17445f0.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

完成上面的操作后，无论你在浏览器的地址栏输入username.github.io，还是你新买的域名aaaab.abc，访问的都是你根据前面教程创建的网站。

在解析域名这一步，不少帖子推荐[DNSPod](https://www.dnspod.cn/)，也有人说使用**[namesilo](namesilo.com)**默认的解析方法的话会比较慢，毕竟它是国外的，可是我把个人域名配置到github就是用的namesilo自带的github解析模板（就是前面提到template的地方），而且我都是在网页操作的，并没有等几小时哦，每次操作顶多等几分钟，**很快就能用自己的域名访问个人网站了**。

另外，看解析域名的帖子，有人不少人提到设置@值，我因为用了模板，并没有输入@，我也不知道怎么回事，**反正现在能用自己的域名访问个人网站了**。

也有人强调A值（见图CNAME.jpg）有两个就够了，但是我用模板后，系统自动生出了四个，我不懂怎么改，也不敢擅自改，就这样了，**反正现在能用自己的域名访问个人网站了**。

哈哈哈，说了太多**反正**。

（可惜的是，配置新域名后，网站上显示的访问量似乎会清零，作为码盲，我还不知道怎么解决这个问题~）

######其他参考：
[Namesilo常见问题大全 - 简书](https://www.jianshu.com/p/a145c2681d7a)
[英文建站必备：Namesilo 购买注册流程 - weed8 - 博客园](https://www.cnblogs.com/weed8/p/7207582.html)
[NameSilo域名购买与购买优惠券 - flyzy2005的博客 - CSDN博客](https://blog.csdn.net/wf632856695/article/details/79433206)
[github怎么绑定自己的域名？ - 知乎](https://www.zhihu.com/question/31377141/answer/103056861)
[教大家注册自己的域名并使用-为了自己的包名！ - 简书](https://www.jianshu.com/p/5dbad365dc71)


### 如果觉得本文对你有任何帮助，欢迎到我的[Github](https://github.com/CandaceYcan/CandaceYcan.github.io)给我的项目点一个star～谢谢

本文首发于[简书](https://www.jianshu.com/p/5487d39a1cb2)
