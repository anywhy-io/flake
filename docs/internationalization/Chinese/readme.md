[English](../../../readme.md) | ***简体中文*** | [Русский](../Russian/readme.md)

<div align="center">
    <img alt="Flake 键盘海报" width="100%" src="../../img/poster/flake_poster(1:2)_1920p.webp">
    <h3>Anywhy Flake</h3>
    <p><i>一款开源、无线、分体式人体工学键盘，旨在实现高效、健康和愉悦的输入体验。</i></p>
    <p>
        <a href="https://github.com/anywhy-io/flake/stargazers"><img src="https://img.shields.io/github/stars/anywhy-io/flake?style=for-the-badge&color=black" alt="GitHub Stars"></a>
        <a href="https://github.com/anywhy-io/flake/blob/main/LICENSE"><img src="https://img.shields.io/github/license/anywhy-io/flake?style=for-the-badge&color=black" alt="License"></a>
        <img src="https://img.shields.io/badge/Latest%20Version-V2-black?style=for-the-badge" alt="Latest Version: V2">
    </p>
</div>

## 为什么选择 Flake？

到了 19 世纪，人们对更快捷书写方式的需求催生了打字机。两个世纪后，现代键盘的外观并无太大变化，尽管其一体式、行式交错的设计已被证明效率低下且常常对健康有害。

Flake 键盘从根本上解决了这些问题，为每天打字的人们在舒适度和效率方面带来了巨大的提升。

## 核心特性

*   **分体式人体工学设计：** 将键盘的左右两半分开，放在你感觉最舒适的位置，消除手腕压力。
*   **列式交错配列：** 键位排列遵循手指的自然运动轨迹。
*   **无线优先：** 由 ZMK 固件驱动，通过低功耗蓝牙（Bluetooth LE）实现真正的无线自由。
*   **混合式热插拔：** 同时支持 **MX**、**Kailh Choc v1** 和 **Kailh Choc v2** 轴体。
*   **三种尺寸可选：** 选择最适合你的配列：**小号 (40键)**、**中号 (46键)** 或 **大号 (58键)**。
*   **超薄外形：** 极其纤薄和低矮的机身，带来最大的舒适度。
*   **完全开源：** 所有硬件和软件文件均可供你构建、修改和分享。

## 设计背后的理念

### 分体式布局
传统键盘迫使你的前臂向内收拢，手腕以不自然的角度弯曲，长期以往可能导致疼痛。分体式键盘允许你独立放置左右两半，使你的手、手腕和前臂保持在一条舒适的直线上。额外的好处是，两半之间多出的空间可以用来放触控板、笔记本，甚至是你的猫 =^..^=

<img alt="分体式键盘的人体工学摆放" width="100%" src="../../img/table.jpg">

### 列式交错配列
看看你的手——你的手指长短不一，更喜欢上下移动。再看看传统键盘——键位是水平错开的。这种“行式交错（row stagger）”迫使你的手指做出笨拙、不自然的移动。Flake 采用“列式交错（columnar stagger）”，每列键位根据手指的自然伸展范围进行垂直偏移，从而带来更愉快、更高效的打字体验。

<img alt="行式交错键盘图" width="100%" src="../../img/row_stagger.svg">

<img alt="行式交错与列式交错的对比" width="100%" src="../../img/col_stagger.svg">

### 混合式轴体支持
机械轴体的世界广阔而精彩，但只选择一种类型可能会限制你的体验。Flake 通过混合式热插拔轴座解决了这个问题。每个键位都同时设有 **Cherry MX 类**和**凯华矮轴（Kailh Choc）**的插座。这让你随时可以自由尝试不同类型的轴体。

为了给较高的 MX 轴体提供最佳的打字手感和稳定性，外壳文件中包含了一块专用的定位板。在安装轴体前，将这块定位板放在 PCB 上，以确保轴体被牢固固定。矮脚的 Choc 轴则直接安装，不需要定位板。

<img alt="同时展示 MX 和 Choc 轴体的 Flake 键盘" width="100%" src="../../img/flake_switches.jpg">

### 更少按键，更强功能
较少的键位数对于生产力而言似乎有悖常理，但这恰恰是其核心特性，而非妥协。更少的按键意味着你的手可以保持在原位，无需伸长去够远处的按键。

这并不意味着功能减少。在强大的 [ZMK 固件](https://zmk.dev) 支持下，Flake 使用[层 (layers)](https://zmk.dev/docs/keymaps#layers) 来实现传统键盘拥有的所有按键，甚至更多。你可以设置专门的数字层、符号层、导航层、宏定义层以及任何你能想到的功能层，所有这些都只需按一下拇指键即可切换。

<img alt="ZMK 键盘层功能示意图" width="100%" src="../../img/config.svg">

为了适应不同偏好，Flake 提供三种尺寸：
*   **Flake L (58 键):** 适合喜欢更多独立按键的用户。
*   **Flake M (46 键):** 功能与形态的完美平衡。
*   **Flake S (40 键):** 极致的简约与人体工学。

<img alt="Flake L 键盘" width="100%" src="../../img/flake-l.jpg">

### 超薄外形
键盘机身厚度仅为 **约 9 毫米**（不含脚垫）。搭配矮轴和薄键帽，可以创造出极低的桌面输入体验，进一步减少手腕的压力。

<img alt="展示 Flake 键盘纤薄侧面的图片" width="100%" src="../../img/thickness.jpg">

## 打造你自己的 Flake

准备好组装一把了吗？这份全面的组装指南包含了你入门所需的一切。
➡️ **[阅读官方组装指南](./build_guide.md)**

另外，也别忘了看看社区成员们分享的精彩作品！
➡️ **[探索作品展示廊 ✨](../../gallery.md)**

## 致谢

非常感谢：
-   [@foostan](https://github.com/foostan) 的 [Corne Keyboard](https://github.com/foostan/crkbd)，它是我进入人体工学键盘世界的敲门砖。
-   [@pashutk](https://github.com/pashutk) 的 [Chocofi](https://github.com/pashutk/chocofi)，我用了一段时间的超棒的小键盘。
-   [@josefadamcik](https://github.com/josefadamcik) 的 [Sofle](https://github.com/josefadamcik/SofleKeyboard)，它极大地启发了 Flake 的按键布局。
-   [@carrefinho](https://github.com/carrefinho) 的 [Forager](https://github.com/carrefinho/forager)。其巧妙的主控安装方式让 v2 版本在保持键盘纤薄的同时，能够使用 Seeed Xiao 主控。
-   [@ebastler](https://github.com/ebastler/) 的杰出作品 [marbastlib](https://github.com/ebastler/marbastlib)，它被用作轴体封装库的基础。
-   [@petejohanson](https://github.com/petejohanson) 以及所有 [贡献者](https://github.com/zmkfirmware/zmk/graphs/contributors)，感谢他们创造并维护了强大的 [ZMK 固件](https://github.com/zmkfirmware/zmk)。
-   所有致力于 [KiCad](https://gitlab.com/kicad/code/kicad) 和 [FreeCAD](https://github.com/FreeCAD/FreeCAD) 的人们，感谢他们创造了如此强大的开源工具。
-   来自 [ZMK Discord 服务器](https://zmk.dev/community/discord/invite) 的热心朋友们，他们帮助我学习 PCB 设计并解决了无数问题。
-   感谢所有探索非主流技术、深入研究小众领域并创造出惊人事物的人们。

## Stars

点亮一颗星是对这个项目最简单的支持方式！

[![Star History Chart](https://api.star-history.com/svg?repos=anywhy-io/flake&type=Date)](https://star-history.com/#anywhy-io/flake&Date)