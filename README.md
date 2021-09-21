Wox Suyana修改版
===
此根据WoX (https://github.com/Wox-launcher/Wox)修改。
感谢原作者的辛劳付出。
根据个人习惯添加和修改一些内容，没有合并到Wox原因有：
- 不会... 
- 修改内容是按我个人需求添加的，不一定适合，不一定符合作者想法
- 作者貌似挺久没更新了


修改内容：
===
2021-09-21
- 修改设置，默认语言设置为中文（Settings.cs）
- 修改设置：上次搜索关键字模式=清空上次搜索关键字执行逻辑为隐藏窗体时触发，原逻辑为显示的时候触发，这样会有闪烁现象。(MainViewModel/MainWindow.xaml.cs)
	处理了三种情况：
    - 执行命令后立即清空
    - 失去焦点清空后隐藏（需延时+异步）
    - 按Esc时清空并隐藏（需异步）
- 修复托盘右键菜单没有中文化的问题(Internationalization.cs/MainWindow.xaml.cs)
- 添加设置：是否关闭输入法。启用时，默认弹出窗口自动切换输入法为英文。（Settings.cs/SettingWindow.xaml/MainViewModel.cs）

WoX
===

![Maintenance](https://img.shields.io/maintenance/yes/2020)
[![Build status](https://ci.appveyor.com/api/projects/status/bfktntbivg32e103?svg=true)](https://ci.appveyor.com/project/bao-qian/wox)
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/Wox-launcher/wox?include_prereleases)](https://github.com/Wox-launcher/Wox/releases)
![GitHub Release Date](https://img.shields.io/github/release-date-pre/Wox-launcher/wox?nclude_prereleases)
[![Github All Releases](https://img.shields.io/github/downloads/Wox-launcher/Wox/total.svg)](https://github.com/Wox-launcher/Wox/releases)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/wox-launcher/wox)

**WoX** is a launcher for Windows that simply works. It's an alternative to [Alfred](https://www.alfredapp.com/) and [Launchy](http://www.launchy.net/).

![demo](http://i.imgur.com/DtxNBJi.gif)

Features
--------

- Search for everything—applications, **UWP**, folders, files and more.
- Use *pinyin* to search for programs / 支持用 **拼音** 搜索程序
  - wyy / wangyiyun → 网易云音乐
- Keyword plugin search `g search_term`
- Search youtube, google, twitter and many more
- Build custom themes at http://www.wox.one/theme/builder
- Install plugins from http://www.wox.one/plugin
- Portable mode
- Auto-complete text suggestion
- Highlighting of how results are matched during query search


Installation
------------

- Download from [releases](https://github.com/Wox-launcher/Wox/releases).
  - Option 1: download `Wox-Full-Installer.*.exe`, which include all dependency.
  - Option 2: download `Wox.*.exe`, which only include wox itself. You may install Everything and Python using below instruction.
- Windows may complain about security due to code not being signed. This will be fixed later. 

- Requirements:
  - .NET >= 4.6.2 or Windows version >= 10 1607 (Anniversary Update)
  - [Optional] Integrate with everything
    1. Download `.exe` [installer](https://www.voidtools.com/)
    2. Use x64 if your windows is x64
    3. Version >= 1.4.1 is supported
  - [Optional] Use Python plugins
    1. install [python3](https://www.python.org/downloads/)
    2. add it to `%PATH%` or set it in WoX settings

Usage
-----

- Launch: <kbd>Alt</kbd>+<kbd>Space</kbd>
- Context Menu: <kbd>Ctrl</kbd>+<kbd>O</kbd>
- Cancel/Return: <kbd>Esc</kbd>
- Install/Uninstall plugin: type `wpm install/uninstall`
- Reset: delete `%APPDATA%\Wox`
- Log: `%APPDATA%\Wox\Logs`

Contribution
------------

- First and most importantly, star it!
- Send PR to master branch
- I'd appreciate if you could solve [help_wanted](https://github.com/Wox-launcher/Wox/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22) labeled issue

Build
-----

Install Visual Studio 2019 with .NET desktop development and Universal Windows Platform development

Documentation
-------------
- [Wiki](https://github.com/Wox-launcher/Wox/wiki)
- Outdated doc: [WoX doc](http://doc.wox.one).
- Just ask questions in [issues](https://github.com/Wox-launcher/Wox/issues) for now.

Thanks
------

I would like to thank

- [Raygun](https://raygun.com/) for their free crash reporting account.
- JetBrains for Open Source licence.
