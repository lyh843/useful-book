# wsl跟随windows代理

## 1. 配置 .wslconfig 文件

检查 Windows的C:\Users\用户名\.wslconfig 文件是否存在。
如果不存在，则创建一个。
在Windows的C:\Users\用户名\.wslconfig文件中添加如下内容：
>[wsl2]
>networkingMode=mirrored
>dnsTunneling=true

ctrl + s 保存文件，然后退出。

## 2. 重启WSL

在 powershell 中执行：
>wsl --shutdown

然后启动WSL。