---
layout:     post
title:      小白教程：Github+私人域名搭建个人博客 
subtitle:   Another Guide 
date:       2018-10-04
author:     易渔 Candace Y.
header-img: 
catalog: true
tags:
    - Blog
    - 指南 guide
    
---


## 重要
请把本文和本文中提到的文章全部看完一遍或多遍后再动手操作。

## 前言
本人是个不懂代码、略懂英语的文科生。凭着浅薄的英语知识辨读了几个代码库，然后依据前人的模板捣鼓出了现在的博客：[易渔爱翻译](https://ifanyi.xyz/)。尤其请看一下这个[本站指南](https://ifanyi.xyz/2018/09/18/A-guide/)，里面有介绍了网站的一些功能和来历。如果你觉得这个博客还不错，请继续往下翻。

噢，如果之前没接触过Github的话，可以先看下这篇文章和里面的资源:
[资源汇总：如何使用Github](https://www.jianshu.com/p/4108c16d0099)

还有一点要说一下：我搭建博客的过程中完全没有用到github的桌面版，也没有安装ruby之类的（虽然调查过、研究过安装方法），因为我的电脑既老旧又低端，没法安装这些东东。也就是说，我全部都是在github的网页上操作的。这样就免去了学习ruby或git的代码语言这样的麻烦了，只是效率有点低，因为有服务器延时之类的问题。


## 步骤
#### 1.看教程，一步步操作。
[教程见这里提到的文章，全部看完后再操作](https://github.com/CandaceYcan/CandaceYcan.github.io/blob/master/README.md)。
教程里面也有提到自购域名然后解析，这些先不用管。没有自己的域名的话，就先用github的域名，这种域名的格式是[你的域名.github.io]，比如我的github域名是CandaceYcan.github.io，在没买自己的独立域名时，我就先用的这个打造网站的。等你买了独立域名，到时可以再绑定买到的域名，现在没有个人域名也不影响建站。

**教程一**：[利用 GitHub Pages 快速搭建个人博客 - 简书](https://www.jianshu.com/p/e68fba58f75c)
**教程二**：[Github+Jekyll 搭建个人网站详细教程 - Blog - Leach Chen](https://leach-chen.github.io/jekyll-github-blog/)

上面两个教程建成的网站风格截然不同，建议先把两个教程都看一遍，决定一下你喜欢哪个网站的风格（比如**文字为主、图片为主、搜索功能、文件夹分类、标签分类**等），然后再去github上fork相应的代码、一点点打造成自己需要的样子。

另外，上面的两个教程非常详细的介绍了用github建个人网站的步骤，但是，我们**不一定非要去fork它们的代码来建站**。其实，我建完自己的网站后，又发现了一些其他利用github建个人网站的例子，而且那些大神的代码库都可以看到，也有的大神愿意让别人用他的代码。所以，你**有探索精神的话，可以去瞅瞅别的网站和相应的代码，结合前人的经验，打造成具有自己风格的网站**。

####2.绑定自己的域名
看完各种教程，建出了自己的网站后，回望一下走过的直路或弯路，如果确定要在个人网站这条路上继续走下去，而且对独立域名很执著，那么可以**去买自己的域名了**。

至于在哪儿买，我最初关注的是阿里云，因为看前面的教程时发现有人买得挺便宜。问题是，在这里买后需要实名、得备案，否则没法用买的域名，感觉好麻烦啊。查找了解一番后，看到有人说**可以在国外的域名注册商那里买域名，这样就不用实名、备案之类的了**。很巧的是，看到多人推荐**[namesilo](namesilo.com)**，它支持**支付宝付款**，这点相当方便。也可以使用优惠码，凭优惠码可以省1美元（欢迎使用我在namesilo的优惠码 **ifanyi**，这个码的有效期至2020-12-31，用这个码你就可以省1美元，如果你的订单符合namesilo的一些条件，比如是新注册、新用户的新域名之类的，我似乎也会得一点好处~）。

###### namesilo下单页面和优惠码的使用方法见下图：
![namesilo.jpg](https://upload-images.jianshu.io/upload_images/1343920-bc5e4c022f2e7bac.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

关于namesilo的拓展阅读：
[Namesilo常见问题大全 - 简书](https://www.jianshu.com/p/a145c2681d7a)
[英文建站必备：Namesilo 购买注册流程 - weed8 - 博客园](https://www.cnblogs.com/weed8/p/7207582.html)


#### 3.解析域名。
这一步就是把你买的域名和你用github建的网站绑定起来。成功完成这一步后，就能通过你自己的域名来访问第一二步创建的域名为username.github.io的个人网站了。 

##### 我的域名解析/绑定方法：
我是在namesilo买的域名，所以对于在别家买域名的同学，下面的方法不太适用。

1.登录你的Github账户，找到你的名称为username.github.io的这个库，在里面找到CNAME文件（没有的这个文件话就创建一个，基本上前面提到的教程的代码库里都会有这个文件），在里面输入你买的个人域名，注意不带http或者www哦，你买的时候是什么就烈军属什么，比如你买的是aaaab.abc，那么这个文件里就输入aaaab.abc，不加http或www。

2. 在**namesilo**中，点击[Manage My Domains](https://www.namesilo.com/account_domains.php)，找到你要用的域名，在右侧找蓝色小球的图标，鼠标放在上面会提示“**Manage DNS for this domain**”，点击它，在出现的页面找**DNS Templates**（如下图），下面有很多主流空间的解析模板，找到Github，点击后面的Apply Template，会弹出一个窗口，告诉你DNS的变动，点确定(Add)。
![DNS.jpg](https://upload-images.jianshu.io/upload_images/1343920-92243c1e2ab1ca9e.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

3.页面跳转后，会在新页面看到一个表格，里面的第二列有四个A，一个CNAME。在CNAME这一行的末尾，点击那个铅笔图标，就是Edit那一列的，然后会出现新页面，把里面的Address / Value换成你在前面步骤上创建的Github域名，即username.github.io，比如我自己的是candaceycan.github.io。如下图：
![CNAME.jpg](https://upload-images.jianshu.io/upload_images/1343920-5e39bf68b17445f0.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

完成上面的操作后，无论你在浏览器的地址栏输入username.github.io，还是你新买的域名aaaab.abc，访问的都是你根据前面教程创建的网站。

在解析域名这一步，不少帖子推荐[DNSPod](https://www.dnspod.cn/)，也有人说使用**[namesilo](namesilo.com)**默认的解析方法的话会比较慢，毕竟它是国外的，可是我把个人域名配置到github就是用的namesilo自带的github解析模板（就是前面提到template的地方），而且我都是在网页操作的，并没有等几小时哦，每次操作顶多等几分钟，**很快就能用自己的域名访问个人网站了**。

另外，看解析域名的帖子，有人不少人提到设置@值，我因为用了模板，并没有输入@，我也不知道怎么回事，**反正现在能用自己的域名访问个人网站了**。

也有人强调A值（见图CNAME.jpg）有两个就够了，但是我用模板后，系统自动生出了四个，我不懂怎么改，也不敢擅自改，就这样了，**反正现在能用自己的域名访问个人网站了**。

好了，看完教程，一步步操作后，你就有自己的网站了。


###### 其他参考：
[github怎么绑定自己的域名？ - 知乎](https://www.zhihu.com/question/31377141/answer/103056861)
[教大家注册自己的域名并使用-为了自己的包名！ - 简书](https://www.jianshu.com/p/5dbad365dc71)



### 如果觉得本文对你有任何帮助，欢迎到我的[Github](https://github.com/CandaceYcan/CandaceYcan.github.io)给我的项目点一个star～谢谢


本文首发于[简书](https://www.jianshu.com/p/5487d39a1cb2)
