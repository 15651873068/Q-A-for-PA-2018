# Q&A for PA2018 NUAA
PA2018常见问题解答（持续更新，更新频率1-2天/次），欢迎star
------
# 读前必看

1.提问以前务必翻看翻看本问答文档，对于文档中已经给出的问题，不再回复，敬请谅解！！

2.有偿（`1分钱QQ红包`）征集你们遇到的问题的解决办法
想分享你遇到问题的解决办法？没问题，这个仓库里有一个叫【`what-you-want-to-say`】的分支，你可以把想说的话，想提醒大家的事情，还包括代码框架本身的bug等等提交到这个分支，遇到有人提交我会上去检查一下后合并的

3.注意这里不是给你共享答案的地方，后面每周检查报告的时候是有查重的，请你们珍惜自己的代码……因此遇到这种提交不予合并，技术性难题你们可以一起讨论

4.这个问答仓库的issue功能关掉了，以免有人使用不文明用语或发答案，有话想说请提交到`what-you-want-to-say`分支，作者每天会上去看有没有人提交

5.温馨提醒：每次你们提交的报告都会**查重**，请不要把自己的代码分享给别人，遇到雷同的估计可能会被**算没交**

6.新添加的问题将放在最前面，以免你们看不到以为没更新，想看历史比较久远的问题往后面看

## 最后更新日期：2018.3.1

# PA2(预更新，请不要惊慌失措)

* 2018.3.1更新:

1. 遇到问题:
```bash
make ARCH=x86-nemu ALL=dummy run
Building am [x86-nemu]
make[2] *** No targets specified and no makefile found
...
```
如果遇到，检查`~/.bashrc`目录，是否存在
```bash
export NEMU_HOME=/home/your name/ics2017/nemu
export AM_HOME=/home/your name/ics2017/nexus-am
export NAVY_HOME=/home/your name/ics2017/navy-apps
```
三个变量

# PA1

PA1的问答预计从`3月4日开始更新`，直接提问建议在`3月3日再开始问`，提前拉进度的同学遇到问题先只有自己解决下

* 2018.3.1更新：

3.有同学问怎么RTFSC，我的回答是从`main函数`开始，后面你就懂了。

2.验证自己的结构体（或联合体）是否写对了：运行项目，不出现`assert failure`就是写对了，其原理是生成几个随机数赋给寄存器，然后从里面再读出来，验证写的和读的是否一样，具体请RTFSC。

1.有同学问，我连寄存器的组织结构都不知道，怎么让我写结构体？问这个问题的同学**纯属不读讲义**，各通用寄存器的组织关系在讲义里写的非常清楚

# PA0

* 2018.3.1更新：

36.关于有同学到宿舍死活docker拉取不了镜像：给你一个寒假在家做就是为了拖到学校用学校的烂网做的吗？有同学说不啊我觉得宿舍网络比家里快，应该要好一些，还有这种想法的同学可以参见问答`第32条`。

35.关于git log记录，编译（`make`命令）几次就应该有几个`compile`的log项，执行（`make run`命令）几次就应该有几个`run`的log项，而自己commit的项（即作者为`user.name`里设置的）则是需要你使用`git commit --allowempty`命令提交的更改（查询时可使用`git log user='xxx'`，其中xxx是`user.name`）。

