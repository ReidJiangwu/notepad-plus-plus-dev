# ROADMAP

## 当前阶段
- 进行中：完成右键命名转换（SmallCamel、BigCamel、Small snake、Big snake）的 Windows 环境安装与功能验证。

## 已完成
- 增加 4 个编辑命令 ID：`IDM_EDIT_SMALLCAMELCASE`、`IDM_EDIT_BIGCAMELCASE`、`IDM_EDIT_SMALLSNAKECASE`、`IDM_EDIT_BIGSNAKECASE`。
- 在默认 `contextMenu.xml` 中新增四个同级菜单项，紧随“转成大写”“转成小写”，并绑定新 ID（右键可见）。
- 在命令分发里接入四种转换入口，含单选与多选处理。
- 将四个新命令加入宏录制白名单。
- 将四个新命令加入主编辑态可用性控制（`hasSelection` 驱动）。
- 在右键菜单弹出时对四个新命令按 `hasSelection` 做上下文可用性控制。
- 生成未签名的完整 x64 NSIS 安装包，包含自编译 `notepad++.exe`、内置插件、GUP 更新器及 Explorer 右键扩展。
- 在 README 记录右键命名转换的用法，并加入实际菜单截图。

## 进行中
- 待完成：在 Windows/MSYS2 或 Visual Studio 环境执行完整构建并启动后，手工验证右键菜单与四种转换结果（当前 Linux 容器不能运行 Windows GUI 程序）。

## 待办
- 待做：确认是否需要为四项转换补充快捷键与主菜单入口（当前仅右键可达）。

## 阻塞
- 无。

## 最近验证
- 2026-07-18：使用 `x86_64-w64-mingw32-g++-posix` 完成 Release 全量构建，菜单项已改为紧随“转成大写”“转成小写”的四个同级项；生成 `PowerEditor/installer/build/npp.8.9.6.4.Installer.x64.exe`（7,954,481 bytes，SHA-256：`a353bf366085a8822c8cf02b00ccfc162313574893590864ea13ca9030024a69`）。解包核对已包含自编译主程序、三项内置插件、GUP 更新器、插件列表和 NppShell Explorer 右键扩展。安装与编辑器右键菜单仍待 Windows 手工验证。
- 2026-07-18：README 已补充本地命名风格转换说明、四种格式和已有配置的刷新方法，并加入右键菜单截图。
