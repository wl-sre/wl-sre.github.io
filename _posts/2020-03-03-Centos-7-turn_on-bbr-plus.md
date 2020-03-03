# 关于bbr 
bbr算法为google的一个开源tcp网络加速算法，使用bbr可以显著提高网络连接速度以降降低延迟，对于国内连接海外服务器，是一个必备的程序。

linux内核必须要更新到4.9以上，脚本内含有更新内核的脚本选项。先更新内核再安装bbr plus加速。

一键代码
```
wget "https://github.com/chiakge/Linux-NetSpeed/raw/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
```

安装内核后重启系统，再安装bbr plus加速。开启后在/etc/sysctl.conf文件中可以看到有以下配置：
```
net.core.default_qdisc=fq
net.ipv4.tcp_congestion_control=bbrplus
```
