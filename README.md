# Ubuntu 18.04 LTS 安裝Cuda及CuDNN

1. [Install Nvidia Driver](#1)
2. [Install CUDA](#2)
3. [Install cuDNN](#3)

<h2 id="1"> Install Nvidia Driver </h2>
更新軟體庫及確認可安裝的版本  

> sudo apt update  
ubuntu-drivers devices

<img src="img/1.png" width = "600">

提示建議安裝nvidia-driver-470
> sudo apt install nvidia-driver-xxx

安裝完畢後重啟電腦，查看Nvidie Driver訊息
> nvidia-smi

<img src="img/2.png" width = "600">

Cuda版本支援到 11.4

<h2 id="2"> Install CUDA </h2>  
https://developer.nvidia.com/cuda-toolkit-archive

選擇要安裝的平台
<img src="img/3.png" width = "600">  

依所提示的指令安裝 CUDA
<img src="img/4.png" width = "600">

顯示卡驅動已經安裝過，故不再安裝
<img src="img/5.png" width = "600">

CUDA安裝完畢後，開敵.bashrc
> sudo gedit ~/.bashrc

添加路徑
```
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda-xx.x/lib64
export PATH=$PATH:/usr/local/cuda-xx.x/bin
```

確認CUDA，開啟新的terminal，輸入
> nvcc -V
安裝成功出現如下
<img src="img/6.png" width = "600">