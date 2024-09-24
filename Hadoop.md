# 1. 安装虚拟机
略
# 2. 安装CentOS7
略

（有需要请在pyq留言或私聊踹我，默认大家都已安装。）

---
# 2.5 配置虚拟机硬件
> 如果使用默认设置，进行某些操作时候可能较为卡顿，建议修改。

1. 打开设置（快捷键`Ctrl+D`）
![alt text](/Picture/打开设置.png)

2. 内存建议2GB起步
![alt text](/Picture/内存大小.png)

3. 处理器建议2\*2或2\*4
![alt text](/Picture/处理器规格.png)

# 3. 配置网络
1. 打开虚拟机的桥接模式(默认应该为NAT模式)
![alt text](/Picture/桥接模式.png)

2. 打开网络设置
![alt text](/Picture/打开网络设置.png)
![alt text](/Picture/打开网络设置1.png)

3. 确定宿主机网络配置
   1. 按`Ctrl+Alt`回到主机，按`Win+R`打开运行，输入`cmd`**打开命令提示符**，输入`ipconfig /all`并回车查看网络配置
   2. 连了**WIFI**或者**手机热点**的请找到“**无线局域网适配器 WLAN**”;插了**网线**或者USB共享的请找到“**以太网适配器**”
![alt text](/Picture/主机网络配置.png)
   1. 注意**IPv4地址**、**子关掩码**、**默认网关**、**DNS服务器**

4. 修改网络配置
回到虚拟机，如果子关掩码为255.255.255.0，则**地址**填写为主机ip地址+1（例：<mark>192.168.205.</mark>93→<mark>192.168.205.</mark>94，高亮部分不变），其他内容与主机相同。
![alt text](/Picture/修改网络设置.png)

5. 配置slave节点
![alt text](image-1.png) 

# 4. 安装MySQL

Hadoop@123

start-dfs.sh
start-yarn.sh