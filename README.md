# net_speeder

https://github.com/snooda/net-speeder


net-speeder 可以在高延迟不稳定链路上优化单线程下载速度，运行时依赖的库：libnet、libpcap 。debian/ubuntu安装libnet：apt-get install libnet1 ；安装libpcap： apt-get install libpcap0.8 。编译需要安装libnet和libpcap对应的dev包，debian/ubuntu安装libnet-dev：apt-get install libnet1-dev ，安装libpcap-dev： apt-get install libpcap0.8-dev 。


CentOS用户执行以下命令：  
sh net_speeder_lazyinstall.sh  
装完后，会给出脚本用法，最简单的就是开启所有IP协议加速。参数：./net_speeder 网卡名 加速规则（bpf规则）。最简单用法： # ./net_speeder venet0 "ip" 加速所有ip协议数据。可执行以下命令：  
nohup /usr/local/net_speeder/net_speeder venet0 "ip" >/dev/null 2>&1 &  


Debian/Ubuntu用户执行以下命令：  
bash debian_netspeeder_tennfy.sh  
装完后  
nohup /root/net_speeder venet0 "ip" >/dev/null 2>&1 &  


查看net-speeder是否运行：  
ps aux|grep net_speeder|grep -v grep。  

停止net-speeder：  
killall net_speeder。  
