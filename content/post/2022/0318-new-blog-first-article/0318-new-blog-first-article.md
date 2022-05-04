---
title: "Hugo|新博客搭建小记"
description: 
date: 2022-05-04T16:24:59+08:00
image: 
categories: [" 2022"," 姓名粗记可以休"]
tag: [" Hugo"]
math: 
license: 
hidden: false
comments: true
draft: false
typora-root-url: ..\..\..\static
---



## ~~废话~~引言 ##



1999年12月31日——世纪之交，平时不爱凑热闹的父母换上新装，特意带我去南京路“下馆子”。一路上，人群摩肩接踵，兴奋地期盼着千禧年的到来，日子越来越好似乎是顺理成章的。两年之后，中国加入了WTO，我们有幸见证了口味不断增多的膨化食品、晚上六点半的柯南与小神龙俱乐部、大学后门包罗万象盗版碟甚至是登录谷歌和YouTube，  直到……二十年后的今天。

为了解决搭建博客的问题，作为技术小白发现了大量无私分享的博客和GitHub这样的平台，一切仿佛回到了2000年初的互联网的良好氛围……

博主是一个“三分钟热度”的人，对有兴趣的事物往往会尝试一下，然后半途而废。自从加入Mastodon，发现了不少嘟友的精美博客，“自己也搭一个”的念头马上浮了出来，加之想要持续写点东西的想法可能已经有十来个年头了，然而却不曾动笔。两个念头一拍即合，热气羊肉出锅了！

怎么建博客作为新博客首文也顺理成章，虽是命题作文，却拖了足足一个月之久。既是小白，搭建过程自然大为不易，也衍生出一些感想，一一记录之，希望给同好一些帮助，也希望这次不再是“三分钟热度”。



## 2022年，还需要一个个人博客吗？



在《哈利·波特》中有一个场景，在夜色的帷幕下，无数的新生拿着火把，登上小船，化作点点“火光”航向霍格沃茨。我想写作仍是最好的输出手段之一，个人博客就如同这一叶叶扁舟，托起我们的精神，也为后来人照亮方向。

- **写得越多，想得越深！**

码字过程中，行文拖沓、用词不切、语句不通的情况比比皆是。对文字的驾驭需要时间的积淀，十年不写的我提起笔就变成文字大师显然是天方夜谭，但另一层面，思考得太浅也是无处落笔的原因之一。

写文章前我列了个大纲，想着按照搭建顺序逐一记录，复制代码，应该没什么难度。实际上每写一小段，我都要反复删减大量的文字，停笔思考的时间也很长，和梦想中的一气呵成的状态相去甚远。大纲只是一个简单的框架，文章具体的内容，重点的安排，语言的组织，这些细节的完善需要得是思考的深度。思考得越深入，意味着对内容理解越全面与深刻，产出的时候也越游刃有余，水到渠成。“吾尝终日而思矣，不如须臾之所学也……”，作为一个日常多想的人，这篇指南的成文过程对我触动很大，如何让思考不只是浮于表面，通过博客输出无疑一个很好的方法。

- **自我审查与记录真实。**

