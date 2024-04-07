## 已测试系统(x86_64):
-	Rocky 8
-	Rocky 9
-	CentOS 7
-	CentOS 8
-	CentOS Stream 8
-	CentOS Stream 9
-	AlmaLinux 8.2/8.4/8.8
-	AlmaLinux 9.0/9.3
-	OpenCloudOS 8.8(腾讯,类似centos8,软件包是oc8.x86_64)
-	AnolisOS 8.6/8.8(龙蜥,兼容centos8生态,软件包是an8.x86_64)
-	openEuler 20.03-LTS-SP3(华为,类似centos8,软件包是oe1.x86_64)
-	openEuler 22.03-LTS-SP1
-	Huawei Cloud EulerOS 2.0(华为,类似centos8,软件包是hce2.x86_64)
-	BigCloud Enterprise Linux 7.1/7.4/7.5/7.6/7.7/7.8(移动,类似centos7,软件包是el7.x86_64)
-	BigCloud Enterprise Linux 8.1/8.2/8.4/8.6(移动,类似centos8,软件包是el8.x86_64)
-	BigCloud Enterprise Linux 20.10/22.10(移动,类似centos8,软件包是oe1、oe2203.x86_64)
## 备注:
1.	[AlmaLinux 8]、[CentOS Stream 8]、[Rocky 8/9]、[AnolisOS 8]、[BCLinux 8]等系统yum没有ntp软件包
2.	[CentOS Stream 8]、[Rocky 9]等系统yum没有xinetd软件包
3.	[AnolisOS 8]、[HCEulerOS 2.0]、[BCLinux 7/8]等系统无法安装rabbtimq(官网的安装脚本无法识别此系统)
4.	[HCEulerOS 2.0]、[BCLinux 20.10/22.10]、[openEuler 20.03-LTS-SP3/22.03-LTS-SP1]等系统yum没有nmap-ncat(nc命令在nmap软件包)、epel-release这几个软件包
5.	[HCEulerOS 2.0]、[BCLinux 20.10/22.10]、[openEuler 20.03-LTS-SP3/22.03-LTS-SP1]等系统没有redhat-release文件
6.	[HCEulerOS 2.0]系统yum没有libvirt软件包
7.	[BCLinux 8]系统yum没有libvirt软件包、安装ovs编译报错
8.	[BCLinux 22.10]系统中filebeat启动有问题,和系统有关系
9.	dstat、glances这两个工具好多系统会提示安装失败,多执行几次"ywtool install",如果还失败则需要离线安装
10.	linux运维工具,只测试过x86_64,未测试过aarch64
11.	工具功能介绍:https://blog.csdn.net/ShunqiziranZ/article/details/135844875

## 未完成:
1.	安全基线
2.	将文本文件生成pdf文件脚本
3.	集成一些安全工具

## 2023.2.18之前
1. 增加了SMTP配置
2. 修改一些脚本文件

3. 增加了ssh配置

## 2023.1.28
1. 增加了vsftp配置

## 2023.2.18
1. 增加了日巡检、周巡检
2. 增加巡检报告定期压缩
3. log日志3天清理
4. 增加ssh禁止root使用密码登陆的功能
5. log日志名称修改

## 2023.2.20
1. 增加了备份工具
2. 增加了移除工具                  

## 2023.3.20
1. 增加了账号策略查看、修改等配置
2. 增加logo(在工具的安装脚本里)
3. 增加关闭功能
4. 增加堡垒机模式
5. 增加黑白名单访问控制

## 2023.4.4
1. 增加加固shell功能

## 2023.4.17
1. 增加堡垒机回放功能

## 2023.5.21
1. 增加安全基线功能

## 2023.6.17
1. 堡垒机增加运维本机资产
2. 调整堡垒机退出后进程依然存在问题

## 2023.7.15
1. 调整堡垒机查看回放功能
2. 调整centos8白名单功能
3. 调整防火墙加固功能
4. 调整加固shell-禁用vsftp、sftp、telnet

## 2023.7.21
1. 增加备份文件定期删除
2. 调整日志文件每天重置逻辑
3. 调整备份文件的路径
4. 调整移除工具步骤
5. 调整加固shell退出后进程依然存在问题
6. 调整日巡检登陆次数和防火墙默认区域配置文件

