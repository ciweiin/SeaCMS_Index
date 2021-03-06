# 安全常识
```
一些新人站长，经常会遇到网站被黑，网站被挂马等一些列安全问题。

下面从一些基本安全常识的角度来说下怎么来做安全防御：

【一】更新海洋CMS到最新版本

海洋CMS更新比较频繁，安全漏洞一经发现，会迅速发布修复补丁，所以保证使用新版程序是第一原则。

另外注意一点，海洋CMS升级必须逐个版本进行升级，不可以跨版本升级。

【二】保护海洋CMS后台目录不被泄露

海洋CMS后台功能比较多，操作权限也比较高，想要保证网站安全，必须保证后台不被黑客知道。一旦后台地址泄露，会引发很多安全问题。

* 使用复杂的后台目录名称，并且定期修改后台目录名称。

* 使用安全软件保护后台，如云锁的后台地址保护功能。

【三】隐藏真实的服务器IP地址

服务器安全也是比较重要的一个环节。如果服务器被攻破，那么放在服务器上网站也就没有安全可言了。

常见的服务器操作系统windows和linux都会不定期爆出安全漏洞。另外服务器上安装的软件和服务器环境搭建用到的PHP，Mysql，Nginx，IIS，apache等软件也会经常出现安全漏洞。如果服务器真实ip暴露出来，那么服务器被黑的可能性是极大的。

* 可以通过使用CDN来保护服务器的真实IP地址，推荐免费的Cloudflare就可以。

* 即使你使用CDN隐藏了真实IP，邮件发送服务（SMTP）也可能会泄露你的服务器真实IP地址。如果一定需要发送邮件，可以使用第三方发信服务，如 Sendcloud。 如果不需要发送邮件，可以在海洋CMS后台关闭该功能。

* 如果无法隐藏服务器真实IP，建议安装服务器安全软件，并做好服务器安全设置。服务器上安装的软件环境也需要及时更新到最新版。

【四】服务器端口安全

（1）做为网站服务器，使用的端口是比较少，可以保留常用端口后，关闭其他无用端口。网站http端口：80，https端口:443。

（2）关闭或修改远程桌面端口。如果不需要远程桌面功能，建议关闭。比如安装BT面包后就基本不再需要远程桌面功能。

（3）关闭或修改FTP端口。如果不需要FTP，可以关闭FTP服务。如果需要开启FTP，建议修改默认端口号，以及使用复杂的FTP密码。

（4）修改可以修改的端口，如Bt面板的。

（5）使用安全软件防御端口扫描。

（6）禁止局域网访问。

【五】安装必要的服务器安全软件

常用的安全软件如：护卫神，云锁，安全狗，悬镜等。可以很大程度提高服务器的安全性。另外需要注意的是，安全软件并不是安装上就万事大吉了，还需要做对应的设置。以云锁为例，就需要自己开启web防护功能，并设置其中的网站漏洞保护和网站后台保护。每个安全软件的具体设置可以参考百度或者软件官方教程，如利用云锁的关键词过滤功能来禁止提交script等关键词等，这里不再赘述。

windows系统建议：安全狗 护卫神 云锁 D盾

linux系统建议：悬镜 云锁

【六】禁止上传有风险的文件
对于网站而言，需要上传的文件一般为图片文件和压缩文件，对应的常用格式为：jpg/bmp/png/jpeg/gif/zip/rar。而php，asp，exe，bat这类文件则是高风险文件，需要禁止上传。禁止上传的方法也很多，比如使用安全软件拦截，使用伪静态规则屏蔽等，具体可以百度搜索帮助文档，这样不再赘述。

【七】已被入侵后需彻底清楚木马后门

如果服务器或者网站已经被入侵，需要彻底删除后门木马文件和恶意代码。否则黑客留下后门文件，任何安全措施都是无效的。如果条件允许做到如下：①格式化所有硬盘。②重新安装服务器操作系统。③备份数据库。④备份模板和图片文件，并检查文件里是否包含后门木马。一般情况下，templets目录里只有图片/js/css/html文件，uploads目录里应该只有图片文件，如出现php/asp/jsp等可执行文件，均为非法文件。

【八】不要使用root账户连接MySQL数据库

因为root用户权限较大，容易造成安全隐患。比如只有root用户可以通过MySQL的outfile来上传后门文件。

【九】定期备份数据

不把鸡蛋放在同一个篮子里，备份数据是最后一道屏障。

【十】云锁的设置提示

很多人不懂怎么设置安全软件，这里以云锁为例大概说下。

注意：如果你的云锁功能不全，找不到一些模块，说明linux内核版本不兼容或安装有问题，去云锁官网看帮助解决。

```