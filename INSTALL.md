# 安装与使用

## 系统要求

- Apple Silicon（M 系列）Mac。
- macOS 13 或更新版本。
- AI 对话和联网研究需要网络及自己的模型服务 API Key。
- 当前无 Intel Mac、Windows、iOS 或 Android 安装包。

## 安装

从 [Releases](https://github.com/JavaApes/yuan/releases/tag/v0.5.2) 下载 DMG，打开后将 Yuan.app 拖到 Applications，再弹出镜像，从“应用程序”启动。

## 首次打开时的系统提示

v0.5.2 当前公开包采用本地临时签名，未经 Apple Developer ID 正式签名和 Apple 公证。

如果 macOS 提示无法验证开发者，先确认文件来自本仓库的 Release。尝试打开后，可在 **系统设置 → 隐私与安全性** 找到此次拦截提示，选择 **仍要打开**。部分组织管理的 Mac 不允许此操作。

如果系统明确提示恶意软件、文件损坏，或校验值不一致，请停止安装并反馈。不要关闭系统整体安全保护，也不要执行来源不明的绕过命令。

[Apple 官方说明](https://support.apple.com/zh-cn/102445)

## 首次配置

打开 **Agent 设置 → 模型与思考**，选择服务并填写自己的 API Key。可在后台开启或关闭模型，前台只显示开启项；新配置默认使用深入思考，切换模型会提示能力可能变化。

OpenAI 联网研究使用自己的 OpenAI Key。外部 MCP、行情与其他集成需要各自配置，部分连接器可能需要额外运行环境。安装应用不意味着自动获得这些服务的账号或权限。

## 本地数据、升级与卸载

数据目录：`~/Library/Application Support/zhiben-desktop/`。

升级时先退出 Yuan，再替换 Applications 中的 Yuan.app；保留上述数据目录即可保留个人资料。移除应用不会自动删除个人资料。

分享时发送 DMG 或 Release 链接即可，不要发送自己的数据目录。Key 的加密与当前 Mac 的系统安全存储相关，不应把复制数据目录当作密钥迁移方式。

## 文件校验

Release 同时提供 `.sha256` 文件。在终端中进入下载目录后执行：

```sh
shasum -a 256 -c Yuan-0.5.0-macOS-AppleSilicon.dmg.sha256
```

显示 `OK` 表示文件与发布的校验值一致；这不是 Apple 公证或安全审计。

## 当前验证范围

安装包已在开发者的 Apple Silicon Mac 上验证：镜像挂载、复制安装、弹出镜像后启动、全新用户状态及重启。其他设备与全部外部服务仍需实际使用验证。