## 2023.7.26
1. 增加加固shell半个小时无内容输入自动断开连接
2. 修改blj运维方式

## 2023.11.8
1. 修改脚本显示内容的配色
2. 修改安全基线功能(脚本未完成)
3. 调整关闭shell功能后进程异常运行、账号没有执行删除的问题
4. 增加blj和shell密码MD5验证
5. 修改mail配置脚本
6. 修改install-yw.sh脚本

## 2023.11.29-2023.12.8
1. 增加blj本机IP运维(本机运维账号有问题)
2. 增加blj源IP记录
3. 增加blj回放昨日运维未结束记录
4. 增加周巡检、日巡检每个服务的配置文件最后修改时间
5. 修改周巡检:系统命令是否被篡改
6. 修改周巡检:登陆信息检查
7. 增加、修改select_check.sh脚本登录系统信息检查、用户信息检查、磁盘检查(vda)等
8. 修改install-yw.bin脚本创建log目录的方法
9. 修改install-low.sh脚本centos8、centos steam 8安装php、mysql、docker步骤
10. 修改check.sh脚本centos8检查mysql、docker服务的方法
11. 修改blj.sh、ssh_config.sh脚本探测端口连通性的配置

## 2023.12.13-2023.12.30
1. 修改vsftp配置脚本
2. 增加vsftp、shell、mail、ssh、dhcp开启服务后,输出都修改了哪些系统文件
3. 增加blj添加和删除运维IP
4. 修改install-yw.sh、install-low.sh
-	#install_ovs、install_rabbitmq、install_erlang.sh:安装前提前备份系统文件
-	#check.sh、check_copy.sh:服务检查的方式修改
-	#daily_check.sh、weekly_check.sh:启动时间因为系统中英文显示不准确、获取公网IP的方法、子网判断
5. 增加install-low.sh脚本centos8、centos steam 8、centos steam 9、rocky 9安装软件的方法
6. 增加install-low.sh脚本检查之前环境是否已安装软件
7. 增加install-low.sh脚本centos7可以选择安装mysql、php、jdk的版本
8. 增加disable_server.sh脚本卸载常用工具、常用软件、其他软件
9. 增加dhcp配置功能(地址池只支持单个)
10. 增加dhcp配置功能(增删改)
11. 增加daily_check.sh、weekly_check.sh脚本显示服务状态前先判断是否安装了该服务

## 2024.1.2-2024.1.14
1. 调整重置日志文件的配置(crond_optimization.sh)
2. 增加安装bridge-utils的步骤(install-low.sh)
3. 调整blj运维本机时不需要输入账号密码(备份文件:blj.sh.2024.1.2)
4. 增加"install-low.sh"脚本AlmaLinux 8.2/8.4/9.0安装软件的方法
5. 增加还原yum、netwrok_ip、network_br、network_bond、network_ovs的方法
6. 增加netwrok_ip、network_br、network_bond、network_ovs配置完后,输出都修改了哪些文件
7. 增加账号策略6个模块分别恢复的配置
8. 调整"account_security.sh"脚本原有账号密码有效期配置
9. 增加"install-yw.sh"脚本同步config.ini.old配置到config.ini中
10. 调整network_ip、network_br、network_bond、network_ovs脚本记录到config.ini文件中的格式
11. 堡垒机改名跳板机
12. 增加自定义清理日志天数
13. 调整"select_check.sh"脚本对内存检查、服务检查、系统信息检查、网络检查等配置
14. 增加blj批量添加、批量删除主机IP
15. 增加blj添加主机的另一种方法
16. 增加blj添加本机IP时需要输入root密码验证
17. 调整"bak_rm.sh"脚本备份功能的配置
18. 增加centos9/rocky9 mail邮件配置功能
19. 增加centos8、centos stream8/9、rocky8/9、AlmaLinux 8.2/8.4/9.0"账户策略"的"设置控制台登陆失败策略"、"设置SSH登陆失败策略"功能
20. 增加加固shell在关闭"telnet-server、vsftpd、sftp"前判断服务是否启动,服务是否通过"ywtool jiagu shell"方式关闭
21. 增加加固shell对telnet命令的判断
22. 调整每个脚本输入日志的格式

