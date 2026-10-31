[English](README.md) | [简体中文](README.zh-CN.md)

# tinyterm

一个原生终端，支持 **SSH**、**串口** 和 **本地 shell**，并为串口设备提供数据工作台视图：
实时曲线、仪表盘、十六进制视图、带时间戳的日志、二进制帧解析、X/YMODEM 发送和可编程宏。
支持 Linux、macOS 和 Windows。

官网：**[tinyterm.zxkmm.com](https://tinyterm.zxkmm.com)**

本仓库用于发布 **二进制版本** 和 **问题反馈**。
请在 [Releases](../../releases) 下载安装包，在 [Issues](../../issues) 报告 bug 或提出功能建议。

## 下载

| 平台 | 安装包 |
| --- | --- |
| macOS（Apple 芯片 + Intel） | `tinyterm-<ver>-macos-universal.dmg` |
| Linux x86_64 / aarch64 | `tinyterm-<ver>-<arch>.AppImage`、`tinyterm_<ver>_<arch>.deb` 或 `.tar.gz` |
| Windows x86_64 | `tinyterm-<ver>-windows-x86_64-setup.exe`（安装版）或便携版 `.zip` |

每个版本附带的 `SHA256SUMS` 列出了校验值。

**macOS：** 应用暂未公证。首次启动时右键 tinyterm.app → 打开，或运行
`xattr -dr com.apple.quarantine /Applications/tinyterm.app`。

**Linux 串口：** 当前用户需要在 `dialout` 组（Arch 上为 `uucp`）中，才能打开
`/dev/ttyUSB*` / `/dev/ttyACM*`。

## 功能

- SSH（密码、keyboard-interactive、密钥文件；known_hosts 校验）、串口和本地 shell，
  每个会话一个标签页，支持保存配置和恢复会话
- 保存密码，可选主密码保护
- 串口：任意波特率、线路参数、流控；“等待设备”在设备重新插入时立即重新打开；
  会话日志、发送文件、XMODEM / XMODEM-1K / YMODEM 发送
- 数据工作台：实时曲线、仪表盘组件（表盘、柱状）、XY 图、十六进制视图、带时间戳的日志、
  支持位字段的二进制帧解析、CSV 导出
- 宏：Rhai 脚本，支持对话框和选项表单、输出触发器、内置示例
- 回滚查看、选择复制、查找

## 报告 bug

请附上 tinyterm 版本（标签栏中的 ℹ → About）、操作系统、连接类型（SSH / 串口 / 本地）
以及复现步骤。串口问题请尽量注明转换器或设备型号以及线路参数。

## 许可

可免费使用，可免费分发未经修改的安装包，详见 [LICENSE.txt](LICENSE.txt)。
tinyterm 为闭源软件。所使用的第三方库保留各自的许可证，许可文本以
`THIRD-PARTY-LICENSES.txt` 随每个安装包分发，也可在应用的 About 窗口中查看。
