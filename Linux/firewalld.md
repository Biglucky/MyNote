### 防火墙操作

```shell
#命令查询
firewall-cmd --help
# 查看firewall 状态
systemctl status firewalld.service
# 启动firewall
systemctl start firewalld.service
# 查看开放服务端口
firewall-cmd --list-services
#增加服务，如增加一个http服务
sudo firewall-cmd --permanent --add-service=http
```

### 修改代理
参考资料:https://blog.csdn.net/hp020740426/article/details/78789680
笔记总结
#### 1. 修改全局的代理
在/etc/profile中可以修改全局代理。
```shell
#(1)修改profile文件
vi /etc/profile

#修改/etc/profile
#add proxy temporaty
http_proxy=http://oa.windoent.com:1003/
export http_proxy

#保存文件，退出，重生效
source /etc/profile

#重启
reboot

#ping 谷歌来测试

```
