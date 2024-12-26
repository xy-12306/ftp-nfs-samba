## 一、环境检查

1.  #### 检查网络是否连接（需要能够ping通）

`ping www.baidu.com`

2.  #### 检查是否可以使用yum下载资源

`yum install -y nano`


> 如果出现某进程睡眠/锁定中，请尝试输入 reboot 重启后，重新从上述第一条开始检查

## 二、传入并运行脚本

1.  先将所有脚本都下载或传入虚拟机，脚本见文章末尾。


```
wget https://github.com/xy-12306/ftp-nfs-samba/releases/download/1.2/ftp.nfs.samba.zip
```

2. 将脚本解压缩
```
unzip ftp.nfs.samba.zip
```



3.  分别赋予脚本运行权限

<!---->

    chmod +x ftp_deploy.sh  
    chmod +x samba_deploy_02.sh
    chmod +x nfs_deploy_server.sh 
   


3.  依次运行脚本 `格式:【./+脚本名称】`

<!---->

    # 运行ftp脚本
    ./ftp_deploy.sh

    # 运行samba脚本
    ./samba_deploy_02.sh

    # 运行nfs脚本（这里是server-服务端的，还需要在另一个虚拟机中运行nfs-client-客户端的脚本）
    ./nfs_deploy_server.sh

> 注：上述ftp、samba已经自动部署成功。
>
> ` nfs还需要在另一台虚拟机中按照上述步骤，运行nfs_deploy_client客户端的脚本。`

***

##### 脚本下载链接：

*   [服务器自动部署脚本.zip - 蓝奏云](https://wwsz.lanzn.com/is7Cu2iz7scd)
*   [服务器自动部署脚本.zip - GitHub](https://github.com/xy-12306/ftp-nfs-samba)

***

> 基于以下文章整理  <https://juejin.cn/column/7448197125262196748>
