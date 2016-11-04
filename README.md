# 《计算机网络》实验

> 本项目为哈尔滨工业大学《计算机网络》实验的代码。使用Python语言进行编写。      
> 软件学院将Python作为主要工作语言的人并不是很多，希望你我能将这份信仰坚持下去。          
> 人生苦短，我用Python!         

请在使用前用pip安装包依赖。

    (sudo) pip install -r requirements.txt
    
## 代理服务器

### 基本功能

- 代理服务器的基本功能
- ~~缓存机制的实现~~（待完善）
- 屏蔽特定用户、特定网站以及钓鱼功能

### 项目说明

**本项目在`proxy`文件夹下。**       
运行`main.py`脚本打开代理服务器，默认端口为`5000`。其中`filter.json`为屏蔽&钓鱼功能的配置文件。`cache`目录为缓存的数据。

## 可靠传输协议的实现

### 基本功能

- GBN协议的实现
- 实现数据的双向传输
- SR协议的实现

### 项目说明

**本项目在`gbn`文件夹下。**     
其中`global_data.py`脚本为gbn协议和sr协议的基本实现。而`client.py`和`server.py`则为服务器和客户端的测试脚本。       
基于20%的数据丢包率进行测试，采用双向传输，C->S和S->C分别使用GBN协议和SR协议进行测试。

## 使用Wireshark分析网络协议

### 基本功能

- 使用Wireshark分析HTTP、TCP、IP协议
- 使用Wireshark分析DNS、UDP、ARP协议

### 项目说明

在Ubuntu下可直接使用以下指令进行安装

    sudo apt-get install wireshark
    
在运行`wireshark`时，一般用户没有抓包的权限。      
官方推荐使用`wireshark`用户组的用户进行抓包，不建议使用`superuser`。    
如果仅为实验，方便起见可以使用超级管理员权限。

    sudo wireshark