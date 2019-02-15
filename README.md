# CentOS 6.8 删除网卡docker0
关闭 docker 服务
sudo service docker stop
关闭 docker0 网桥（安装docker 自动生成的）
sudo ifconfig docker0 down
删除docker0 网桥
sudo brctl delbr docker0
