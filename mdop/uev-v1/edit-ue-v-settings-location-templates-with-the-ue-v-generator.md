---
title: 使用 UE-V 生成器编辑 UE-V 设置位置模板
description: 使用 UE-V 生成器编辑 UE-V 设置位置模板
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804103"
---
# 使用 UE-V 生成器编辑 UE-V 设置位置模板


使用 Microsoft 用户体验虚拟化（UE-V）生成器编辑设置位置模板。 使用 UE-V 生成器将修改后的设置添加到模板时，模板内的版本信息将自动更新，以确保在企业中部署的任何现有模板都能正确更新。

**如何使用 UE-V 生成器编辑 UE-V 设置位置模板**

1.  依次单击 "**开始**"、"**所有程序**"、" **microsoft 用户体验虚拟化**"，然后单击 " **microsoft 用户体验虚拟化生成器**"。

2.  单击 "**编辑设置位置模板**"。

3.  在最近使用的模板列表中，选择要编辑的模板。 或者，通过**浏览找到**设置模板文件。 单击**下一步**以继续。

4.  查看设置模板的**属性**、**注册表**位置和**文件**位置。 根据需要进行编辑。

    -   "**属性**" 选项卡允许你查看和编辑以下属性：

        -   **应用程序名称**：写入程序文件属性说明中的应用程序名称。

        -   **程序名称**：从程序文件属性中获取的程序的名称。 此名称通常具有 .exe 扩展名。

        -   **产品版本**：应用程序的 .exe 文件的产品版本号。 此属性与**文件版本**一起可帮助确定设置位置模板面向的应用程序。 此属性接受主版本号。 如果此属性为空，则设置位置模板将应用于产品的所有版本。

        -   **文件版本**：应用程序 the.exe 文件的文件版本编号。 此属性与**产品版本**一起有助于确定设置位置模板面向的应用程序。 此属性接受主版本号。 如果此属性为空，则设置位置模板将应用于该程序的所有版本。

        -   **模板作者名称**（可选）：设置模板作者的名称。

        -   **模板作者电子邮件**（可选）：设置位置模板作者的电子邮件地址。

    -   "**注册表**" 选项卡列出了 "设置位置" 模板中包含的注册表位置的**密钥**和**范围**。 可通过使用 "**任务**" 下拉菜单来编辑注册表位置。 任务包括添加新密钥、编辑现有密钥的名称或作用域、删除密钥和浏览注册表（位于其中的注册表项）。 定义注册表的范围时，可以使用 "**所有设置**" 范围将所有注册表设置包含在指定键下。 使用**所有设置**和**子项**将所有注册表设置包含在指定项、子项和子项设置下。

    -   "**文件**" 选项卡列出了 "设置位置" 模板中包含的文件位置的文件路径和文件掩码。 可以通过使用 "**任务**" 下拉菜单来编辑文件位置。 文件位置的任务包括添加新文件或文件夹位置、编辑现有文件或文件夹的范围、删除文件或文件夹以及在 Windows 资源管理器中打开所选位置。 若要包括指定文件夹中的所有文件，请将文件掩码保留为空。

5.  单击 "**保存**" 以将更改保存到 "设置位置" 模板。

6.  单击 "**关闭**" 以关闭 "设置模板" 向导。 退出 UE-V 发生器应用程序。

    在编辑应用程序的设置位置模板后，应测试该模板。 在实验室环境中部署已修改的设置位置模板，然后再将其置于企业中的生产环境中。

**如何手动编辑设置位置模板**

1.  创建设置位置模板（.xml 文件）的本地副本。 UE-V 设置位置模板是 .xml 文件，用于标识应用商店设置值的位置。

2.  使用 XML 编辑器打开 "设置位置" 模板文件。

3.  编辑设置位置模板文件。 所有更改都必须符合 SettingsLocationTempate 中定义的 UE-V 架构文件。 默认情况下，.xsd 文件的副本位于 `\ProgramData\Microsoft\UEV\Templates` 默认位置。

4.  保存设置位置模板文件，然后关闭 "XML 编辑器"。

5.  通过 UE-V 发生器验证修改后的设置位置模板文件。 有关通过 UE-V 生成器进行验证的详细信息，请参阅[通过 Ue-v 生成器验证 Ue-v 设置位置模板](validate-ue-v-settings-location-templates-with-ue-v-generator.md)。

## 相关主题


[使用自定义 UE-V 模板和 UE-V 生成器](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[UE-V 1.0 的操作](operations-for-ue-v-10.md)

 

 




