# linux 中的 pytorch 环境安装

## 1. 安装python环境（略）

### 检查 python3 是否安装

```linux
python3 --version
```

## 2. 安装 miniconda

### 使用清华源下载 

```linux
# 一条命令完成
conda config --remove-key channels 2>/dev/null && \
conda config --add channels defaults && \
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/ && \
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r/ && \
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2/ && \
conda config --set show_channel_urls yes
```

### 环境变量更新

```linux
source ~/.bashrc
```

### 部署虚拟环境

```linux
conda create --name d2l python=3.9 -y
```

该命令中的`d2l`为虚拟环境的名称，可根据自己的需求进行修改。

## 3. 激活与退出虚拟环境

激活指令：

```linux
conda activate d2l
```

该命令中的`d2l`为虚拟环境的名称，可根据自己的需求进行修改，与上文部署的虚拟环境名称保持一致。

退出指令：

```linux
conda deactivate
```