# dns-dependency-go
# 画出一个域名与其它DNS域的依赖关系图 
# Draw the dependency/relationship of a domain name with other DNS domains/zones
## 二进制(Binary)： [Windows, Linux, Darwin](https://gitee.com/mchtech/dns-dependency-go/attach_files)
## 效果(Result)：
### weibo.com
![image](https://gitee.com/mchtech/dns-dependency-go/raw/master/sample.min.png)
### www.amazon.com
![image](https://gitee.com/mchtech/dns-dependency-go/raw/master/complexsample.min.png)
## 用法(Usage)：
> dns-dependency-go [-t] [-c] [-eip] [-nv] [-root] 域名/domain name or FQDN
## 参数(Parameters)：
>  -t 指定DNS解析超时时间(秒，默认为2秒) [Specify DNS resoving timeout (in second, default is 2 seconds)]

>  -c 指定DNS解析超时重试次数(默认为4) [Specify DNS resoving timeout retry times (default is 4)]

>  -eip 指定 EDNS-Client-Subnet 的 IPv4 或 IPv6 地址 [Specify the IPv4 or IPv6 address for EDNS-Client-Subnet]

>  -nv 不验证权威记录 [do not verify authoritative records]

>  -root 解析根域名服务器记录 [Resoving the root-servers records]
## 例子(Examples)：

> dns-dependency-go weibo.com

> dns-dependency-go -t 2 -c 4 -eip 219.141.140.10 -root weibo.com

> dns-dependency-go -t 2 -c 4 -eip 2001:db8::1 -root weibo.com
## 依赖(Library Dependency)：
### echarts http://echarts.baidu.com/