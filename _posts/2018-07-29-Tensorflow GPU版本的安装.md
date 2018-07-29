# WIN10 下 Tensorflow GPU版本的安装

##### 准备

- anaconda
- cuda 9.0（目前tensorflow官方的tensorflow只支持这个cuda版本）
- cunn 7.0（目前tensorflow官方的tensorflow只支持这个cunn版本）

##### 安装过程

1. 进入cmd模式

2. 设置conda代理：打开文件C:\Users\Administrator\\.condarc，

   channels:

   - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
   - defaults
     show_channel_urls: true
     ssl_verify: true

   proxy_servers:
       http: http://127.0.0.1:1080
       https: https://127.0.0.1:1080

3. 创建conda环境 ：conda create -n tensorflow-gpu python=3.6

4. 更新pip: conda update pip

5. 安装 tensorflow：pip install --ignore-installed --upgrade tensorflow-gpu --proxy https://127.0.0.1:1080

6. 安装jupyter notebook： conda install jupyter

7. 安装cuda 9.0

8. 安装cunn 7.0

9. 运行jupyter notebook



