> 此文推荐手持 Windows PC 的 PHP 新手阅读：即是那些想学习 PHP 的新同学。因为在学习 PHP 之前，你需要一个环境来运行 PHP。

### 版本说明

1. Windows 10
2. Wampserver 3.0.6 (期望安装的软件版本：Apache 2.4.33, PHP 7.1.16, MySQL 5.7.21)
3. Composer 1.6.4

## 安装 WampServer

WampServer 是一个集成环境，它就包含了 Apache（服务器软件），PHP 和 MySQL （数据库），所以我们安装 WampServer 的话，即可获取这三个关键的，
运行 PHP 环境所需要的软件。

来到 WampServer 官网：http://www.wampserver.com/en/ 点击下载按钮：

<img width="778" alt="codecasts_2018-04-13_19-07-09" src="https://user-images.githubusercontent.com/6011686/38780007-24068d60-4103-11e8-89aa-ed91fed0865b.png">

然后选择自己系统位数对应的版本下载即可：

<img width="822" alt="codecasts_2018-04-13_19-09-23" src="https://user-images.githubusercontent.com/6011686/38780026-4d5205a0-4103-11e8-836f-48147e5b3580.png">

下载完成之后，跟安装其他的 Windows 软件过程没有太大的差别（我下面用一些列截图说明这个安装的每一步）


<img width="223" alt="codecasts_2018-04-14_22-36-05" src="https://user-images.githubusercontent.com/6011686/38780049-a4e89e8c-4103-11e8-9ee7-24687fac58ca.png">
<img width="374" alt="codecasts_2018-04-14_22-36-32" src="https://user-images.githubusercontent.com/6011686/38780050-a5280b30-4103-11e8-8335-0fd829e9a9d2.png">
<img width="374" alt="codecasts_2018-04-14_22-36-52" src="https://user-images.githubusercontent.com/6011686/38780051-a569d3d0-4103-11e8-98a9-be361e4a4889.png">
<img width="374" alt="codecasts_2018-04-14_22-37-04" src="https://user-images.githubusercontent.com/6011686/38780052-a5a92576-4103-11e8-82fb-1933fe2b021d.png">
<img width="374" alt="codecasts_2018-04-14_22-37-21" src="https://user-images.githubusercontent.com/6011686/38780053-a5e797c0-4103-11e8-9cf4-fc240af9b1c1.png">
<img width="374" alt="codecasts_2018-04-14_22-37-35" src="https://user-images.githubusercontent.com/6011686/38780054-a62589c2-4103-11e8-8d27-6415753ce79a.png">
<img width="374" alt="codecasts_2018-04-14_22-40-00" src="https://user-images.githubusercontent.com/6011686/38780055-a669d8b6-4103-11e8-84bd-ce29f4ba693e.png">
<img width="374" alt="codecasts_2018-04-14_22-40-43" src="https://user-images.githubusercontent.com/6011686/38780056-a6a9b5da-4103-11e8-85ba-d84311e98ccf.png">
<img width="461" alt="codecasts_2018-04-14_22-41-45" src="https://user-images.githubusercontent.com/6011686/38780057-a6f14b0c-4103-11e8-8ab2-62bdf92d1d75.png">
<img width="374" alt="codecasts_2018-04-14_22-42-09" src="https://user-images.githubusercontent.com/6011686/38780322-5730d5c0-4107-11e8-82d9-7f3e733ec762.png">
<img width="374" alt="codecasts_2018-04-14_22-42-20" src="https://user-images.githubusercontent.com/6011686/38780323-578e74dc-4107-11e8-84d6-618d53edd30d.png">

安装过程中会询问你是否使用 IE 作为默认浏览器，是否使用 Notepad++ 作为默认编辑器。这两个选项你不确定的话，直接选择`否`就可以。

安装完成之后，双击桌面的 WampServer 图标即可启动 WampServer，待 WampServer 图标变成绿色即表明 WampServer 启动成功。

<img width="258" alt="codecasts_2018-04-14_23-04-20" src="https://user-images.githubusercontent.com/6011686/38780331-67fe608e-4107-11e8-8865-5e5081aa68b3.png">

启动成功之后，在浏览器（推荐 Chrome，或者你使用其他浏览器也 OK）地址栏访问 http://localhost ，可以看到类似下面的界面：

<img width="783" alt="codecasts_2018-04-14_23-08-03" src="https://user-images.githubusercontent.com/6011686/38780403-300a9cfa-4108-11e8-8a7a-026d1ce277a1.png">

启动成功后，我个人推荐首先修改 PHP 的版本，因为默认的是 PHP 5.6 的大版本，为了更好的性能和更多的新特性，我们可以将 WampServer 的 PHP 版本升级为
PHP 7.1 的大版本。

