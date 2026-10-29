# 霓虹茶舍

四日互动叙事游戏。玩家扮演椎名立希，通过观察、交谈、调茶和整理手账推进故事。

## 下载

| 用途 | 下载 |
| --- | --- |
| Windows 64 位可玩版本 | [NeonTeahouse-Windows-x64-20261029.zip](https://github.com/xez65/-/releases/download/windows-20261029/NeonTeahouse-Windows-x64-20261029.zip) |
| Unity 工程源码和正式资产 | [NeonTeahouse-Unity-Source-20261029.zip](https://github.com/xez65/-/releases/download/windows-20261029/NeonTeahouse-Unity-Source-20261029.zip) |
| 文件校验值 | [SHA256SUMS.txt](https://github.com/xez65/-/releases/download/windows-20261029/SHA256SUMS.txt) |

[查看版本说明与全部附件](https://github.com/xez65/-/releases/tag/windows-20261029)。本仓库以 Releases 附件提供完整工程；`main` 分支提供下载入口，不包含逐文件展开的游戏源码。

## 玩家启动

1. 下载并完整解压 Windows ZIP。
2. 打开 `NeonTeahouse` 文件夹，双击 `NeonTeahouse.exe`。
3. 保留 `NeonTeahouse_Data`、`MonoBleedingEdge` 和同目录 DLL；无需安装 Unity。

调茶时选择茶叶、辅料和水温，加水后锁定本杯；开始浸泡后按回车键或点击出汤结束浸泡，再点击奉茶。

## 编辑工程

1. 下载并解压 Unity 源码 ZIP。该附件已包含实际大文件资源，无需安装 Git LFS。
2. 使用 Unity **6000.5.8f1** 打开 `NeonTeahouse-Unity`。
3. 打开 `Assets/NeonTeahouse/Scenes/Day1VerticalSlice.unity`，按 Play。

源码包包含 `Assets`、`Packages`、`ProjectSettings`、当前正式角色和 CG、剧情与交互代码、测试、剧本与项目文档，以及 `Work/HtmlGuiModels20261028/gallery.html` 可编辑 HTML 布局模型。Unity 缓存、机器设置、临时存档和已替代的旧版角色烘焙文件未纳入交付。

## 本版本验证范围

- Windows x64 新构建成功，0 个错误、0 条警告。
- 玩家 ZIP 和源码 ZIP 的全部条目通过 CRC 完整性检查，并附 SHA-256。
- 新构建已执行 Direct3D 11、1280×720 启动检查，日志确认初始化正式叙事流程。
- 本次发布未重新完成完整四日人工游玩验收。部分过场影片仍使用画面与字幕过渡。

源码中的第三方组件和美术资产保留各自现有许可；本下载入口不额外授予其商业使用或再分发权利。
