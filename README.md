# 项目助手 · CallNotesAssistant

Windows 上的个人项目工作台，提供本地录音与转写、AI 会议纪要、项目待办和企微机器人连接。本仓库提供程序发行包、使用说明和版本记录。

## 下载与运行

1. 打开 [Releases](https://github.com/k1365688544-max/CallNotesAssistant-Downloads/releases)，下载最新版 `CallNotesAssistant-v版本-windows-x64.zip`。
2. 完整解压整个 ZIP，再双击 `CallNotesAssistant.exe`。不要只取 EXE，离线模型和运行库需要保留。
3. 在设置里确认录音设备和记录保存目录。目录含义、热键及录音规则见[使用说明](USER_GUIDE.md)。

每版提供 `.sha256` 校验文件和 `.verify.json` 构建验证报告。在 PowerShell 中可用 `Get-FileHash -Algorithm SHA256 <ZIP路径>` 核对文件。

## 功能

- 双轨通话录音与麦克风面聊录音，分段保存在本机。
- 麦克风占用开始/结束提醒、托盘和录音热键。
- 本地 CPU Paraformer ONNX + VAD 转写；音频不上传，资源不足时延后处理。
- 文字校对、会议纪要、行动项选择导入待办与个人 AI 待办整理。
- 项目待办编辑、完成、恢复、搜索筛选、标题复制及企微机器人连接。

## 使用条件与数据

需要 Windows x64、可用音频设备和桌面应用麦克风权限。录音与转写在本机完成；当前 AI 功能需本机安装并登录 Codex、联网并有可用额度。企微功能需自己的机器人凭据。

录音、转写和待办存入设置中的记录目录，默认“文档\CallNotes”；模型位于程序的 `models` 目录。详细用途见[使用说明](USER_GUIDE.md)。升级前退出旧程序并备份自己的记录目录，保留用户设置与凭据。

## 版本和模型说明

v0.1.1 修复保存待办后跳回清单顶部，保留滚动与选中状态；公开包使用通用示例并附模型许可。

离线模型来源与许可证见[第三方说明](THIRD_PARTY_NOTICES.md)及[Apache-2.0 全文](licenses/Apache-2.0.txt)。第三方模型许可不代表本应用源码采用相同许可。

当前版本为预发布：云端离线测试、EXE 隔离启动、模型散列和 ZIP 校验已完成。真实通话识别、设备切换和长时压力需要实机验证；NPU 未启用，当前使用 CPU 转写。
