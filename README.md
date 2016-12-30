# shadowsocks四合一自用修改版

#仅对默认配置进行了适当修改。

1,包括加密方式改为：chacha20

2,设置默认时区设置为：东八区-上海

3,修改shadowsocksR的协议修改为auth_sha1_v4_compatible 兼容原版shadowsocks

4,修改shadowsocksR的混淆方式为http_simple_compatible  兼容原版shadowsocks

#本脚本适用环境

系统支持：CentOS 6+，Debian 7+，Ubuntu 12+

内存要求：≥128M

日期　　：2016 年 12 月 04 日

#关于本脚本

1、一键安装 Shadowsocks-Python， ShadowsocksR， Shadowsocks-Go， Shadowsocks-libev 版（四选一）服务端；

2、各版本的启动脚本及配置文件名不再重合；

3、每次运行可安装一种版本；

4、支持以多次运行来安装多个版本，且各个版本可以共存（注意端口号需设成不同）；

5、若已安装多个版本，则卸载时也需多次运行（每次卸载一种）；

6、Shadowsocks-Python 和 ShadowsocksR 安装后不可同时启动（因为本质上都属 Python 版）。

请按照对应的版本安装

#默认配置

服务器端口：自己设定（如不设定，默认为 8989）

密码：自己设定（如不设定，默认为 gatoslu.xyz）

备注：脚本默认创建单用户配置文件，如需配置多用户，请手动修改相应的配置文件后重启即可。

客户端下载

常规版 Windows 客户端

https://github.com/shadowsocks/shadowsocks-windows/releases

ShadowsocksR 版 Windows 客户端

https://github.com/breakwa11/shadowsocks-csharp/releases


#使用方法

使用root用户登录，运行以下命令：

wget --no-check-certificate https://raw.githubusercontent.com/gatoslu/onestick-shadowsocks/master/shadowsocks-all.sh

chmod +x shadowsocks-all.sh

./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log

#安装完成后，脚本提示如下

Congratulations, your_shadowsocks_version install completed!

Your Server IP        :your_server_ip

Your Server Port      :your_server_port

Your Password         :your_password

Your Encryption Method:chacha20

Welcome to visit:https://teddysun.com/486.html

Enjoy it!

#卸载方法

若已安装多个版本，则卸载时也需多次运行（每次卸载一种）

使用root用户登录，运行以下命令：

./shadowsocks-all.sh uninstall

#启动脚本

#启动脚本后面的参数含义，从左至右依次为：启动，停止，重启，查看状态。

Shadowsocks-Python 版：/etc/init.d/shadowsocks-python start | stop | restart | status

ShadowsocksR 版      ：/etc/init.d/shadowsocks-r start | stop | restart | status

Shadowsocks-Go 版    ：/etc/init.d/shadowsocks-go start | stop | restart | status

Shadowsocks-libev 版 ：/etc/init.d/shadowsocks-libev start | stop | restart | status

#各版本默认配置文件

Shadowsocks-Python 版：/etc/shadowsocks-python/config.json

ShadowsocksR 版      ：/etc/shadowsocks-r/config.json

Shadowsocks-Go 版    ：/etc/shadowsocks-go/config.json

Shadowsocks-libev 版 ：/etc/shadowsocks-libev/config.json

#更多单版本 Shadowsocks 服务端一键安装脚本

ShadowsocksR 版一键安装脚本（CentOS，Debian，Ubuntu）

CentOS 下 Shadowsocks-libev 一键安装脚本

Debian 下 Shadowsocks-libev 一键安装脚本

Shadowsocks-go 一键安装脚本（CentOS，Debian，Ubuntu）

#注意：以上单版本不可与该四合一版本混用。

#原创作者为秋水逸冰大神 https://teddysun.com/486.html



