> [!NOTE]
>
> - 本文是对 [FirPE Project](https://firpe.cn) 网站中相关操作的详细说明
> - 在有条件的基础上，请尊重版权（购买正版，即：给微软打钱）
> - 在有条件的基础上，请给 [FirPE 作者](https://firpe.cn/donate) 购买一杯咖啡 ☕

# 第一章：制作 WinPE 启动盘

## 1.1 概述

所谓的 WinPE (Windows Preinstallation Environment) 就是预安装环境，它是一种极简的操作系统环境，通常用来进行系统安装、修复或备份等操作。

> [!NOTE]
>
> 需要一个 U 盘来制作 WinPE 系统！

在 `U 盘`中安装 WinPE 系统后，可以通过 U 盘启动电脑，进入 WinPE 环境进行操作：系统修复、数据恢复以及磁盘分区等。

## 1.2 下载 FirPE

1. 点击进入 [FirPE 官网](https://firpe.cn/page-247)

2. 下载 FirPE：

![](./assets/10.png)

![](./assets/11.png)

3. 查看下载的 FirPE ：

![](./assets/12.png)

## 1.3 制作启动盘

1. 将事先准备好的 U 盘插入到电脑中：

![](./assets/13.png)

2. 打开上面下载的 FirPE 程序，点击「全新制作」按钮制作启动盘：

> [!CAUTION]
>
> 此操作会将 U 盘中的所有数据清除，请提前备份 U 盘中的资料，防止数据丢失！

> [!NOTE]
>
> [制作器各种选项说明](/feature/bootdisk/#写入模式配置指南)

![](../../feature/bootdisk/assets/make_disk.gif)

# 第二章：下载 Windows 和 Office

## 2.1 概述

- 该网站上提供的所有下载链接均指向正版文件。

![](./assets/1.png)

## 2.2 下载 Windows 系统镜像

1. 点击[下载链接](https://massgrave.dev/windows_11_links)：

![](./assets/2.gif)

2. 下载指定语言版本的操作系统，如：[简体中文](https://drive.massgrave.dev/zh-cn_windows_11_business_editions_version_24h2_x64_dvd_5f9e5858.iso)：

![](./assets/3.gif)

![](./assets/4.gif)

3. 查看下载的 Windows 系统镜像：

![](./assets/5.gif)

## 2.3 下载 Office

1. 点击[下载链接](https://gravesoft.dev/office_c2r_links)：

![](./assets/6.gif)

2. 下载指定语言版本的 Office，如：[简体中文](https://c2rsetup.officeapps.live.com/c2r/download.aspx?ProductreleaseID=ProPlus2024Retail&platform=x64&language=zh-cn&version=O16GA)：

![](./assets/7.gif)

3. 查看下载的 Office 安装包：

![](./assets/8.gif)

## 2.4 复制到 U 盘

将下载的 Windows 镜像以及 Office 安装包复制到 U 盘中：

![](./assets/15.gif)

# 第三章：安装 Windows 和 Office

## 3.1 进入 WinPE

1. 将刚才制作好的 WinPE 启动盘 插入到电脑上，并重启系统，以便引入 BIOS：

![](./assets/16.png)

2. 进入 WinPE （硬件不同，进入的方式不同）：

> [!NOTE]
>
> - 不同的硬件，进入 BIOS 的快捷键不同：
>   - **戴尔 (Dell)**、**联想 (Lenovo)**、**华硕 (ASUS)**、**宏碁 (Acer)** 通常是 `F2` 键。
>   - **惠普 (HP)** 通常是 `F10` 键。
>   - **MSI (微星)** 通常是 `Delete` 键。
>   - ...
> - 此处使用 `VMWare WorkStation Pro 17` 来模拟电脑演示，和实际电脑操作方式类似！

![](./assets/17.gif)

## 3.2 硬盘分区

使用 WinPE 自带的分区软件对硬盘进行分区：

> [!CAUTION]
>
> - 全新硬盘默认没有分区，表现为 WinPE 内"此电脑"中看不到硬盘，需要使用硬盘工具进行分区。
> - 如果之前硬盘已有操作系统（即第二次安装操作系统），此时可以不对硬盘进行分区，保留原分区结构。
> - 分区的主要目的是初始化硬盘和区分系统与数据独立，建议以`系统`、`数据`、`游戏`这三者为界限分区。
> - 此操作会将硬盘的文件抹除，需要谨慎操作！

![](./assets/18.gif)

## 3.3 安装 Windows

1. 使用 WinPE 自带的软件进行操作系统的安装：

> [!CAUTION]
>
> - 需要选择 U 盘中的 Windows 镜像作为安装文件！
>
> ::: details 点我查看
>
> ![](./assets/20.png)
>
> :::
>
> - 安装的硬盘是分区之后的硬盘，而不是 WinPE 所在的 U 盘！
>
> ::: details 点我查看
>
> ![](./assets/21.png)
>
> :::

![](./assets/19.gif)

2. 漫长的等待...，操作系统终于安装到本地硬盘上：

![](./assets/22.gif)

3. 在 WinPE 中选择重启系统，拔出 U 盘，进入 Windows 安装过程

> [!CAUTION]
> 如未拔出 U 盘进行 Windows 安装则会影响盘符顺序！

![](./assets/23.gif)

4. 开始 Windows 的安装：

> [!NOTE]
> 中间可能会多次重启，请耐心等待

![](./assets/25.gif)

![](./assets/24.gif)

5. 进行 Windows 系统的设置：

> [!NOTE]
>
> Windows11 默认是需要联网登录微软账户，也可以使用本地账户登录，步骤如下：
>
> ::: details 点我查看
>
> 1. 使用 Shift + F10 调用 cmd 窗口：
>    ![](./assets/26.png)
>
> 2. 在 cmd 窗口，输入如下的命令，并按回车：
>
>    ```cmd
>    oobe\bypassnro.cmd
>    ```
>
>    ![](./assets/27.png)
>
> 3. 等待重启，重启之后，就可以使用本地账户登录：
>    ![](./assets/28.gif)
>
> :::

> [!NOTE]
>
> 根据个人喜好进行设置，以下仅为填写示例内容，请根据实际需要填写！

![](./assets/29.gif)

## 3.4 安装 Office

1. 找到 U 盘中的 Office 的安装包，并复制到桌面上：

![](./assets/30.png)

2. 鼠标双击，下一步安装：

> [!NOTE]
>
> 安装 Office 的时候，需要联网！

![](./assets/31.gif)

3. Office 安装完成：

![](./assets/32.gif)