## 2024.1.15-2024.2.4
1. 增加登录防护脚本:检测3分钟15次登录系统失败,并拉黑IP
2. 增加"resources_check.sh"脚本中系统重启/关机操作检查
3. 调整"jiagu_shell_crond.sh"脚本中每天0点0分重置日志的步骤
4. 增加"install-low.sh"脚本cloud-utils-growpart工具安装
5. 增加自定义检测登录系统失败的次数(登录防护脚本)
6. 调整"account_security.sh"脚本配置"设置控制台登陆失败策略"、"设置SSH登陆失败策略"功能和查看的方法
7. 调整"security_baseline.sh"检查的配置
8. 调整"disable_server.sh"脚本每个功能的输出内容
9. 增加"install-yw.sh"脚本对系统和系统版本的判断,未测试过的系统无法安装工具
10. 修改"install-low.sh"脚本对jdk、mysql是否安装的判断
11. 增加"blj.sh"通过IP方式运维主机方法
12. 修改"dhcp.sh"、"crond_inspect.sh"、"install-low.sh"、"disable_server.sh"脚本
13. 修改"install-yw.sh"脚本对第一个版本号的判断
14. 修改"account_security.sh"脚本的"密码复杂度"、"原有账号密码有效期"的配置
15. 修改所有脚本if语句的判断方式
16. 增加工具对OpenCloudOS 8.8系统的支持 
17. 修改network的所有脚本的执行顺序
18. 修改所有脚本对系统和系统版本的获取方式:从config.ini文件中获取
19. 修改centos8本地安装dhcp服务所缺的依赖包
20. 增加dhcp脚本查看地址池的配置
21. 增加access_control.sh脚本在添加、删除IP前先检测此IP是否已存在
22. 增加access_control.sh脚本如果开启了登录防护功能,无法开启白名单,如果开启了白名单功能,无法开启登录防护功能
23. 调整disable_server.sh脚本关闭白名单的步骤

## 2024.2.19-2024.4.1
1. 增加查看容器的MAC地址
2. 周巡检脚本调整对AlmaLinux release 9.3 alias命令不显示任何内容的判断
3. 调整"install-service.sh"、"disable_server.sh"脚本记录git的安装和卸载有报错的问题
4. 调整移除工具的提示
5. 增加华为Huawei Cloud EulerOS 2.0系统对脚本的使用
6. 调整jiagu_shell.sh、jiagu_shell_enable.sh脚本
7. 调整network_ip.sh、network_br.sh、network_bond.sh、network_ovs.sh四个脚本输出的内容
8. 调整select_check.sh、daily_check.sh、weekly_check.sh脚本对网关的检查
9. 调整tail_log.sh脚本对network日志的查看
10. 调整install_ovs.sh脚本对是否安装成功的判断
11. 调整jiagu_firewall.sh脚本输出的内容
12. 增加移动BigCloud Enterprise Linux 7/8系统对脚本的使用
13. 增加"dstat"、"mtr"、"glances"工具的安装
14. 增加AnolisOS 8.6/8.8系统对脚本的使用
15. 增加openEuler-20.03-LTS-SP3系统对脚本的使用
16. 调整"install_elk.sh"对docker网络的判断
17. 增加openEuler-22.03-LTS-SP1系统对脚本的使用
18. 调整"select_check.sh"、"daily_check.sh"、"weekly_check.sh"脚本对磁盘的检查
19. 增加移动BigCloud Enterprise Linux 20.10/22.10系统对脚本的使用
20. 调整"install-service.sh"、"crond_inspect.sh"、"disable_server.sh"脚本
21. 调整"dhcp.sh"脚本添加到配置文件的参数方式
22. 调整"daily_check.sh、weekly_check.sh、select_check.sh"脚本对获取磁盘和显示磁盘信息的方式
23. 调整"install-yw.bin"脚本对Rocky系统的判断
24. 调整"install-service.sh"脚本Rocky系统yum的配置
25. 调整"install-service.sh"脚本CentOS Stream系统yum的配置
26. 增加AlmaLinux 8.8系统对脚本的使用
27. 调整"install-service.sh"脚本对Rocky9、BC-Linux8系统对部分软件的安装判断
