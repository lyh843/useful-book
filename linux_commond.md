# Linux 常用指令介绍

## 文件和目录操作

### ls - 列出目录内容

```bash
ls                    # 列出当前目录内容
ls -l                 # 以详细格式列出文件信息
ls -a                 # 显示隐藏文件
ls -la                # 显示所有文件的详细信息
```

### cd - 切换目录

```bash
cd /path/to/directory # 切换到指定目录
cd ..                 # 返回上级目录

cd ~                  # 返回用户主目录
cd -                  # 返回上次所在目录
```

### pwd - 显示当前工作目录

```bash
pwd                   # 显示当前工作目录的完整路径
```

### mkdir - 创建目录

```bash
mkdir dirname         # 创建新目录
mkdir -p a/b/c        # 递归创建多级目录
```

### rm - 删除文件或目录

```bash
rm filename           # 删除文件
rm -r dirname         # 递归删除目录及其内容
rm -f filename        # 强制删除文件
```

### cp - 复制文件或目录

```bash
cp file1 file2        # 复制文件
cp -r dir1 dir2       # 递归复制目录
```

### mv - 移动或重命名文件

```bash
mv oldname newname    # 重命名文件或目录
mv file /path/to/dir  # 移动文件到指定目录
```

## 文件查看和编辑

### cat - 显示文件内容

```bash
cat filename          # 显示文件全部内容
cat file1 file2       # 连接显示多个文件
```

### less/more - 分页查看文件内容

```bash
less filename         # 分页查看文件内容（推荐）
more filename         # 分页查看文件内容
```

### head/tail - 显示文件头部/尾部

```bash
head filename         # 显示文件前10行
tail filename         # 显示文件后10行
tail -f filename      # 实时查看文件末尾更新
```

### vim/nano - 编辑文件

```bash
vim filename          # 使用vim编辑文件
nano filename         # 使用nano编辑文件
```

## 系统信息和进程管理

### ps - 显示进程信息

```bash
ps                    # 显示当前终端的进程
ps aux                # 显示所有进程详细信息
```

### top/htop - 实时进程监控

```bash
top                   # 显示系统进程和资源使用情况
htop                  # 更友好的进程监控界面（需要安装）
```

### kill - 终止进程

```bash
kill PID              # 终止指定PID的进程
kill -9 PID           # 强制终止进程
```

### df - 显示磁盘使用情况

```bash
df -h                 # 以人类可读格式显示磁盘使用情况
```

### du - 显示目录大小

```bash
du -h dirname         # 显示目录大小
du -sh dirname        # 显示目录总大小
```

## 网络相关

### ping - 测试网络连接

```bash
ping hostname         # 测试与主机的连接
ping -c 4 hostname    # 发送4个ping包后停止
```

### wget/curl - 下载文件

```bash
wget url              # 下载文件
curl url -o filename  # 使用curl下载文件并指定保存名
```

### ssh - 连接到远程服务器

```bash
ssh user@hostname     # 连接到远程服务器
```

## 搜索和查找

### find - 搜索文件

```bash
find /path -name "filename"    # 在指定路径查找文件
find . -type f -name "*.txt"   # 在当前目录查找txt文件
```

### grep - 搜索文本

```bash
grep "text" filename  # 在文件中搜索文本
grep -r "text" dir/   # 递归搜索目录中的文本
```

## 系统管理

### sudo - 以管理员权限执行命令

```bash
sudo command          # 以root权限执行命令
```

### systemctl - 管理系统服务

```bash
systemctl start service   # 启动服务
systemctl stop service    # 停止服务
systemctl status service  # 查看服务状态
```

### history - 显示命令历史

```bash
history               # 显示命令历史
```

## 环境变量管理

### export - 设置环境变量

```bash
export VAR=value      # 设置环境变量
echo $VAR             # 显示环境变量值
```

### source - 重新加载bash配置文件

```bash
source ~/.bashrc      # 重新加载bash配置文件
```