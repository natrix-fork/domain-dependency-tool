# domain-dependency-tool
# 一个能画出域名与其它DNS域的依赖关系/拓扑图的工具
# A dependency graph/topology tool that can draw domain names with other DNS domains/zones
## 二进制(Binary)： [Windows, Linux, Darwin](https://github.com/mchtech/domain-dependency-tool/releases/tag/v1.1)
## 效果(Result)：
### github.com
![image](https://raw.githubusercontent.com/mchtech/domain-dependency-tool/master/sample.min.png)
![image](https://raw.githubusercontent.com/mchtech/domain-dependency-tool/master/sample.focus.min.png)
### 图缩放：滚轮(Zoom: use the wheel)：
![image](https://raw.githubusercontent.com/mchtech/domain-dependency-tool/master/sample.zoom.min.png)
## 用法(Usage)：
> dns-dependency-go [-t timeout] [-c retry_count] [-eip clientip] [-nv] [-root] 域名/domain_name_or_FQDN
## 参数(Parameters)：
>  -t 指定DNS解析超时时间(秒，默认为2秒) [Specify DNS resoving timeout (in second, default is 2 seconds)]

>  -c 指定DNS解析超时重试次数(默认为4) [Specify DNS resoving timeout retry times (default is 4)]

>  -eip 指定 EDNS-Client-Subnet 的 IPv4 或 IPv6 地址 [Specify the IPv4 or IPv6 address for EDNS-Client-Subnet]

>  -nv 不验证权威NS记录 [Do not verify authoritative NS records]

>  -root 解析根域名服务器记录 [Resolve the root-servers records]
## 例子(Examples)：

> dns-dependency-go github.com

> dns-dependency-go -t 2 -c 4 -eip 192.0.2.0 -root github.com

> dns-dependency-go -t 2 -c 4 -eip 2001:db8::1 -root github.com
## 依赖(Library Dependency)：
### echarts http://echarts.baidu.com/
