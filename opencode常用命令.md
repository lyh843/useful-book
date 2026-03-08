# OpenCode 常用命令

## 会话管理

```
/sessions
```

查看所有历史会话列表。
 适合在不同项目任务之间切换。

```
/session new
```

创建一个新的对话会话。

```
/session rename
```

重命名当前会话。

```
/session delete
```

删除当前会话。

------

## Agent 切换

```
/agent
```

查看当前可用的 agent。

```
/agent hephaestus
```

切换到指定 agent。

例如：

```
/agent oracle
/agent librarian
/agent explore
```

这些 agent 来自你安装的 **oh-my-opencode** 配置。

------

## 模型查看

```
/models
```

查看当前 provider 可用模型。

```
/model opencode/glm-4.7-free
```

切换当前模型。

------

## 文件操作

```
/files
```

查看当前项目已加载的文件。

```
/add path/to/file.py
```

将文件加入上下文。

```
/add src/
```

将整个目录加入上下文。

------

## 工具与插件

```
/plugins
```

查看当前加载的插件。

```
/doctor
```

诊断 opencode 环境问题（配置、provider、插件等）。

------

## 上下文控制

```
/context
```

查看当前上下文内容。

```
/clear
```

清空当前上下文。

------

## 退出

```
/exit
```

退出 opencode。

或者使用：

```
Ctrl + D
```