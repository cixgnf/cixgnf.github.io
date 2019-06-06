# CentOS 普通用户配置 sudo 权限
在 root 权限下执行 visudo ，找到 root ALL=(ALL) ALL 这一行，在下面增加 abc ALL=(ALL) ALL ,其中 abc 是普通用户。
