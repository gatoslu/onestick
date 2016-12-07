# onestick  shadowsocks四合一安装版，仅对默认配置进行了适当修改
#原创作者秋水逸冰大神 https://teddysun.com/486.html
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
#shadowsocks一键安装脚本
#请按照对应的版本安装

#默认配置
服务器端口：自己设定（如不设定，默认为 8989）
密码：自己设定（如不设定，默认为 teddysun.com）
备注：脚本默认创建单用户配置文件，如需配置多用户，请手动修改相应的配置文件后重启即可。

客户端下载
常规版 Windows 客户端
https://github.com/shadowsocks/shadowsocks-windows/releases

ShadowsocksR 版 Windows 客户端
https://github.com/breakwa11/shadowsocks-csharp/releases


#使用方法
使用root用户登录，运行以下命令：

wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log

安装完成后，脚本提示如下
Congratulations, your_shadowsocks_version install completed!
Your Server IP        :your_server_ip
Your Server Port      :your_server_port
Your Password         :your_password
Your Encryption Method:aes-256-cfb

Welcome to visit:https://teddysun.com/486.html
Enjoy it!