<img width="388" alt="codecasts_2018-04-14_23-06-42" src="https://user-images.githubusercontent.com/6011686/38780374-ddfd624e-4107-11e8-9ef1-06cfba17cdc7.png">

升级到 PHP 7.1 之后，浏览器访问 http://localhost?phpinfo=1 ，可以看到类似下面的页面，即表示 PHP 升级成功。

<img width="766" alt="codecasts_2018-04-14_23-07-22" src="https://user-images.githubusercontent.com/6011686/38780420-5fea9c0e-4108-11e8-98f0-27b450a88943.png">

至此，WampServer 已经成功安装了，即我们已经拥有执行 PHP 代码的完整环境。但是

> 我们自己写的 PHP 代码（自己创建的 `.php` 文件）如何执行呢？如何像其他网站那样使用 PHP 跑起一个浏览器也可以访问的站点呢？


在这里，使用 WampServer 作为 PHP 开发环境的情况下，需要记住一个非常非常重要的目录：`www` 目录。你可以直接从 WampServer 打开这个目录：

<img width="206" alt="codecasts_2018-04-14_23-31-47" src="https://user-images.githubusercontent.com/6011686/38780487-de220bf6-4109-11e8-874e-4e72aeefb1c3.png">

点开图片中的 `www directory` 即可，正常情况下，打开的目录是：`C:\wamp\www` 类似的目录。作为新手学习 PHP 的时候，可以将自己写的 PHP 代码放到这个目录下，然后从浏览器访问对应的 `.php` 文件即可看到解析的 PHP 内容。比如你在 `C:\wamp\www` 目录下创建了一个自己写的 `my.php` 文件，你就可以通过访问 http://localhost/my.php 来看到 `my.php` 的 PHP 代码解析后的具体内容。

这样，通过浏览器看到 PHP 代码执行效果就完整实现了。

那么，问题来了：如何在命令行中执行 PHP 代码或者 PHP 命令呢？

这个问题的答案是：在 Windows 上，我们需要设置环境变量。

具体的设置过程如下（演示系统为 Windows 10）：

<img width="282" alt="codecasts_2018-04-14_23-38-06" src="https://user-images.githubusercontent.com/6011686/38780581-a29082b4-410b-11e8-8640-2d554275af31.png">

在 Windows 10 底部的搜索栏输入 `sy` ，然后打开 `系统[控制面板]` 。

<img width="590" alt="codecasts_2018-04-14_23-38-24" src="https://user-images.githubusercontent.com/6011686/38780589-b5880734-410b-11e8-96fc-5294e020d8e6.png">

点击左侧的 `高级系统设置`。

<img width="374" alt="codecasts_2018-04-14_23-39-01" src="https://user-images.githubusercontent.com/6011686/38780614-1e7e8a4c-410c-11e8-8186-fb90817ca007.png">

然后，点击下方的 `环境变量(N)`。

<img width="485" alt="codecasts_2018-04-14_23-39-53" src="https://user-images.githubusercontent.com/6011686/38780602-d5728dc6-410b-11e8-9ff1-9d47b98af6de.png">

选择 `Path` 那一行，点击 `编辑` ：

<img width="414" alt="codecasts_2018-04-14_23-48-00" src="https://user-images.githubusercontent.com/6011686/38780636-77b1dfce-410c-11e8-811f-e995fe36d5eb.png">

点击右上 `新建` 按钮，在需要输入的地方输入类似图片中的内容：`C:\wamp\bin\php\php7.1.16` 。这里的 `php7.1.16` 目录需要对应你使用的 php 版本，比如你使用的是 PHP 5.6.38，这里会对应成 `php5.6.38` 。这些 PHP 版本的对应都可以在 `C:\wamp\bin\php` 目录下看得到的。 最后 `确定` 保存。

> 往回退的界面也注意要点击 `确定` 保存。

在完成以上的环境变量设置之后，既可打开命令行工具

<img width="263" alt="codecasts_2018-04-14_23-48-30" src="https://user-images.githubusercontent.com/6011686/38780720-a6bb7b3a-410d-11e8-94b4-39b8430441fe.png">

在底部搜索栏输入 `cmd` ，然后 Enter 即可打开命令行工具。

<img width="734" alt="codecasts_2018-04-14_23-48-51" src="https://user-images.githubusercontent.com/6011686/38780722-a7950350-410d-11e8-84c5-ec0dafe525a5.png">

在命令行输入 `php -v`，能看到类似上图的结果，即表明 PHP 的环境变量设置成功。