34.有虚拟机同学反映`standard system utilities`无法安装，跳过后没有sudo，这里给大家列出这个标准系统组件中含有的包（需要哪个安装哪个，比如`sudo`，`ifconfig`等等）：[http://bbs.chinaunix.net/thread-1924206-1-1.html](http://bbs.chinaunix.net/thread-1924206-1-1.html) 请看链接的五楼回答。另外这个方法不能保证后面和正常安装的同学一模一样不会出问题，到时候出了问题再解决就好了，所以平时注意保存你们的代码（推荐申请一个代码仓库来，现在国内的[码云](http://git.oschina.net/)蛮火的，而且免费建私有项目，不妨试试）

* 2018.2.28更新：

33.**能在手册上查到的东西尽量自己查手册**（如指令的操作和含义等啦，GDB/GCC的使用方法和那些参数的意义啦，docker的这些命令参数啦，Linux的指令和参数啦，某某库里有哪些函数啦），我这又不是机器人，你问我我也是去查手册，何必一定要搬运一次呢

32.与课程无关，科普一个概念：**网络环境好≠网速很快**。有人说宿舍网络快就是网络环境好，实则不然，网络环境的要素很多，如果有玩P2P（BitTorrent,Emule,Share,....）的同学应该知道一个High/Low ID的概念，实际上你们不更换源从国外下载，更是经过多少次的转发，一般来说ISP给家庭用户是能够达到给公网IP的开放程度的（有些为了节省IP采用NAT，都不是很影响），但是宿舍的网首先就和家庭网不太一样，架构不同，甚至被所谓“客户端”绑架，导致网络环境很差，跑测试都不是很好用，说这么多只想证明一点，在家不做的回学校做这个更难做

31.找不到SDL2/SDL.h的问题，参考链接：[http://blog.csdn.net/hank12580/article/details/45949995 ](http://blog.csdn.net/hank12580/article/details/45949995)

30.（还有几天就截止了还有人在装虚拟机，进度要加快了啊）安装完虚拟机后马上开机，可能又进入安装界面，因此请大家安装成功后关闭虚拟机，然后调整**开机的引导顺序，将硬盘调整至光驱之前**，再开机

29.请**一个一个字读讲义**，如果条件允许建议**一边朗读一边做**，以免有些人讲义上写的明明白白的黑底白字就是没看到，让人感到上帝为何要赐予你被蒙蔽着的双眼

28.你们都20左右不小了，应该知道做什么都没有一帆风顺的，遇到问题首先应该**学会自己解决**，把能查的（`官方文档/手册`、`搜索引擎`、`在线近期问题汇总`）都查了，解决不了的再说（当了二十年的**网虫**就是当**伸手党**的吗？）

* 2018.2.27更新：

27.如果遇到`gdb`出现问题：
```bash
warning: Error disabling address space randomization: Operation not permited
```
可能是由于 docker 默认开启了 ASLR(Address space layout randomization) 。
我的解决方法是重新配置容器，在`create`选项中加入`--privileged`参数即可。

26.`PA`是`组成原理课程设计`，是独立于组成原理课的单独的一门课，1个学分，挂了没有补考，按目前行情重修100元；组成原理实验0.5个学分，同样挂了没补考，重修50元，如果内容和去年相同的话那就是ICS Lab的前两个实验，这个具体后面老师会布置的，现在暂时不用管

25.关于有同学dockerfile中没把用户名密码替代成自己的问题：修改用户名用命令`sudo usermod –l 新名字 旧名字`，修改密码命令自己网上查一下吧很简单（关键词：【`Linux 修改密码`】），这个注意一下，为了确保检查报告的时候看你的图是不是自己做的而不是盗图，所以请务必把debian的用户名设成自己的真名拼音（不一定非要全名拼音，简写QQ啥的都可以，只要能认得出你就OK），这个将作为抄袭检查的依据之一（这个作为建议，只要能让人看出来是你自己做的就行，对于已经做完的，**就在报告末尾加一句，我改名啦就行了**，而且**造成这个问题的本来原因就是你们在生成容器的时候不仔细看讲义没有修改那个用户名参数**，无可非议）

24.补充之前说的建议装32位系统：64位也可以，只要能成功编译拉取到的那个项目就OK，不必拘泥于到底该装哪个。

23.tmux分屏功能个人觉得通过`多开putty或Xshell`替代效率更高，这条仅作为经验之谈，具体根据个人情况和喜好确定。

22.有同学问git log怎么检查，这里简单给个参考标准（**仅供参考**）：使用命令`git log --author="你在项目中设置的那个你自己的学号-姓名"`，将本次报告的进度部分中产生的手动commit的截图，然后那些make run和编译的记录有就可以，当然如果你申请了在线的代码托管，在网页上截图也可以

21.有同学反映VM按教程设置了网卡2为仅主机网络（Host-Only）后查eth1的状态出错，这个两方面可能性：一方面是你的Host-Only网卡名字不叫`eth1`，这种情况请使用`ifconfig -a`命令查看并确定哪个才是你的Host-Only网卡（一般IP分配为`10.x.x.x`的是NAT网卡，IP为`127.0.0.1`为环回网卡，不是这两个中其一的**另一个网卡**必然就是Host-Only网卡了）；另一方面可能是网卡找到了，但是没有IP，说明没启动，解决办法如下：使用命令`sudo vim /etc/network/interfaces`对网络设置文件进行修改 ，在文件末尾加入以下两行（**其中如果涉及到第一种情况，则eth1应替换为相应网卡名**）：
```
auto eth1            #自动启动eth1
iface eth1 inet dhcp #设置eth1从DHCP处获得IP
```
保存退出 ，输入命令`sudo /etc/init.d/networking restart`重启网络服务。然后最好再重启一次虚拟机确保设置成功更改。经试验发现**使用桥接模式**可实现单网卡既能上网又能让物理机连接到22端口，可以试试。

* 2018.2.26更新：

20.开学以后，你们还要兼顾很多课的进程，所以请大家**每周的PA进度一定要周中就开始做**了，留到周末做有两方面问题：一个是到后面量大了以后，`不是一两个通宵就能肝的完的`（这个光说无用，你们体会一次就知道了）；第二是集中到周末做，`问问题的人太密集太多，短时间内我也解答不过来`，等解答到你的问题的时候可能是几个小时以后了，耽误了你的进程我也很抱歉，但是没有办法；第三是`提交时间是严格截止`的，迟交了可能会被**惩♂罚**，注意一下吧

19.还没开始做的同学可以留意下，docker和vm没有绝对的哪个好哪个不好，一个是看个人习惯，一个是看自己的**OS环境能不能用docker**（只有`Windows10`**非家庭版**和`Linux当桌面`的大佬同学可以用docker）。至于用vm的同学，装机一定要装**32位（x86）的debian**，装64位理论上可做（我就是在64位CentOS上面跟着你们进度），但是需要自己安装的时候安装系列**32位的编译环境**等等（这个我自己亲自试过可行），后面可能会有未知的问题（因为我也没有在64位环境下试验过，反正去年的项目拿来是能编译能跑，今年由于代码体系不同了，谁知道会出什么问题呢），无法保证

18.报告的过程要有截图，不要等做完了突然想起来我一个图都没截，做的过程中就**一边做一边截图**，有些图可以补，但是有些就不是很好补，注意一下

* 2018.2.25更新：

17.还是发现有人不看这个问答就来问，能自助解决的问题还是请**先尝试一下问答文档里的解决方案**。

16.ping百度ping不通，可能会提示是域名解析错误，这个时候再去ping一个外网的IP地址（这里我提供我自己的服务器给大家拿去ping：IP地址为`115.159.190.100`（Linux/CentOS）和`106.14.118.136`（Windows Server）），ping IP也ping不通才是DNS解析的问题，这个搜索关键词：【`linux 域名无法解析`】

15.讲义以群文件中的【`NUAA ICS 2018.pdf`】为准，其余不管你在哪里看到的什么（包括某些人翻出来的网页版的讲义啦，哪怕是我这个问答文档也要辩证来看这些问题）都**仅供参考**

14.建议经常**备份一下虚拟机**（把整个虚拟机导出，VirtualBox和VMware都支持，这个网上查一下就明白了，很简单，就不附具体流程了，提供关键词：【`virtualbox 导出虚拟机`】【`vmware 导出虚拟机`】），docker的同学备份可能要麻烦些（因为我自己没具体操作过，这个网上也有，关键词：【`docker 导出容器`】），但是但是，最保险的是自己申请一个代码仓库（`GitHub`，`Coding`，`码云`都可以），把自己的代码push到代码仓库上面，这个的相关指导文章就数不胜数了，自己查百度即可

* 2018.2.24更新：

13.再提醒一遍，用docker做实验的同学搭SSH参考`2018讲义`，用VM的做实验的同学搭SSH参考`VM的SSH讲义`，注意`端口`不要搞混

12.关于有的同学安装了`debian的VM`，还在VM里面试图用ssh命令假装混成`GNU/Linux and Mac Users`，我只能用**请仔细理解讲义，并好好查阅这份问答文档**来回答你

11.关于SSH中你到底应该看For Windows还是For Linux/Mac Users呢？：你应该看哪个小节指的是你自己**物理机**里是啥系统，形象地说，大部分同学应该对应`For Windows Users`，**小部分平时就用Linux当桌面的大佬和用Mac OS的同学**，才参考`For GNU/Linux and Mac Users`

10.2018讲义（或VM的SSH讲义）中的ssh连接，形象地说，如果把Docker（或VM）中安装debian看作一台笔记本电脑，那么通过ssh连接（Windows下的putty/linux和mac自带的ssh功能），**就相当于给这台笔记本电脑接一个外接显示器**

9.安利部分：传文件可以用`FileZilla`提高效率，终端可以用`Xshell`替代putty（根据个人喜好）

* 2018.2.23更新：

8.重修同学，如果不想重新搭建docker环境，可以将就沿用去年的`虚拟机环境`（前提当然是你没删），但是请把去年的ics目录删掉（不删也罢，但是别搞错了哪个是哪个），2018和2017的PA用的代码框架不同（这个对比下讲义就显而易见了），因此去年不管做到哪挂的。。代码几乎没用了。。

* 2018.2.22更新：

7.开始做PA0以后**不要去瞎搞电脑**（包括重装系统，升级系统，装某某驱动，重装docker或者虚拟机什么的），这个搞坏了**只有从头做**，除非自己网上找代码仓库（比如`码云`，`github`，`coding`这些）存代码，这种情况也要重做PA0，所以这一个学期，电脑坏了只要还能将就用能做PA，就不要修电脑，期末结束了再修，否则影响了进度问题很严重

6.遇到docker好像开启了容器但是连不上，多半是上次用完没停止容器，然后挂起假死了，`stop一下，然后重启下电脑`，基本上都正常了

5.再再然后有时候遇到vim修改某某系统文件失败，麻烦用`sudo vim`来修改

4.拉取镜像慢和apt-get慢，以及拉取镜像1/11失败，apt-get失败等，解决办法都是挂VPN和换国内源（搜索关键字：【`docker 更换国内源`】【`debian 更换国内源`】【`apt-get 阿里源`】）
* docker的镜像加速（摘自菜鸟教程）：
鉴于国内网络问题，后续拉取 Docker 镜像十分缓慢，我们可以需要配置加速器来解决，我使用的是网易的镜像地址：http://hub-mirror.c.163.com。
新版的 Docker 使用 /etc/docker/daemon.json（Linux） 或者 %programdata%\docker\config\daemon.json（Windows） 来配置 Daemon。
请在该配置文件中加入（没有该文件的话，请先建一个）：
```json
{
  "registry-mirrors": ["http://hub-mirror.c.163.com"]
}
```

3.docker命令无法识别，不是网络问题，是docker安装的有问题，解决方法是`卸载重装`，并检查`hyper-v`等是否处于正常打开状态

2.关于vmware的host-only，给一个参考博文，[请点击这里](http://blog.csdn.net/u013121305/article/details/49505679)
搜索关键词：【`linux host-only vmware`】，另外经验证使用虚拟机网卡的`桥接模式`可以连通虚拟机的22端口，可以尝试。

1.近期90%以上的问题**来自手误**，麻烦出问题的同学自己仔细**逐个字符**检查一下敲的内容（`dockerfile`，修改`debian的update源`，敲`命令`等等）有没有打错的（前几天一个比较极端的例子是`debian`打成`debain`搞了半个小时，昨天还有一个把参数的-打成全角横杠，搞了一个小时）。
* 附常见手误：
```
debian和debain
docker build -t和docker built -d
半角字符和全角字符（多半是输入法造成的）
（持续更新中...）
```
