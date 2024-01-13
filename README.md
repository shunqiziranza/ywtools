# ywtools
已测试系统:
        centos7
        centos8
        centos steam8
        centos steam9
        rocky 8
        rocky 9
        AlmaLinux 8.2/8.4
        AlmaLinux 9.0
备注:linux运维工具
#############################################################################################################
 NAME: 
	ywtool - Yunwei tool
        
 AGE: 
	ywtool [global options] command [command options] [arguments...]
        
 VERSION: 
	v1.16.30  2024年 01月 13日 星期六 23:43:19 CST 
        
 COMMANDS: 
	install													install service
	blj													跳板机模式配置
	mail													SMTP配置
	vsftp													VSFTP配置
	account													账号策略配置
	backup													备份工具
	remove													移除工具
	dhcp    [config]											DHCP配置
	security baseline											安全基线
	access  { white  | black }										黑白名单访问配置
	inspect { daily  | weekly }										巡检配置
	ssh	[ config | peer [IP] ]										SSH密钥登陆
	clean	{ log  | cache | journal }									清理日志
	jiagu	{ auto | shell | single }									安全加固
	network	{ ip   | br  | ovs  | bond }									配置网卡
	check	[ -I   | all | io   | elk | php | mysql | nginx | system | docker_nbip ]			检查已安装软件的版本
	disable { ssh  | blj | mail | vsftp | shell | white | black | daily | weekly | -h | ... }		关闭功能
	
 GLOBAL OPTIONS::
	--help,-h												查看帮助
	--tail [COMMANDS]											查看日志
	--history												回放跳板机当天运维主机的操作记录
#############################################################################################################
#增加了SMTP配置
#修改一些脚本文件

#增加了ssh配置

#2023.1.28
#增加了vsftp配置

#2023.2.18
#增加了日巡检、周巡检
#巡检报告定期压缩
#log日志3天清理
#ssh禁止root使用密码登陆
#log日志名称修改

#2023.2.20
#增加了备份工具
#增加了移除工具                  

#2023.3.20
#增加了账号策略查看、修改等配置
#增加logo
#增加关闭功能
#增加堡垒机模式
#增加黑白名单访问控制

#2023.4.4
#增加加固shell功能

#2023.4.17
#增加堡垒机回放功能

#2023.5.21
#增加安全基线功能

#2023.6.17
#堡垒机增加运维本机资产
#调整堡垒机退出后进程依然存在问题

#2023.7.15
#调整堡垒机查看回放功能
#调整centos8白名单功能
#调整防火墙加固功能
#调整加固shell-禁用vsftp、sftp、telnet

#2023.7.21
#增加备份文件定期删除
#调整日志文件每天重置逻辑
#调整备份文件的路径
#调整移除工具步骤
#调整加固shell退出后进程依然存在问题
#调整日巡检登陆次数和防火墙默认区域配置文件
###########################
mail:1843929213@qq.com
