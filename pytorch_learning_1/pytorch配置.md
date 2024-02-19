## pytorch配置
### 什么是pytorch
    PyTorch是一个由Facebook的人工智能研究团队开发的开源深度学习框架。
    利用python3.6进行配置
### 下载Anaconda  https://www.anaconda.com/
    Anaconda的作用就是将工作的环境化成很多的独立的房子，在不同的房子里可以隔离运行不同的python版本，集成了很多的工具包
    利用Anaconda分割工作环境，避免python版本的卸载和安装。
    现在Anaconda的版本很高了，历史版本在https://repo.anaconda.com/
    Anaconda3对应的是python3的版本，选择Anaconda3-5.2.0-Windows-x86_64.exe下载安装
### 查看电脑配置
    打开命令行窗口输入nvidia-smi查看显卡的cuda支持的版本，具体的pytorch-cuda-cudatitle版本对应关系需要查看手册
### 建立python3.6环境
    打开conda的命令行窗口，初始显示为（base）
    输入conda create -n pytorch python=3.6
    开始下载pytorch所需环境，询问是否移除搭建的环境，输入y
    环境需要安装的包，输入y
    安装成功后需要激活pytorch环境，输入activate pytorch，左边转为显示（pytorch），可以输入pip list 查看已经安装的包
### 下载pytorch
    进入pytorch官网选择合适的版本，一定需要注意显卡的cuda版本以及pytorch的版本问题，选择cuda10.2，pytorch1.6.0，可以查看历史版本
    复制网站里的链接，粘贴进去conda命令行下载安装
### 检验是否安装成功
    conda命令行输入python，进入python页面，输入import torch，能够继续出现不报错
    继续输入torch.conda.is_available()检验是否返回True，返回True即为安装成功
### 安装pycharm
    官网下载社区版pycharm即可，配置pycharm环境，需要在解释器里选择Anaconda路径里envs虚拟环境里的python文件，这样才可以使用pytorch
    错误一般是pytorch、torchvision、cuda版本不配可以去官网查询对应文档
    检验是否成功和上面方法一样，在pycharm的console里输入import torch，能够继续出现不报错
    继续输入torch.conda.is_available()检验是否返回True，返回True即为安装成功
    注意解释器的选择，需要在Anaconda的路径里选择的，否则无法使用torch
### 配置jupyter notebook
    在conda命令行中激活pytorch后输入conda install nb_conda如果一直在 solving，可以改成使用
    pip install notebook
    安装完成之后使用
    pip list
    查看是否有所需要的库文件，i开头的4个文件
    解决所有问题后打开Jupyter后发现没有创建的虚拟环境，只有python 3
    解决办法：打开Anaconda Prompt，进入pytorch环境，输入如下命令：python -m ipykernel install --name pytorch
    输入jupyter notebook D：打开jupyter

    
    
    
