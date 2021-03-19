#### 实验1 ubuntu20.04无人值守安装

##### 1. 手动安装ubuntu20.04

* 下载纯净版 Ubuntu 安装镜像 iso 文件（ubuntu-20.04.2-live-server-amd64.iso) 

  ![](img/下载镜像.png) 

* 配置双网卡
  
  ![](img/配置双网卡.png)

* 安装完成
  
  ![](img/手动安装完成.png)

##### 2. 制作包含 user-data 和 meta-data 的 ISO 镜像文件

* 下载老师提供的可用配置文件user-data

* 创建空文件meta.data

* 上传文件到安装好的ubuntu20.04虚拟机
  
 ![](img/文件上传.png)

* 安装cloud-image-utils

 ![](img/安装cloud-img-utils.png) 

* 制作镜像

 ![](img/制作镜像.png) 

* 将镜像传到本地

 ![](img/拷贝镜像.png) 

##### 3. 无人值守安装 

* 新建虚拟机focal-init

 ![](img/新建focal-init.png)

* 移除上述虚拟机「设置」-「存储」-「控制器：IDE」并按顺序先挂载「纯净版 Ubuntu 安装镜像文件」后挂载 focal-init.iso 

 ![](img/挂载镜像.png) 

* 启动虚拟机，命令行中出现以下提示信息时，输入 yes 并按下回车键。 

 ![](img/输入yes.png) 

* 无人值守安装完成

 ![](img/安装完成.png) 

##### 参考资料

* https://c4pr1c3.github.io/LinuxSysAdmin/chap0x01.exp.md.html
  
* https://www.bilibili.com/video/BV1Hb4y1R7FE