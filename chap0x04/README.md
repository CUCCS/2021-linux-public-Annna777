## 实验四：shell脚本编程基础实验

### 实验环境

- Ubuntu 20.04
- Travis

### 实验内容

#### 任务一：用bash编写一个图片批处理脚本，实现以下功能：
- [x] 支持命令行参数方式使用不同功能
- [x] 支持对指定目录下所有支持格式的图片文件进行批处理指定目录进行批处理
- [x] 支持以下常见图片批处理功能的单独使用或组合使用
  - [x] 支持对jpeg格式图片进行图片质量压缩
  - [x] 支持对jpeg/png/svg格式图片在保持原始宽高比的前提下压缩分辨率
  - [x] 支持对图片批量添加自定义文本水印
  - [x] 支持批量重命名（统一添加文件名前缀或后缀，不影响原始文件扩展名）
  - [x] 支持将png/svg图片统一转换为jpg格式

#### 任务二：用bash编写一个文本批处理脚本，对以下附件分别进行批量处理完成相应的数据统计任务：

- [x] 统计不同年龄区间范围（20岁以下、[20-30]、30岁以上）的球员数量、百分比
- [x] 统计不同场上位置的球员数量、百分比
- [x] 名字最长的球员是谁？名字最短的球员是谁？
- [x] 年龄最大的球员是谁？年龄最小的球员是谁？

#### 任务三：用bash编写一个文本批处理脚本，对以下附件分别进行批量处理完成相应的数据统计任务：

- [x] 统计访问来源主机TOP 100和分别对应出现的总次数
- [x] 统计访问来源主机TOP 100 IP和分别对应出现的总次数
- [x] 统计最频繁被访问的URL TOP 100
- [x] 统计不同响应状态码的出现次数和对应百分比
- [x] 分别统计不同4XX状态码对应的TOP 10 URL和对应出现的总次数
- [x] 给定URL输出TOP 100访问来源主机

### 实验要求

- 所有源代码文件必须单独提交并提供详细的脚本内置帮助信息
- 任务二的所有统计数据结果要求写入独立实验报告

### 实验过程

#### 任务1

##### 实验过程

1. 安装imagemagick、shellcheck和p7zip
```sudo apt-get update 
sudo apt-get install -y shellcheck imagemagick p7zip-full
```

2. 将图片文件上传到Linux
   
   ![](img/上传图片.png)

3. 编辑脚本

4. 本地测试

5. 编写`.travis.yml`文件后上传至GitHub测试

##### 实验结果

- [任务1实验结果](./任务1结果.md)

#### 任务2.1

##### 实验过程

1. 下载[2014世界杯运动员数据](https://c4pr1c3.github.io/LinuxSysAdmin/exp/chap0x04/worldcupplayerinfo.tsv)到本地
   
   ```wget "https://c4pr1c3.gitee.io/linuxsysadmin/exp/chap0x04/worldcupplayerinfo.tsv"```

   ![](img/下载数据文件.png)

2. 编辑脚本
3. 本地测试
4. 编写`.travis.yml`文件后上传至GitHub测试

##### 实验结果

- [任务2.1实验结果](./任务2.1结果.md)

#### 任务2.2

##### 实验过程

1. 下载[Web服务器访问日志](https://c4pr1c3.github.io/LinuxSysAdmin/exp/chap0x04/web_log.tsv.7z)到本地

```wget "https://c4pr1c3.gitee.io/linuxsysadmin/exp/chap0x04/worldcupplayerinfo.tsv"
7z x web_log.tsv.7z
```
2. 解压`Web服务器访问日志.tsv`文件
3.  编辑脚本
4. 本地测试
5. 编写`.travis.yml`文件后上传至GitHub测试

##### 实验结果

- [任务2.2实验结果](./任务2.2结果.md)

#### Travis

- [Travis部署结果](https://travis-ci.com/github/CUCCS/2021-linux-public-Annna777)

### 参考资料
- [Linux 系统与网络管理(2021)视频](https://www.bilibili.com/video/BV1Hb4y1R7FE?p=79)
- [LyuLumos的ch0x04实验报告](https://github.com/CUCCS/linux-2020-LyuLumos/blob/ch0x04/ch0x04/%E7%AC%AC%E5%9B%9B%E6%AC%A1%E5%AE%9E%E9%AA%8C%E6%8A%A5%E5%91%8A.md)
- [SagiSiuirs的chap0x04实验报告](https://github.com/CUCCS/2021-linux-public-SagiSiuirs/blob/chap0x04/%E5%AE%9E%E9%AA%8C%E6%8A%A5%E5%91%8A%E5%9B%9B.md)