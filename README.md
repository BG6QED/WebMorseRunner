# Web Morse Runner（网页版莫尔斯电码练习器）

## 关于
这是一个全新编写的网页版莫尔斯电码练习器（Morse Runner）应用。

该应用托管在 GitHub Pages 上：https://fritzsche.github.io/WebMorseRunner/


本项目的灵感灵感来源于 VE3NEA（Alex Shovkoplyas）开发的《Morse Runner》程序（https://github.com/VE3NEA/MorseRunner）。开发这个全新网页应用的想法，源于作者之前将《Morse Runner》移植到 Linux 和 Mac 系统的尝试（https://github.com/fritzsche/MorseRunner）。


本项目是独立开发的全新版本，与 Alex 的项目无关。原版 Morse Runner 面向 Windows 系统，采用 Pascal 语言开发；而本版本则完全从零开始，使用 JavaScript 编写，旨在支持网页浏览器环境。


## 尚未实现的功能

* 其他竞赛模式（暂不支持 WPX / HST）
* WAV 文件导出
* 最佳成绩列表
* 实时得分统计
* 部分键盘快捷键


## 操作系统支持
Web Morse Runner 已在 **Mac**、**Windows 11** 和 **Linux** 系统上测试通过。
主要测试浏览器为 **Chrome**，但 **Edge**、**Firefox** 和 **Safari** 也被反馈可正常使用。
请注意，作者无法在每次更新时测试所有操作系统与浏览器的组合。

* iOS 设备使用说明*：本项目作者已在多款 iOS 设备（iPhone/iPad）上通过 Safari 和 Chrome 成功运行 Web Morse Runner。使用时需连接外部蓝牙键盘。
如需听到声音，请确保未开启静音模式且音量已调大。在系统设置中确保练习过程不会被节能模式中断。若设备无功能键，可点击网页中的 F1-8 按钮来保持会话活跃。


## 呼号上传
从 0.05 版本开始，Web Morse Runner 会将 `calls.txt` 中的呼号信息缓存到浏览器本地存储中。当你清除本地存储或点击 **reload（重新加载）** 链接时，`calls.txt` 文件会重新加载。
你也可以通过点击 **upload（上传）** 链接，上传自己的呼号文件。
上传的文件必须是标准文本文件，每行包含一个呼号。
请注意，上传格式未来可能会有变动。

呼号文件的格式非常简单，示例文件可在 GitHub 仓库的 `Example_Calls` 文件夹中找到。


## 版本历史
   *（2025-04-13）修复部分漏洞：
      * 避免在原始请求未完成时重复请求额外的 DX 电台。
      * 适配部分 Android 设备的特殊键盘事件（感谢 TOM DG5CW 反馈）。
      * 修复读取新竞赛定义时可能导致竞赛交换字段隐藏的问题。
      * 新增 Alt 修饰键，用于模拟功能键按压。


* **0.6-beta**（2025-2-27）- **狂欢节版本**
   * 代码内部重构，为未来支持多种竞赛模式做准备。
   * Tom（DF7TV）提供了基于 JJ1WTL 数据库的日本呼号列表（文件：JA-All_JJ1QTL）。
   * 提供了基于 DL6ER 数据库的德国呼号列表（文件：DL-All_DOK.txt）。
   * 移动端使用优化：按住 CTRL 或 Meta 键时，可使用数字键替代功能键。
   （部分移动平台不支持功能键）。若键盘带有数字小键盘，也可使用小键盘按键。
   *（部分移动平台不支持功能键）。若键盘带有数字小键盘，也可使用小键盘按键。

* **0.5-beta**（2024-12-27）- **2024 新年版本**
   * 新增对电波条件（QRN、QRM、QSB、信号抖动和干扰）的支持。
   * 新增键盘快捷键：支持 **Shift** 键。
   * 呼号现在缓存到浏览器本地存储，无需重复加载。
   * 实验性功能：支持上传自定义呼号文件（感谢 K5GQ 提供的示例呼号列表）。
   * 修复多个重要漏洞。

* **0.4-alpha**（2024-12-15）- **2024 圣诞版本**
   * 新增堆积模式（pileup mode）。
   * 限制 Tab 键切换范围为呼号/信号报告/编号字段。
   * 增大呼号/信号报告/编号字段的尺寸。
   * 修复多项漏洞。

* **0.3-alpha**（2024-12-12）漏洞修复：修正莫尔斯电码时序，包括对 v0.2-alpha 版本的调整。


## 参考资料
* [Morse Runner](https://github.com/VE3NEA/MorseRunner)（Windows/Pascal 版），作者：VE3NEA - Alex Shovkoplyas
* [Morse Runner 社区版](https://groups.io/g/MorseRunnerCE)
* [Morse Runner 移植版](https://github.com/fritzsche/MorseRunner)（Linux/Mac 版），改编者：DJ1TF - Thomas Fritzsche


## 致谢
特别感谢 VE3NEA（Alex Shovkoplyas），其开发的 Morse Runner 带来了启发。


73（业余无线电祝福用语），Thomas - DJ1TF