[English](README.md) | [简体中文](README.zh-CN.md)

# tinyterm

A native terminal for **SSH**, **serial ports** and the **local shell**, with a
data-studio view for serial devices: live plots, dashboard tiles, hex view,
timestamped log, binary frame parsing, X/YMODEM send and scriptable macros.
Linux, macOS and Windows.

Website: **[tinyterm.zxkmm.com](https://tinyterm.zxkmm.com)**

This repository hosts the **binary releases** and the **issue tracker**.
Download a package from [Releases](../../releases), and report bugs or ask for
features in [Issues](../../issues).

## Downloads

| Platform | Package |
| --- | --- |
| macOS (Apple silicon + Intel) | `tinyterm-<ver>-macos-universal.dmg` |
| Linux x86_64 / aarch64 | `tinyterm-<ver>-<arch>.AppImage`, `tinyterm_<ver>_<arch>.deb`, or the `.tar.gz` |
| Windows x86_64 | `tinyterm-<ver>-windows-x86_64-setup.exe` (installer) or the portable `.zip` |

`SHA256SUMS` in each release lists the checksums.

**macOS:** the app is not notarized yet. On first launch, right-click
tinyterm.app → Open, or run `xattr -dr com.apple.quarantine /Applications/tinyterm.app`.

**Linux serial ports:** your user needs to be in the `dialout` group
(`uucp` on Arch) to open `/dev/ttyUSB*` / `/dev/ttyACM*`.

## Features

- SSH (password, keyboard-interactive, key files; known_hosts checking), serial
  ports and the local shell, each in its own tab, with saved profiles and
  session restore
- Saved passwords, optionally behind a primary password
- Serial: any baud rate, line settings, flow control, "wait for device" that
  reopens the port the moment it is plugged back in, session log, send file,
  XMODEM / XMODEM-1K / YMODEM send
- Data studio: live plots, dashboard tiles (gauges, bars), XY plot, hex view,
  timestamped log, binary frame parser with bit fields, CSV export
- Macros: Rhai scripts with dialogs and option forms, output triggers, built-in
  demos
- Scrollback, selection and copy, find

## Reporting a bug

Please include the tinyterm version (ℹ in the tab bar → About), your OS, the
connection kind (SSH / serial / local) and the steps that reproduce it. For
serial issues, the adapter or device and the line settings help a lot.

## Licence

Free to use and to redistribute unmodified. See [LICENSE.txt](LICENSE.txt).
tinyterm is closed source. The third-party libraries it uses keep their own
licences; their texts ship as `THIRD-PARTY-LICENSES.txt` in every package and
are shown in the app's About window.
