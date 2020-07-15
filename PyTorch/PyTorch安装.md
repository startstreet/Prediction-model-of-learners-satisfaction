# PyTorch安装

[TOC]

## 1 安装Anaconda管理Python环境

下载链接：https://repo.anaconda.com/archive/Anaconda3-2020.02-Windows-x86_64.exe

选择为所有用户安装

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200521130010203.png" alt="image-20200521130010203" style="zoom:50%;" />

记得勾选添加到环境变量（否则需要手动添加）

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200521123035431.png" alt="image-20200521123035431" style="zoom: 50%;" />

安装完成后测试是否成功：

cmd输入 `conda --version`

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200521130218512.png" alt="image-20200521130218512" style="zoom:50%;" />



## 2 配置Conda清华镜像源

==十分重要！否则安装一些包会遇到各种网络问题！==

详见： https://mirror.tuna.tsinghua.edu.cn/help/anaconda/

cmd输入： `conda config --set show_channel_urls yes`

在用户目录下新建.condarc文件（例如我的路径是 `C:\Users\AstirMoonscape`）

复制以下到.condarc文件中并保存

```
channels:
  - defaults
show_channel_urls: true
channel_alias: https://mirrors.tuna.tsinghua.edu.cn/anaconda
default_channels:
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/pro
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
custom_channels:
  conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
```

## 3 创建虚拟环境Torch并激活

win+R输入cmd启动命令行窗口

```shell
conda create -n torch python=3.7
```

中间过程有选择提示输入y，如图为创建成功

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517153309656.png" alt="image-20200517153309656" style="zoom:50%;" />

激活虚拟环境torch

```shell
conda activate torch
```

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517153440642.png" alt="image-20200517153440642" style="zoom:50%;" />

## 4 查看GPU对应的CUDA版本

桌面右键-NVIDIA控制面板

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517153620321.png" alt="image-20200517153620321" style="zoom:50%;" />

==如果没有NVIDIA控制面板，说明你的电脑中没有英伟达GPU显卡，之后安装PyTorch选择CPU版本安装即可。==

帮助-系统信息-组件

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517153705958.png" alt="image-20200517153705958" style="zoom:67%;" />

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517153754298.png" alt="image-20200517153754298" style="zoom:50%;" />

如图查看NVCUDA.DLL对应的版本号，我的是CUDA 10.1.120 driver

## 5 进入Pytorch官网选择下载命令

由于PyTorch的集成做的很好，提供了CUDA+CuDNN套件，所以无需另外安装CUDA和CuDNN。

以下列举了各种CUDA版本对应的安装选择，请自行对号入座：

* 如果**CUDA版本>=9.2**，根据你的版本选择对应命令：

https://pytorch.org/

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517154032719.png" alt="image-20200517154032719" style="zoom:50%;" />

如果访问不了PyTorch官网，以下提供了对应命令：

CUDA9.2：`conda install pytorch torchvision cudatoolkit=9.2 -c pytorch -c defaults -c numba/label/dev`

CUDA10.1：`conda install pytorch torchvision cudatoolkit=10.1 -c pytorch`

CUDA10.2：`conda install pytorch torchvision cudatoolkit=10.2 -c pytorch`

注：CUDA是向下兼容的，比如电脑是10.1的CUDA版本，当然可以安装9.2的



* 如果**CUDA版本<9.2**，选择其他版本命令：

https://pytorch.org/get-started/previous-versions/

针对CUDA 9.0以上（PyTorch 1.1）：`conda install pytorch==1.1.0 torchvision==0.3.0 cudatoolkit=9.0 -c pytorch`

CUDA 8.0（PyTorch 1.1）：`conda install pytorch==1.0.0 torchvision==0.2.1 cuda80 -c pytorch`



* 如果**CUDA版本太低或者没有NVIDIA显卡**，选择CPU版本：

`conda install pytorch torchvision cpuonly -c pytorch`

## 6 下载安装PyTorch

进入到cmd，粘贴选择的命令；

==一定是注意在虚拟环境下！==

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200521132601939.png" alt="image-20200521132601939" style="zoom:50%;" />



中间过程选择提示输入y；耐心等待下载即可

安装成功：

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517154305491.png" alt="image-20200517154305491" style="zoom:50%;" />

## 7 测试PyTorch

输入python：

<img src="C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517154426702.png" alt="image-20200517154426702" style="zoom:50%;" />

输入以下两行：

```python
import torch
torch.cuda.is_available()
```

结果为True：

![image-20200517161851591](C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517161851591.png)



## 8 Pycharm中使用PyTorch

其实只要用上面创建好的环境torch，选择环境下的python解释器就可以使用pytorch了。

新建一个项目命名为Torch，点击小齿轮-添加本地

![image-20200517162139780](C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517162139780.png)

选择环境torch所在的路径（找到Anaconda3文件夹所在位置）：./Anaconda3/envs/torch/python.exe

![image-20200517162429676](C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517162429676.png)

![image-20200517162458800](C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517162458800.png)

点击确定，选择create创建

新建python文件，编写代码，右键运行

![image-20200517162701410](C:\Users\AstirMoonscape\AppData\Roaming\Typora\typora-user-images\image-20200517162701410.png)

