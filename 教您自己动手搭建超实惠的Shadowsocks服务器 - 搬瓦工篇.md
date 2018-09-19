# 教您自己动手搭建超实惠的Shadowsocks服务器 - 搬瓦工篇

【不满意包退 】包教会 本图文教程详细介绍了如何搭建Shadowsocks服务器,简单到不需要任何电脑基础就可以轻松学会。

自己搭建Shadowsocks服务器有如下优势：

优势1: 独享一台Shadowsocks服务器，不与其他用户共享资源, 个人安全和隐私都有保障。

优势2: 配备CN2专线，默认自带BBR加速算法，Youtube 1080p无压力。

优势3: 支持一键换IP地址，不用担心被封。

优势4: 比直接买SS账号B格略高 🙂

费用: 最低每月16元，本站还提供9.3折优惠码:BWH26FXH3HIQ

## 一、注册搬瓦工账号

1.点击[搬瓦工首页地址](https://bwh1.net/aff.php?aff=36779)，点击右上角注册按钮。

![图片](/bandwagon/WechatIMG20.jpeg)

2.填写注册信息（注意：国家请务必选择China，不要乱选择，这样可以避免以后被暂停服务。除了注册邮箱剩下的不需要填写真实信息，毕竟翻墙有一些匿名性比较好），然后输入验证码(如果有碰到的话),最后选中最下面的小方框(I have read and agree the Terms of service), 点击Register按钮完成注册。

![图片](/bandwagon/WechatIMG21.jpeg)

![图片](/bandwagon/WechatIMG21a.jpg)

3.登录进入搬瓦工
![图片](/bandwagon/WechatIMG22.jpeg)

## 二、购买服务器

1.点击Services->Order New Service
![图片](/bandwagon/WechatIMG23.jpeg)

2.选择合适的套餐

强烈推荐选择第一个或者第二个套餐，这两个套餐对比如下。

|套餐名称|地理位置|是否是CN2线路|硬盘大小|内存大小|每月流量|价格|
-------| -------|------|------|------|------|------|
SPECIAL 10G KVM PROMO V3 – LOS ANGELES – CN2|LOS ANGELES|是|10GB|512MB|500GB|29.99美元/年|
SPECIAL 20G KVM PROMO V3 – LOS ANGELES – CN2|LOS ANGELES|是|20GB|1024MB|1024GB|49.99美元/年，29.99美元/半年|

注：CN2代表到中国大陆有专线连接，网速会比较快并且有保障。

3.点击对应套餐后面Order Now按钮
![图片](/bandwagon/WechatIMG24.jpeg)

4.直接点击Add To Cart按钮。
![图片](/bandwagon/WechatIMG25.jpeg)

5.在promotional code处输入优惠码：BWH26FXH3HIQ，点击Validate Code，然后点击Checkout，进入结账页面。
![图片](/bandwagon/WechatIMG26.jpeg)

6.确认好信息后，选择支付宝付款(Alipay)，勾选同意协议的选项，点击Complete Order，提交订单。
![图片](/bandwagon/WechatIMG28.jpeg)

7.点击Pay Now，进行支付。
![图片](/bandwagon/WechatIMG29.jpeg)

8.使用支付宝完成付款。完成付款后，稍等几分钟，然后回到搬瓦工主页，点击Services->My Services，查看已经购买的服务器。
![图片](/bandwagon/WechatIMG30.jpeg)

## 三、安装Shadowsocks服务端软件

1.在My Services页面点击KiwiVM Control Panel按钮，进入服务器控制面板。
![图片](/bandwagon/WechatIMG32.jpeg)

2.进入控制面板首页，记录下服务器IP地址，最后连接会使用该服务器IP。
![图片](/bandwagon/WechatIMG33.jpeg)

3.点击Shadowsocks Server选项, 注意：如果面板左边kiwivm extras那里没有显示Shadowsocks选项，先用账号登陆搬瓦工网站以后，再在同一个浏览器中打开下面的链接 https://kiwivm.64clouds.com/main-exec.php?mode=extras_shadowsocks   然后点击下面的 Install Shad0ws0cks Server 按钮继续.
![图片](/bandwagon/WechatIMG34.jpeg)

4.点击Install Shadowsocks Server，等待几分钟，完成安装。
![图片](/bandwagon/WechatIMG35.jpeg)

5.待安装完成后，在会显示Shadowsocks账号信息：加密方式、端口和密码，加上前面获取的服务器IP地址，就可以在客户端登录了。
![图片](/bandwagon/WechatIMG36.jpeg)

6.最后参考下面的Shadowsocks(简称SS)各个客户端的免费下载配置教程,就可以呼吸到自由的互联网空气了.
有碰到问题的网友可以在底下留言，我会尽全力帮助大家，让墙内的网友都能呼吸到自由的互联网空气

### 希望想搭建的朋友可以通过我的教程搭建起来， 恳请大家一起帮忙转发穿墙技术教程让更多人看到外面的世界，星星之火可以燎原。

所有客户端的下载配置教程:
https://vultr.aicnm.com/Windows%E3%80%81Mac%E3%80%81%E5%AE%89%E5%8D%93%E5%92%8CiOS%E4%B8%8B%E8%BD%BDss%E5%AE%A2%E6%88%B7%E7%AB%AF%E5%8F%8A%E9%85%8D%E7%BD%AE%E6%96%B9%E6%B3%95/   连接成功后，可以去Youtube测试网速。1080p毫无压力。


![图片](/bandwagon/WechatIMG37.jpeg)


## Q&A
### 没有看到Shadowsocks Server选项怎么办？
答：一般情况是由于套餐选择或者数据中心选择跟教程不一样导致的。解决方案也非常简单，点击控制面板里面的Root shell - advanced，然后把下面这段脚本复制粘贴进去，然后点击Execute执行即可。
执行成功后会显示Shadowsocks安装成功的提示和账号信息，就可以直接使用了。
```
yum --enablerepo=epel -y install python-pip
pip install shadowsocks
echo '443' > /root/.my-shadowsocks-port
openssl rand -base64 16 > /root/.my-shadowsocks-password
echo 'aes-256-cfb' > /root/.my-shadowsocks-encryption

/usr/bin/ssserver -s ::0 -p `cat /root/.my-shadowsocks-port` -k `cat /root/.my-shadowsocks-password` -m `cat /root/.my-shadowsocks-encryption` --user nobody --workers 2 -d start
printf "\n/usr/bin/ssserver -s ::0 -p \`cat /root/.my-shadowsocks-port\` -k \`cat /root/.my-shadowsocks-password\` -m \`cat /root/.my-shadowsocks-encryption\` --user nobody --workers 2 -d start\n\n" >> /etc/rc.d/rc.local

MY_IP=$(curl http://myip.dnsomatic.com)
printf "*****************************************\nShadowsocks服务器已经安装成功，账号如下：\n服务器：$MY_IP \n端口：`cat /root/.my-shadowsocks-port` \n密码：`cat /root/.my-shadowsocks-password` \n加密方式：`cat /root/.my-shadowsocks-encryption` \n*****************************************\n"

```
执行成功后会看到如下的账号信息，就可以直接使用了。
![图片](/bandwagon/WechatIMG280.jpeg)

### 执行完上述代码，仍然没有Shadowsocks Server选项怎么办？
答：不需要Shadowsocks Server选项了，直接下载Shadowsocks，并使用上面显示的账号信息就可以连接了。
