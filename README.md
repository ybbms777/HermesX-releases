# HermesX

HermesX 是 Windows 桌面 AI 编程助手，基于 MIT 许可的 DeepSeek Harness 修改而来，额外加了记忆和会话搜索功能。本仓库只放安装包，源码不在这里。

HermesX 不是 DeepSeek 官方产品，与 DeepSeek 没有关联。

## 下载

在 [Releases](../../releases) 页面下载 `hermesx-<版本>-win-x64-unsigned.exe`。

下载后可以核对 SHA-256，结果应与 Release 说明里写的一致：

```powershell
Get-FileHash .\hermesx-0.1.0-win-x64-unsigned.exe
```

## 安装

1. 双击安装包。安装到当前用户目录 `%LOCALAPPDATA%\Programs\HermesX`，不需要管理员权限。
2. 安装包没有代码签名，Windows SmartScreen 会提示“Windows 已保护你的电脑”。点“更多信息”，再点“仍要运行”。
3. 第一次启动后，在设置里填入你自己的模型 API Key。

目前只提供 Windows x64 安装包，在 Windows 11 上测试过。

## 和 DeepSeek Harness 并存

HermesX 可以和官方 DeepSeek Harness 装在同一台电脑上，两者互不影响：

| 项目 | HermesX |
| --- | --- |
| 程序目录 | `%LOCALAPPDATA%\Programs\HermesX` |
| 数据目录 | `%USERPROFILE%\.hermesx` |
| 应用数据 | `%APPDATA%\hermesx-desktop` |
| 默认工作区 | `文档\HermesX\default-workspace` |
| 链接协议 | `hermesx://` |

已知限制：官方登录完成页使用 `dsh://` 链接，无法唤起 HermesX。

## 更新

HermesX 不会自动更新，也不会检查更新。新版本发布在本仓库的 Releases 页面，下载新安装包直接覆盖安装即可，数据会保留。

## 卸载

在“设置 → 应用 → 已安装的应用”里卸载 HermesX。卸载会删除程序、快捷方式、应用数据和 `hermesx://` 协议注册。`%USERPROFILE%\.hermesx`（会话、记忆、配置）会保留，不需要的话可以手动删除。

## 许可

基于 DeepSeek Harness 修改，按 MIT 许可发布，原版权声明见 [LICENSE](LICENSE)。
