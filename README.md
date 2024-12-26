## 一、环境检查

1.  #### 检查网络是否连接（需要能够ping通）

`ping www.baidu.com`

2.  #### 检查是否可以使用yum下载资源

`yum install -y nano`

![](https://p0-xtjj-private.juejin.cn/tos-cn-i-73owjymdk6/0f00f3bc160c4441856b83f2b0669639~tplv-73owjymdk6-jj-mark-v1:0:0:0:0:5o6Y6YeR5oqA5pyv56S-5Yy6IEAgeHkxMjMwNg==:q75.awebp?policy=eyJ2bSI6MywidWlkIjoiMjIzMjQyNTUwMDM4NDQ2NyJ9&rk3s=f64ab15b&x-orig-authkey=f32326d3454f2ac7e96d3d06cdbb035152127018&x-orig-expires=1735813423&x-orig-sign=xCeUGFFV7AThetxAIgpDkWzsSjU%3D)

> 如果出现某进程睡眠/锁定中，请尝试输入 reboot 重启后，重新从上述第一条开始检查

## 二、传入并运行脚本

1.  先将所有脚本都传入虚拟机，脚本见文章末尾。

> 可以直接拖到虚拟机里面的主文件夹 或者 用Xftp传入。

![](https://p0-xtjj-private.juejin.cn/tos-cn-i-73owjymdk6/805c380c8cc242ea9eb16f5079e8acf7~tplv-73owjymdk6-jj-mark-v1:0:0:0:0:5o6Y6YeR5oqA5pyv56S-5Yy6IEAgeHkxMjMwNg==:q75.awebp?policy=eyJ2bSI6MywidWlkIjoiMjIzMjQyNTUwMDM4NDQ2NyJ9&rk3s=f64ab15b&x-orig-authkey=f32326d3454f2ac7e96d3d06cdbb035152127018&x-orig-expires=1735813423&x-orig-sign=2UvXoNbKuI5iNwUEx54V6acNZV4%3D)

2.  分别赋予脚本运行权限

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

***

> 基于以下文章整理  <https://juejin.cn/column/7448197125262196748>
