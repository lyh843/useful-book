# OpenCode 常用命令

## 常用命令

### 会话管理

```
/sessions
```
查看所有历史会话列表。适合在不同项目任务之间切换。
- **快捷键**: `Ctrl+x l`

```
/new
```
开始一个新会话。清除当前上下文并创建新会话。
- **别名**: `/clear`
- **快捷键**: `Ctrl+x n`

```
/session rename
```
重命名当前会话。

```
/session delete
```
删除当前会话。

### 文件操作

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

### Agent 切换

```
/agent
```
查看当前可用的 agent。

```
/agent <name>
```
切换到指定 agent。

例如：
```
/agent build
/agent plan
/agent explore
```

### 模型管理

```
/models
```
查看当前 provider 可用模型。
- **快捷键**: `Ctrl+x m`

```
/model opencode/glm-4.7-free
```
切换当前模型。

### 项目初始化

```
/init
```
创建或更新 `AGENTS.md` 文件。帮助 OpenCode 分析项目结构。
- **快捷键**: `Ctrl+x i`

### 撤销与重做

```
/undo
```
撤销上一步操作。包括文件修改和消息。
- **快捷键**: `Ctrl+x u`

```
/redo
```
重做之前撤销的操作。
- **快捷键**: `Ctrl+x r`

### 上下文控制

```
/compact
```
压缩当前会话，清理上下文。
- **别名**: `/summarize`
- **快捷键**: `Ctrl+x c`

```
/clear
```
清空当前上下文。

```
/context
```
查看当前上下文内容。

### 分享功能

```
/share
```
分享当前会话，生成链接。
- **快捷键**: `Ctrl+x s`

```
/unshare
```
取消分享当前会话。

### 帮助与配置

```
/help
```
显示帮助对话框。
- **快捷键**: `Ctrl+x h`

```
/themes
```
查看可用主题。
- **快捷键**: `Ctrl+x t`

### 连接与认证

```
/connect
```
添加 provider 并配置 API 密钥。

### 工具与诊断

```
/plugins
```
查看当前加载的插件。

```
/doctor
```
诊断 opencode 环境问题（配置、provider、插件等）。

### 显示控制

```
/details
```
切换工具执行详细信息的显示。
- **快捷键**: `Ctrl+x d`

```
/thinking
```
切换 thinking/reasoning 块的可见性。

---

## 不常用命令

### 编辑器相关

```
/editor
```
打开外部编辑器编写消息。使用 `EDITOR` 环境变量指定的编辑器。
- **快捷键**: `Ctrl+x e`

```
/export
```
将会话导出为 Markdown 并在编辑器中打开。
- **快捷键**: `Ctrl+x x`

### 会话管理

```
/new
```
开始新会话。
- **别名**: `/clear`

### 退出

```
/exit
```
退出 opencode。
- **别名**: `/quit`, `/q`
- **快捷键**: `Ctrl+x q`

---

## Shell 命令

### 文件引用

```
@filename
```
在消息中引用文件。会自动将文件内容添加到对话中。

```
@packages/functions/src/api/index.ts
```
引用项目中的特定文件。

### Bash 命令

```
!ls -la
```
运行 shell 命令。命令输出会作为工具结果添加到对话中。

---

## 快捷键速查

| 功能 | 快捷键 |
|------|--------|
| 切换 agent | `Tab` |
| 压缩上下文 | `Ctrl+x c` |
| 显示详情 | `Ctrl+x d` |
| 打开编辑器 | `Ctrl+x e` |
| 帮助 | `Ctrl+x h` |
| 初始化 | `Ctrl+x i` |
| 切换模型 | `Ctrl+x m` |
| 新建会话 | `Ctrl+x n` |
| 重做 | `Ctrl+x r` |
| 会话列表 | `Ctrl+x l` |
| 分享 | `Ctrl+x s` |
| 主题 | `Ctrl+x t` |
| 撤销 | `Ctrl+x u` |
| 退出 | `Ctrl+x q` |
| 导出 | `Ctrl+x x` |

---

## CLI 命令

除了 TUI 命令外，还可以使用命令行命令：

```
opencode                    # 启动 TUI
opencode /path/to/project   # 指定项目目录启动
opencode run "message"      # 非交互模式运行
opencode serve              # 启动 headless 服务器
opencode web                # 启动 web 界面
opencode models             # 列出可用模型
opencode models --refresh   # 刷新模型列表
opencode auth login         # 登录 provider
opencode auth list          # 查看已认证的 provider
opencode agent create       # 创建新 agent
opencode agent list         # 列出所有 agent
opencode mcp add            # 添加 MCP 服务器
opencode mcp list           # 列出 MCP 服务器
opencode session list       # 列出所有会话
opencode stats              # 查看 token 使用统计
opencode export [sessionID] # 导出会话数据
opencode import <file>      # 导入会话数据
opencode upgrade            # 升级 OpenCode
opencode uninstall          # 卸载 OpenCode
```
