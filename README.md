# osanaly
对系统运行信息的监控。

# 准备

以下调用需要提取安装必要程序

## gpu

gpustat是python开发的一个包,可以直接使用pip安装。
> [gpustat](https://github.com/wookayin/gpustat)
> 此工具：gpustat基于`nvidia-smi`，可以提供更美观简洁的展示，结合 watch 命令，可以动态实时监控 GPU 的使用情况。
> 备注，`nvidia-smi`是Nvidia显卡命令行管理套件，基于NVML库，旨在管理和监控Nvidia GPU设备。

* v0.x, 用于：`python 2.7, <3.4`。
* v1.x, 用于：`python3.4+`。

```bash
######################### 安装gpustat #########################
pip -V
# pip 19.3.1 from /usr/local/lib/python2.7/dist-packages/pip (python 2.7)

# 1.在线安装
pip install pytest-runner
pip install gpustat
# 可以查看安装的版本
pip freeze
# gpustat==0.6.0
# pytest-runner==5.2

# 2.离线安装gpustat, 前往github, 找到需要tag, 右边有Release发布版本，选中xxx.tar.gz下载即可。
gpustat-0.6.0.tar.gz
tar -xvf gpustat-0.6.0.tar.gz
cd gpustat-0.6.0
# 通过setup.py进行离线安装
python setup.py install

######################### 使用gpustat #########################
gpustat -v
gpustat -cp
# 等命令
```
