[English](../../flashing_guide.md) | **简体中文** | [Русский](../Russian/flashing_guide.md)

# Flake 键盘固件刷写指南

## 获取固件

在键盘能够工作之前，你需要为其刷写合适的固件。固件可在 [GitHub 仓库](https://github.com/anywhy-io/flake-zmk-module) 中找到。

要下载固件：
1. 访问仓库的 [Actions 页面](https://github.com/anywhy-io/flake-zmk-module/actions)
2. 选择最近一次成功的构建（由绿色对勾标记）
3. 下载固件包

<img alt="固件下载页面" width="100%" src="../../img/flashing_guide/firmware.png">

## 刷写流程

### 左半边
1. 通过 USB 将键盘的左半边连接到你的电脑
2. 快速连按两次复位按钮，进入引导加载模式（bootloader mode）
   - 键盘将在你的文件管理器中显示为一个存储设备
3. 找到以 "anywhy_flake_left..." 开头的文件（扩展名为 `.uf2`）
4. 将此文件复制到键盘的存储设备中
   - 刷写完成后，设备将自动断开连接

### 右半边
1. 断开左半边的连接，然后连接右半边
2. 使用以 "anywhy_flake_right..." 开头的文件重复相同的过程

## 使用 ZMK Studio 进行配置

### 初始连接
1. 重新连接键盘的左半边
2. 访问 [ZMK Studio](https://zmk.studio) 网站

<img alt="ZMK Studio USB 连接" width="100%" src="../../img/flashing_guide/zmk_usb.png">

3. 点击 USB 按钮，并从设备列表中选择 "Anywhy Flake"

### 解锁键盘

要解锁键盘的配置功能：

1. 按住右半边最左侧的拇指键，进入第二层
2. 按下左半边额外食指列上最下方的按键

<img alt="ZMK Studio 解锁过程" width="1-00%" src="../../img/flashing_guide/zmk_unlock.png">

这将让你进入 ZMK Studio 界面，在这里你可以自定义键盘的设置。

<img alt="ZMK Studio 界面" width="100%" src="../../img/flashing_guide/zmk_studio.png">

### 设置配列
1. 在左侧边栏中，从可用选项中选择你的键盘尺寸
2. 这将确保所有配置都与你的 Flake 型号相匹配

<img alt="ZMK Studio 配列选择" width="100%" src="../../img/flashing_guide/zmk_layout.png">

## 最后步骤

你的 Flake 键盘现在已经准备就绪！你可以：
- 继续通过 USB 连接使用
- 断开 USB 线缆，切换到蓝牙模式
- 使用 ZMK Studio 自定义你的键盘布局和功能

随意尝试不同的配置，找到最适合你的设置。