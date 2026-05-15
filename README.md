使用shift+tab，可以让CC在计划模式、默认模式和Accept Edits模式之间来回切换
模式
功能
默认模式
启动 Claude Code 后的初始交互状态，类似于一个增强版的对话终端，用于意图确认、信息查询和简单任务。
计划模式
 Claude 进行复杂的代码更改时，它会进入这一阶段。分析需求并制定执行步骤。不直接动代码。
Accept Edits模式
这是 Claude Code 的“落地”阶段，会执行代码变更的最终确认与写入
额外提醒：
1. 如果希望CC能一路绿灯执行所有操作，需要输入指令/exit 退出重启后，在启动CC时输入以下命令
claude --dangerously-skip-permissions
2. CC在Accept Edits模式下，执行终端命令时，下图三个选项的含义依次分别是：
  - 仅同意这一次的命令执行
  - 同意，且该项目之后执行项目依赖安装时，不再询问
  - 不同意，再商量
[图片]

5. 如何提供文件给CC
方式 1：本地文件
使用 @ 指令让CC进行本地文件信息查找：
[图片]
方式 2：图片
直接拖拽图片至对话框，或复制/粘贴：
- Windows：Alt + V
- macOS：Command + V
方式 3：多行文本输入
在CC文本框内换行的快捷键（不是 Shift + Enter）：
- Windows：Ctrl + Enter
- macOS：Option + Enter

6. 指令大全
Claude指令
功能说明
/help
提供所有指令，以及指令背后遵循的意思
/model
切换高中低档模型
/btw
By the way缩写，可以暂时切出正在执行的项目，隔离上下文，方便使用者与CC进行临时对话。会话完毕后，可按esc消除临时会话
/simplify
输入后会派生出3个agent，从代码质量、运行效率和复用性三个角度做一次代码审核，然后自动优化修改
/rewind
进入回滚界面
/compact
主动压缩精简上下文
/clear
彻底清空上下文，相当于重开一个会话
/context
详细展示agent当前的上下文信息，诸如：上下文占比，上下文类别等等
/resume
在全新的上下文窗口，选择恢复到之前的对话
/init
初始化创建项目级Claude.md
/memory
针对Claude的全局、项目记忆，以及auto memory进行操作和管理
/agents
创建、调用、管理子agent
/plugin
发现新插件，管理已下载插件，新增插件生态
  更多指令可参考以下pdf文档：
