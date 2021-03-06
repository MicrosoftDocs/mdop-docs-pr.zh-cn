---
title: 使用 UE-V 生成器创建 UE-V 设置位置模板
description: 使用 UE-V 生成器创建 UE-V 设置位置模板
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804009"
---
# 使用 UE-V 生成器创建 UE-V 设置位置模板


Microsoft 用户体验虚拟化（UE-V）使用*设置位置模板*在用户计算机之间漫游应用程序设置。 用户体验虚拟化附带了一些标准设置位置模板。 你还可以通过 UE-V 生成器创建、编辑或验证自定义设置位置模板。

UE-V 生成器监视应用程序以发现和捕获应用程序存储其设置的位置。 正在监视的应用程序必须是传统的应用程序。 UE-V 生成器无法从以下应用程序类型创建设置位置模板：

-   虚拟化应用程序

-   通过终端服务提供的应用程序

-   Java 应用程序

-   Windows 8 应用程序

**注意** UE-V 模板不能从虚拟化应用程序或终端服务应用程序创建。 但是，可将使用模板同步的设置应用于这些应用程序。 若要创建支持虚拟桌面基础结构（VDI）和终端服务应用程序的模板，请使用 UE-V 生成器打开 Windows Installer 文件（.msi）版本的应用程序。

 

**排除的位置**

发现过程不包括经常存储应用软件文件的位置，这些文件不能在用户计算机或环境之间实现良好漫游。 以下内容将被排除：

-   HKEY \ _CURRENT 已登录用户无法向其写入值的 _USER 注册表项和文件

-   HKEY \ _CURRENT \ _USER 与 Windows 操作系统的核心功能相关联的注册表项和文件

-   位于 HKEY \ _LOCAL \ _MACHINE 配置单元中的所有注册表项

-   位于程序文件目录中的文件

-   位于用户 \\ [用户名 \] \\ AppData \\ LocalLow 中的文件

-   位于% systemroot% 中的 Windows 操作系统文件

如果需要在这些排除位置存储的注册表项和文件才能漫游应用程序设置，管理员可以在模板创建过程中手动将位置添加到设置位置模板。

## 创建 UE-V 模板


使用 UE-V 生成器为业务线应用程序或其他应用程序创建设置位置模板。 创建应用程序的模板后，你可以将模板部署到计算机，以便用户可以漫游该应用程序的设置。

**使用 UE-V 生成器创建 UE-V 设置位置模板**

1.  依次单击 "**开始**"、"**所有程序**"、" **microsoft 用户体验虚拟化**"，然后单击 " **microsoft 用户体验虚拟化生成器**"。

2.  单击 "**创建设置位置模板**"。

3.  指定应用程序。 通过浏览找到要为其创建设置位置模板的应用程序（.exe）或应用程序快捷方式（.lnk）的文件路径。 指定命令行参数（如果有）和工作目录（如果有）。 单击**下一步**以继续。

    **注意** 在应用程序启动之前，系统将显示 "**用户帐户控制**" 提示。 需要权限来监视应用程序用于存储设置的注册表和文件位置。

     

4.  应用程序启动后，关闭该应用程序。 UE-V 生成器记录应用程序存储其设置的位置。

5.  过程完成后，单击 "**下一步**" 以继续。

6.  查看并选中相应注册表设置位置和设置文件位置旁边的复选框，以便为此应用程序漫游。 该列表包含设置位置的以下两个类别：

    -   **标准**：存储在注册表中的应用程序设置，这些设置存储在 HKEY \ _CURRENT \ _USER 键或在 \\**用户**\\ [用户名 \] \ **AppData**漫游] 下的文件文件夹中  \\  **Roaming**。 UE-V 生成器默认包括这些设置。

    -   **非标准**：存储在设置数据存储的最佳做法中指定的位置之外的应用程序设置（可选）。 其中包括 " **Users** \\ [用户名 \] \" \ " **AppData**  \\  **本地**的文件和文件夹"。 查看这些位置以确定是否将它们包含在 "设置位置" 模板中。 选中 "位置" 复选框以包括它们。

    单击**下一步**以继续。

7.  查看和编辑设置位置模板的任何**属性**、**注册表**位置和**文件**位置。

    -   在 "**属性**" 选项卡上编辑以下属性：

        -   **应用程序名称**：写入程序文件属性说明中的应用程序名称。

        -   **程序名称**：从程序文件属性中获取的程序的名称。 此名称通常具有 .exe 扩展名。

        -   **产品版本**：应用程序的 .exe 文件的产品版本号。 此属性与文件版本结合使用，可帮助确定设置位置模板面向的应用程序。 此属性接受主版本号。 如果此属性为空，则设置位置模板将应用于产品的所有版本。

        -   **文件版本**：应用程序 the.exe 文件的文件版本编号。 此属性与产品版本结合使用，可帮助确定设置位置模板面向的应用程序。 此属性接受主版本号。 如果此属性为空，则设置位置模板将应用于该程序的所有版本。

        -   **模板作者名称**（可选）：设置位置模板作者的名称。

        -   **模板作者电子邮件**（可选）：设置位置模板作者的电子邮件地址。

    -   "**注册表**" 选项卡列出了 "设置位置" 模板中包含的注册表位置的**密钥**和**范围**。 通过使用 "**任务**" 下拉菜单编辑注册表位置。 任务包括添加新密钥、编辑现有密钥的名称或范围、删除密钥以及浏览注册表项所在的位置。 使用 "**所有设置**" 范围将所有注册表设置包含在指定的键下。 使用 "**所有设置" 和 "子项**"，将所有注册表设置包含在指定的项、子项和子项设置下。

    -   "**文件**" 选项卡列出了 "设置位置" 模板中包含的文件位置的文件路径和文件掩码。 通过使用 "**任务**" 下拉菜单来编辑文件位置。 文件位置的任务包括添加新文件或文件夹位置、编辑现有文件或文件夹的范围、删除文件或文件夹以及在 Windows 资源管理器中打开所选位置。 将文件掩码保留为空，以包括指定文件夹中的所有文件。

8.  单击 "**创建**" 并将设置位置模板保存在计算机上。

9.  单击 "**关闭**" 以关闭 "设置模板" 向导。 退出 UE-V 发生器应用程序。

    为应用程序创建设置位置模板后，应测试该模板。 在实验室环境中部署模板，然后再将其放入企业中的生产环境中。

## 相关主题


[使用自定义 UE-V 模板和 UE-V 生成器](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[UE-V 1.0 的操作](operations-for-ue-v-10.md)

 

 





