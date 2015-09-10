# FreeNetBox
这个项目的目标是实现一个基于树莓派使用运营商网络的免流量WIFI路由器.
## 实现
1. 树莓派用蓝牙链接手机拨号上网
RespberryPi -- Bluetooth DUN -- Modem (手机也可以) -- cmwap/cmnet
2. 客户端通过wifi连接树莓派上proxy免流量上网
1. 客户端连接树莓派 wifi，树莓碰用iptable限制端口连接, 只可以为socks proxy的端口
2. 客户端修改全局代理为树莓派上的socks proxy
3. 树莓派上搭建 socks over http proxy 并连接 http proxy
4. 树莓派上搭建 http proxy， 通过http proxy 修改请求头欺骗流量计费系统
3. 成功
## Todolist
