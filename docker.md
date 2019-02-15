# CentOS 6.8 删除网卡 docker0
## 有一台 CentOS 6.8 的服务器卸载 docker 后网络设备里仍然有 docker0，想把它删掉。经过查询发现虚拟网卡 docker0 其实是一个网桥，是在启动 Docker Daemon 时创建的，可以通过以下方法删除。
### 关闭 docker 服务
sudo service docker stop
### 关闭 docker0 网桥
sudo ifconfig docker0 down
### 删除 docker0 网桥
sudo brctl delbr docker0
