# 霓虹茶舍

[Windows 可玩包与 Unity 工程源码下载](https://github.com/xez65/-/releases/tag/windows-20261029)

玩家下载 `NeonTeahouse-Windows-x64-20261029.zip`，完整解压后运行 `NeonTeahouse.exe`。

开发者下载 `NeonTeahouse-Unity-Source-20261029.zip`，使用 Unity 6000.5.8f1 打开解压后的 `NeonTeahouse-Unity` 目录。

本次通过 GitHub Releases 发布完整工程包；仓库首页仅提供下载入口，不将工程包误表述为已逐文件推送到 Git 分支。

# 霓虹茶舍／灯火长安

## Windows 可玩版本（2026-10-29）

玩家请到 [GitHub Releases](https://github.com/xez65/-/releases/tag/windows-20261029) 下载 `NeonTeahouse-Windows-x64-20261029.zip`。解压整个 ZIP 后，双击 `NeonTeahouse/NeonTeahouse.exe` 即可启动，不需要安装 Unity。请保留同目录的数据文件夹和 DLL。

本次从当前正式场景重新构建 Windows x64 程序，构建结果为成功、0 个错误、0 条警告。ZIP 包含完整运行依赖，已执行压缩包 CRC 检查；校验值和构建摘要见 [发布验证记录](Work/UploadBuild20261028/package-verification.json)。新构建已执行 Direct3D 11 启动检查，运行日志确认 `Day1Bootstrap` 启动并初始化叙事与独立测试存档；本次发布没有重新完成四日全流程人工验收。部分过场影片仍使用现有画面和字幕过渡。

开发者请安装 Git LFS 后克隆本仓库，并执行 `git lfs pull`，再使用 Unity **6000.5.8f1** 打开仓库根目录。正式场景是 `Assets/NeonTeahouse/Scenes/Day1VerticalSlice.unity`。浏览器布局编辑器位于 [HTML GUI 模型](Work/HtmlGuiModels20261028/gallery.html)。Unity 可重建缓存、个人设置、临时存档和旧版中间文件不属于发布包。

2026-10-28 更新 [四日流程与立希视角](docs/project-context.md)：序章、换日和四条烈火尾声已设独立过场入口，缺片时使用现有画面与字幕过渡；旁白加括号，观察物件有特写。三项数值全程隐藏，先尾声、后按执念自动去留。运行 [当前 Windows 程序](Work/FrameworkRevision20261028/player/NeonTeahouse.exe)，查看 [实际画面与验收](Work/FrameworkRevision20261028/gallery.html)。完整影片、四种烈火分支正式CG与新版旧香／静灯CG尚缺。

2026-10-27 接入 [七套正式 Live2D](docs/review/七套正式Live2D接入_2026-10-27.md)：立希轻甲与便装，以及爱音、乐奈、灯、素世和祥子。正式场景读取实际 Cubism 模型，保留六个剧情身份与旧存档兼容。查看 [Unity 实际截图](Work/SevenLive2DIntegration20261027/gallery.html)。

2026-10-26 新增 [五项 UGUI 工具试用](Work/UGUIToolTrial20261026/gallery.html)：MacacaViewSystem、PrimeTween、LoopScrollRect、Auto9Slicer、TMPEffects。在 [独立 Unity 场景](Assets/NeonTeahouse/ToolTrials/UguiToolTrial.unity) 中按 Play，或运行 [Windows 试用程序](Work/UGUIToolTrial20261026/player/NeonTeahouse-ToolTrial.exe)。这是实际集成工具的试用页面，正式四日流程尚未整体迁移；功能和视觉记录见 [接入记录](docs/review/五项UGUI工具接入试用_2026-10-26.md)。

这是当前主要维护的 Unity 四日互动叙事工程。玩家扮演椎名立希，通过接待来客、交谈、调茶、整理手账和逐步核对记忆，认识她与千早爱音的过去，四日相处形成的回忆度与共情度决定高松灯尾声，尾声之后的执念值自动决定立希离店、留店或追查过去营救爱音。

第二日正式正文采用乐奈；为兼容原数据和存档，内部编号仍为 `eri`。四位当日主客依次为长崎素世、乐奈、高松灯和丰川祥子。三结局为留灯、旧香和静灯，高松灯的伙伴、获救收留、救狐未归、烈火身亡四种尾声先发生，随后自动进入立希的去向；三项隐藏数值只在全流程完成后显示。

## 打开与运行

- 使用 Unity **6000.5.8f1** 打开当前目录，而不是外层 `My project (2)` 或 `Design` 中的验证副本。
- 正式场景是 [Assets/NeonTeahouse/Scenes/Day1VerticalSlice.unity](Assets/NeonTeahouse/Scenes/Day1VerticalSlice.unity)。名称保留早期命名，现已绑定四日内容和完整正文。
- 运行后从主菜单开始新游戏，或继续已有存档。正式流程含营业、剧情、调茶、茶后反馈、独立后室、手账、茶柜、回顾、设置及第四夜收束。
- 项目依赖使用 [Packages/manifest.json](Packages/manifest.json)。当前配置采用 Universal Render Pipeline 17.5.0；Ink 插件存在，但活动四日剧情由结构化 JSON 与 C# 流程执行。

## 接手工程先看

| 目标 | 文档或代码入口 |
| --- | --- |
| 理解架构、数据来源、存档和验证边界 | [docs/project-context.md](docs/project-context.md) |
| 修改已审核正文 | [四日篇完整互动剧本_乐奈版](docs/narrative/霓虹茶舍_四日篇完整互动剧本_乐奈版.md) |
| 维护动作、表情和在场角色 | [Live2D 行为标签接入说明](docs/narrative/霓虹茶舍_Live2D行为标签接入说明.md) |
| 理解九类页面与独立后室 | [场景素材接入记录](docs/review/霓虹茶舍_场景素材接入与交互脚本_2026-10-21.md)、[后室修复记录](docs/review/霓虹茶舍_独立后室接入修复_2026-10-21.md) |
| 查看现存后室与手机截图 | [Work/BackroomIntegration20261021/gallery.html](Work/BackroomIntegration20261021/gallery.html) |
| 查看随后接入的街巷论坛 | [论坛接入记录](docs/review/霓虹茶舍_街巷论坛接入_2026-10-21.md)、[论坛图册](Work/ForumIntegration20261021/gallery.html) |
| 绑定过场动画、CG和配音 | [Unity素材绑定说明](Assets/NeonTeahouse/Cinematics/README.md)、[正式CG接入与剩余素材](docs/review/霓虹茶舍_正式CG接入与剩余素材清单_2026-10-24.md)；15个CG位置及1张旧信差分已绑定，视频和配音尚未绑定 |
| 预览第一日过场样片 | [两次都没泡好的茶 · Remotion 样片](Cinematics/first-tea/README.md)，为独立制作项目，尚未接入 Unity |
| 查全工作区的其他项目和素材 | [外层工作区说明](../../docs/workspace-context.md) |

## 不修改内容的快速检查

在当前工程根目录的 PowerShell 中执行：

```powershell
python -X utf8 Tools/narrative/compile-four-day-narrative.py --check
python -X utf8 -m unittest discover -s Tools/narrative -p 'test_*.py' -v
node --test Tools/unity/export-day1-content.test.cjs
```

2026-10-21 在 Windows 11、Python 3.12.10、Node.js v24.19.0 下运行，编译一致性检查通过，Python 8 项通过、Node.js 31 项通过，失败和跳过均为 0。Unity 历史验证和本次未重跑的范围见 [项目上下文](docs/project-context.md#验证记录与适用范围)。

街巷论坛已接入 16 个主帖、54 条回复，按游戏日显示，在后室手机中只读浏览；已有测试、构建和 1920 × 1080 截图记录。它不提供联网、回帖或点赞。源稿和预览中的物证拼图、完整来源卡、联网发送等内容，不因文档或图片存在而计为已完成玩法。

当前 Windows 构建：[NeonTeahouse.exe](Work/SevenLive2DIntegration20261027/player/NeonTeahouse.exe)，包含七套正式 Live2D。运行时保留同目录游戏数据和依赖。旧空间清理记录见 [2026-10-25 记录](../../Work/WorkspaceCleanup20261025/阶段收尾记录.md)；它描述当时缓存状态，不代表当前验证仍使用未导入的工程。