众所周知，在简中互联网发布任何文字都要经过严密的审查，这种审查不仅指向作品本身，长期的审查会影响乃至改变作者的语言习惯，避讳与“404”某种程度上已经改变了中文互联网的语言生态，一些正常的词语，如：翠、龟、胸等都无法通过审查，晋江这几年的“囗囗文学”亦可以很好的说明这一问题。受影响的不仅是网文，从端传媒的[《全面審查時代：中國媒體人正在經歷什麼？》](https://theinitium.com/article/20180910-mainland-censorship-journalist-in-china/)一文中，可以看到审查逐渐造成中国媒体劣化的过程。对于个人而言，独立博客是避免审查影响的有效方式。

另一方面，有一种说法是，这几年只需记录社会事实就能成书出版了。想想上海从2022年3月底开始到现在的封城，期间无数的魔幻、呼救与互助，我们在记录历史，这种记录也注定会变成历史的一部分。

- **技术？技术！**

Hugo架构的搭建让我摸了摸技术的“外衣”，大量傻瓜教程让搭建网站变成了近似“复制粘贴，下一步”的过程。某种意义上也是技术的下放，每个人都能为之所用，拓展一片新的天地。当初我觉得初音未来的是非常伟大的造物，让许多这辈子也许不会和音乐有交集的阿宅发现了自己作曲的天赋，创作出了大量的佳作，走向了不一样的人生。博客、Mastodon、VPS甚至播客等等，其实也是给我们一个发掘更多自我可能的机会，为什么不试一试呢！

- **交个朋友……**

其实说建个博客能找到大量朋友可能过了，但无疑通过博客建立的友情往往是舒适可人的。说可人有点怪（笑。毕竟能相互找到对方，会互相看博客的已经属于是同温层。另一方面互相交换友链，浏览不同博客也是扩展自己信息面，拓展交友圈的行为，一定程度上避免了被算法裹挟，信息茧房的产生。



## 搭建方式



目前搭建博客方式多样，而且教学贴齐全，总有一款适合你。主流的博客类型有：静态博客、Wordpress托管、博客网站、Notion等，作为技术小白，其实也研究了很久，简单说说自己理解下各自特点：



### 静态博客



所谓静态博客，笔者的理解是作者事先安排好的内容（静态文件），通过一定的框架（如Hugo，Hexo等）转为可见页面，通过托管网站发布到互联网上，所见（页面内容）即所得（静态文件）。

**优点**

1. 访问速度快。
2. 建站费用低。如果不考虑购买域名的话，只需依靠免费服务就能获得非常不错的效果。
3. 备份，转移方便。静态博客的内容均存储在本地，使得博客的备份，资料的管理变得相对简单。
4. 多数静态博客均支持Markdown解析。

**缺点**

1. 需要一定的编程知识*。实际上目前静态博客的建站已经非常傻瓜，本博客就是“复制粘贴，下一步”的产物。但日常的发布，修改网站等操作扔需要使用到代码。
2. 网页互动与交互较少。静态博客插件数量较少，特别注意的是，需要自己搭建才能实现评论功能（一样有傻瓜教程）。
3. 在线编写与便携性较差。写作的发布和网站的管理需要在同一台电脑上进行，当然也有方式可以在线写作发布（但是我还没研究），所以便携性不是很够。

**常见框架**

[Hugo](https://gohugo.io/)：Go语言编写，特点是快，易扩展，易部署。本博客即采用Hugo搭建而成。

[Hexo](https://hexo.io/zh-tw/)：老牌静态博客框架，主题多样而且视觉效果酷炫。

[Jekyll](https://jekyllrb.com/)：似乎是GitHub亲儿子。



### 动态博客



动态博客，一个运行在服务器上的博客程序，一般提供一个在线的编辑器供使用者在线编写，因为有服务器后台，所以可以直接上传文章，交互性相比静态博客也好很多。

**优点**

1. 无需代码知识。在线直接编写，也有大量Markdown插件可以选择
2. 插件类型数量多样。~~有钱可以升级更多可能~~

**缺点**

1. 由于有后台数据库，访问速度相对较慢
2. 托管平台一般需要费用。~~没错，动态博客有钱的话就能为所欲为~~
3. 插件升级更新较多，可能需要常常关心一下~~（是否续费）~~。

**常见框架**

[WordPress](https://wordpress.org/)：老牌的动态博客框架，插件多，功能全，一般提到动态博客就是他了！

[Halo](https://halo.run/)：最近经常见到的名字，特点似乎是易于上手。

[Typecho](http://typecho.org/)：比较简洁，专注于写作。



### 博客平台



开袋即食不要钱，唯一的缺点可能是少了一些“个人”的感觉，但是博客重要的是内容，不是吗？但是国内的在线平台都难逃审查的影响，所以将境外写作平台当作个人博客的话，需要考虑科学上网和受众。

**常见平台**

[Blogger](https://www.blogger.com/about/?bpli=1)

[Matters](https://matters.news/)

[写意Writee](https://writee.org/)

WordPress本身应该也有一个在线写作平台



### Notion



[Notion](https://www.notion.so/3d4ea90227e84d3d94d6f6e06e5ef872) 是一款提供笔记、任务、数据库、看板、维基、日历和提醒等组件的应用程序。如果你本身有用Notion管理日常的话，其实Notion主页当作个人博客也是非常好的选择，简单速食。

**优点**

1. 免费。
2. 全平台在线，方便省心。

**缺点**

1. 没有RSS订阅功能。解决方法可以参考椒老师的文章[《How to setup RSS for notion blog using Zapier》](https://blog.douchi.space/rss-for-notion-zapier/)。
2. Notion有数据安全的隐患，仁者见仁了。
3. 未来有可能被墙。



实际上正如段首所言，目前搭建博客方式多样，只需挑选适合自己的即可。而且作为一个个人博客，最重要的是文字输出，如果让博客搭建和不断地调整样式变成了主心骨，那搭建个人博客的意义也就本末倒置了。所以选择一个方案，然后写作输出吧！

更多的选择可参考此方老师的文章[《【新手向】你究竟需要什么样的博客方案》](https://blog.konata.co/?p=148)。



## 参考文章



搭建过程中主要参考了以下文章，大大们保姆式的教学令人感到快乐。

1. 主要建站流程：[《Hugo | 一起动手搭建个人博客吧》](https://mantyke.icu/2021/hugo-build-blog/)
2. 主题换皮：[《Hugo | Hugo-stack-theme 主题魔改版》](https://mantyke.icu/2022/stack-theme-mod/)
3. 评论区搭建：[《从Disqus迁移到Waline》](https://candinya.com/posts/migrate-from-disqus-to-waline/#%E8%BF%81%E7%A7%BB%E8%AE%B0%E5%BD%95)

注：个人独立建站的话应该从1开始按步骤操作，但是如果满意塔塔魔改皮肤的话（即本站皮肤），可以注册完工具网站后直接从2开始，弯道超车。



## 搭建过程



本站搭建基于Windows10操作系统下，且部分网站流量需要自备科学上网工具。



### 事前准备



1. [Hugo](https://github.com/gohugoio/hugo/releases/tag/v0.89.0)，Hugo是前文所提及的静态网页框架，通过Hugo我们可以将我们的markdown文件转为HTML网页，最终通过托管服务器展示出来。进入页面后，下拉网页，在Asset中找到[hugo_extended_0.89.0_Windows-64bit.zip](https://github.com/gohugoio/hugo/releases/download/v0.89.0/hugo_extended_0.89.0_Windows-64bit.zip)，下载解压到你所希望的位置，如E盘的Hugo文件夹下，即`E:\Hugo`。
2. [Git](https://git-scm.com/)，Git是一个免费开源的分布式版本控制系统。我们通过Git命令在本地文件夹创建新的静态文件，通过也需要通过Git将我们的静态文件从本地推送至托管服务器。下载后直接安装即可。
3. [Github Desktop](https://desktop.github.com/)，Github的桌面客户端，我们发布本地修改到托管服务器需要一次次输入Git命令，但是Github Desktop可以帮助我们简化这个流程，以后只需要启动客户端，点击发布即可。
4. [VScode](https://code.visualstudio.com/)，知名的代码编辑器。下载后点击左侧边栏的`Extensions`，在搜索框中搜索`Chinese Language Pack for Visual Studio Code` 和`Markdown All in One`插件并安装。前者为界面汉化，后者则是 Markdown 编辑插件，可以帮助你更好的查看Hugo框架的代码，进行网站的修改。
5. [Github](https://github.com/) ，注册一个Github账号，Github 负责储存我们整个的博客文件，同时GitHub的账号可以一键注册登录其他工具网站。
6. [Vercel](https://vercel.com/new)，是一个网站托管平台，直接用关联Github的账号登录。Vercel可以帮助我们自动搭建、部署静态网站。而且支持自动配置https，不用自己去FreeSSL申请证书，更是省去了一大堆证书的配置，最重要的是这么多功能都是免费的！免费的！真神仙网站！



### 搭建过程（弯道超车版）



本人最初是基于塔塔君的[《Hugo | 一起动手搭建个人博客吧》](https://mantyke.icu/2021/hugo-build-blog/)逐步搭建的，但塔塔君后续放出了[《Hugo | Hugo-stack-theme 主题魔改版》](https://mantyke.icu/2022/stack-theme-mod/)一键换装版本，珠玉在前，在此直接引用塔塔博客的原文步骤。同时大部分Hugo主题在Github上均有发布，有兴趣的读者可以在[Hugo主题](https://themes.gohugo.io/)中寻找喜欢的主题用类似的方法设置博客。这里我们采用[Even](https://themes.gohugo.io/themes/hugo-theme-even/)主题进行尝试，步骤如下：



> Github 仓库地址：[Mantyke](https://github.com/Mantyke)/[stack-theme-mod](https://github.com/Mantyke/Hugo-stack-theme-mod)
>
> 本主题由 [CaiJimmy](https://github.com/CaiJimmy) 制作并[发布](https://github.com/CaiJimmy/hugo-theme-stack)，这个仓库是由 [Mantyke](https://mantyke.icu/) 修改的魔改版本
>
> 预览：[Demo 站](https://stack-theme-mod.vercel.app/)
>
> **使用方式**
>
> **从零建立博客**：Fork 仓库到自己账号下，用 Github 注册 Vercel，依次点击 Overview → New Project → import 刚刚 Fork 的仓库，设置`FRAMEWORK PRESET`为 Hugo → 点击`Environment Variables`，设置`NAME`为`HUGO_VERSION`，`Value`为`Hugo版本号（如0.89.0）` → 点击 Add → 点击 Deploy，稍等十来秒即可部署完成。下载仓库到本地后使用 Github Desktop 更新文章。



1. 注册完Github后，进入[Even主题的Github页面](https://github.com/olOwOlo/hugo-theme-even/blob/master/README-zh.md)，点击右上角Fork按钮，如下图确认后，Fork该仓库至自己账号下。



![Fork仓库](../static/images/0318-new-blog-first-article.assets/ApplicationFrameHost_hGRkE5akij.png)



2. 打开[Vercel](https://vercel.com/new)，用Github账号登录，然后依次点击Overview和New Project，可以看到刚刚Fork的Even主题已经在我们的仓库中，可以通过Vercel直接Import。



![Vercel部署](../static/images/0318-new-blog-first-article.assets/POWERPNT_fH6C6TzX9z.png)



3. 随后打开GitHub Desktop，选择左上角File-clone仓库-选择本地Hugo安装文件夹，之后就大功告成了。



![Github拉取仓库到本地](../static/images/0318-new-blog-first-article.assets/image-20220503235026027.png)



4. 随后就可以在Vercel点击域名查看网页了。

注：Even本身需要从要从[`exampleSite`](https://github.com/olOwOlo/hugo-theme-even/tree/master/exampleSite)文件夹中将`config.toml`文件拖到根目录下放才能正常运行，很多主题都会在Github有详细的步骤说明，先仔细阅读有助于搭建顺利展开。



### 评论区建设



由于静态博客没有自带评论区，所以需要自己搭建评论区框架和服务器，这里我们选用[Waline](https://waline.js.org/)作为我们的评论系统。Waline本身的[说明文档](https://waline.js.org/guide/get-started.html#leancloud-%E8%AE%BE%E7%BD%AE-%E6%95%B0%E6%8D%AE%E5%BA%93)写的非常清晰，跟着步骤走就能完成在Vercel中的部署。Waline默认使用LeanCloud数据库，当然你也可以选择其他数据库进行操作，笔者别出心裁的选择了MongoDB数据库（其实过程有点自讨苦吃，而且MongoDB的数据库免费容量更小），具体过程可以参考[《从Disqus迁移到Waline》](https://candinya.com/posts/migrate-from-disqus-to-waline/#%E8%BF%81%E7%A7%BB%E8%AE%B0%E5%BD%95)一文，值得注意的是，原文中 **创建数据库-4.（可选）创建专用账户**的过程，我虽然创建了专用账户，但是Vercel设置完环境变量后，似乎无法通过MongoDB的验证，正常读取数据库内容，最后只能作罢，直接使用主账户。不怕麻烦爱折腾的用户可以尝试寻找原因。

完成Waline部署后，我们只需改变Stack设置，技能将Waline评论挂上我们的网站。Stack主题本身就支持Waline，我们找到根目录下的`config.yaml`文件用VScode打开，找到如下代码。

```yaml
    comments:
        enabled: true
        provider: waline //此处填写waline
        
        //省略若干代码
        
        waline:
            serverURL: //此处填写Vercel服务器地址
```

按上文填写后，我们的个人博客就顺利下水了，如前文所言，个人博客最重要的是文字输出，如果能在其中享受”Debug“的快乐，那自是最好，反之技术对于博客来说，也是”粗记可休“足矣。希望大家都能享受畅所欲言的快乐！



## 书写与发布



搭建完博客后，书写和发布中遇到的一些困难与心得，在此记录。



### 书写文章



在Hugo根目录中右键点击`Git bash here`，输入下方内容并回车，

```
hugo new posts/文章名字.md
```

即可在对应文件夹中创造一个新md文件，用Markdown编辑器（推荐Tyopa，好用不贵！）即可打开编写。

这里笔者发现没法用代码在post下的文件夹新建md文件（如：`\content\post\2022\`），不知原因。在`post`和`posts`均可以新建md文件，现在采用的是先新建文件，然后再将文件搬到下属文件夹的笨办法。



### Markdown文件

- Front-matter

Front-matter 是文件最上方以 `---` 分隔的区域，用于指定个别文件的变量，举例如下：

```markdown
---
title: "Hugo|新博客搭建小记"
description: 
date: 2022-05-03T07:05:51+08:00
categories: [" 2022"," 姓名粗记可以休"]
tag: [" Hugo"] 
---
```

它规定了这篇文章的标题、描述、建立时间等，可以看到还有categories和tag也包含在此。自带模板的Front-matter不多，可以编辑`archetypes`文件夹下的`default.md`文件来设置默认的Front Matter模板。笔者觉得比较好用的有：

```
categories: //分类
tag: //标签 
hidden: //是否隐藏，隐藏和draft不同，隐藏只要有对应的url仍旧可以查看，但草稿则不行。
draft: //是否为草稿
```



- 图片

Markdown本身插入图片是以`![]()`的形式存在的，如何可以直接调用文章文件夹下的图片呈现在网页上，笔者本身尚未弄清。目前通过设置静态根目录的方法另辟了一个文件夹专门存储图片与调取，详见：[在Typora和Hugo中正确显示图片](https://www.jtr109.com/posts/manage-images-in-typora-and-hugo/)，但强迫症总觉得不舒服，塔塔原文件中似乎是直接调取文章文件夹目录下的图片，有待继续捣鼓。



## 后续修改



主体建设完后，后续做了一些其他修改，因年代久远不可考，记录一些主要的，实际上还未完工，后续就慢慢修补吧。装修贵在折腾，有兴趣者可以参考塔塔的三篇装修指南：

[Hugo | 看中 stack 主题的归档功能，搬家并做修改](https://mantyke.icu/2021/f9f0ec87/)

[Hugo | 另一篇 stack 主题装修记录](https://mantyke.icu/2021/a08f1963/)

[Hugo | 第三篇 Stack 主题装修记录，堂堂再临！](https://mantyke.icu/2022/stack-theme-furnish03/)



### 代码高亮

主要参考了Revi的[《调整代码风格为Nord》](https://www.norevi.icu/2021/hugo-%E8%B0%83%E6%95%B4%E4%BB%A3%E7%A0%81%E9%A3%8E%E6%A0%BC%E4%B8%BAnord/#%E4%BB%A3%E7%A0%81%E5%BC%95%E7%94%A8%E6%96%B9%E5%BC%8F)，但是实际操作发现了一个问题，那就是当开启行号后，行号无法正常展示，且出现长代码时不能有效换行。查找了Github发现也有类似的问题，[Highlight.js与Hugo不兼容](https://github.com/nanxiaobei/hugo-paper/issues/12)。目前没有找到行之有效的解决方案，读者也可直接采用Hugo自带的Chroma插件显示，可参考[《设置Hugo的代码高亮》](https://dp2px.com/2020/05/29/hugo-highlighting/)。想了想本身博客也不是技术博客，应该也不会出现大量的代码，干脆暂时关闭了行号，按下不表。



### 有待后续调查的疑问和工作

- **插入图片**

如何不用静态文件夹，直接使用文章文件夹下的图片，且可以被识别读取有待后续调查。

- **样式修改**

头像，网站图标、下划线效果、网站颜色等一些杂活有待后续慢慢修改。

个人介绍、友链需要改一下文字，现在还是使用说明书！

- **在线写作**

Hugo是否可以实现在线协作方案，有待搜索。理论上通过Github是一定可以实现的，但是已经感觉到技术的压力了。（在线后台，折腾静态博客是何苦？）

- **图片边框调整**

Hugo能否实现自动为图片添加边框和修改圆角，这个感觉还是一个很实用的功能，特别在白底的博客上。

- **VPS**

内心：搭建完了博客，不买个VPS搭建一个实例吗？脑袋：不，我感觉不行。



以上便是整个搭建过程和后续，中间其实也偷懒了省略了很多，不过算是有始有终的一个开始，至于能写到哪里，我想坚持才是最重要的，仅以此牌作为纪念与警示。（ 写完发现是五月四号，也是另一种纪念吧）



![](../static/images/0318-new-blog-first-article.assets/image-20220504162045114.png)



希望大家看的愉快！

















