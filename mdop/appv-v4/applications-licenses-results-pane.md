---
title: “应用程序许可证结果”窗格
description: “应用程序许可证结果”窗格
author: dansimp
ms.assetid: 8b519715-b2fe-451e-ad9b-e9b73f454961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5a86c22e67e061ec873317c455958536fae75b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10802244"
---
# “应用程序许可证结果”窗格


应用程序虚拟化服务器管理控制台中的**应用程序许可证结果**窗格显示可用的应用程序许可证组和应用程序许可证的列表。

右键单击任何应用程序许可证组以显示包含以下元素的弹出菜单。

<a href="" id="new-unlimited-license"></a>**新的无限通许可证**  
显示 "新建无限制许可证" 向导。 仅当许可证组没有许可证时，此选项才可用。 此向导包含三个页面：

1.  在 "**应用程序许可证组名称**" 字段中输入组名称，在 "**许可证过期警告**" 字段中输入一个值（以分钟为单位）。 （可以输入0到100之间的任何值。）您也可以使用向上键和向下键选择分钟数。

2.  在 "**许可证说明**" 字段中输入简短的描述性文本，然后选中 "**已启用**" 复选框。 或者，您可以使用 "**到期日期**" 字段指定许可证的到期日期。 你可以选择 "默认" 复选框或使用日历实用工具浏览到所需的到期日期。

3.  单击 "**完成**" 以添加新许可证。

<a href="" id="new-concurrent-license"></a>**新的并发许可证**  
显示 "新建并发许可证" 向导。 仅当许可证组没有无限许可证时，此选项才可用。 此向导包含以下页面，与新的无限许可证向导几乎完全相同：

1.  在 "**应用程序许可证组名称**" 字段中输入组名称，在 "**许可证过期警告**" 字段中输入一个值（以分钟为单位）。 （可以输入0到100之间的任何值。）您也可以使用向上键和向下键选择分钟数。

2.  在 "**许可证说明**" 字段中输入简短的描述性文本，然后在 "**并发许可证数量**" 字段中输入一个值。 您也可以使用向上键和向下键来指定并发许可证的数量。 选中 "**已启用**" 复选框以启用许可证。 或者，您可以使用 "**到期日期**" 字段选择许可证的到期日期。 您可以选中该复选框以使用显示的到期日期，也可以使用日历实用工具浏览到所需的到期日期。

3.  单击 "**完成**" 以添加新许可证。

<a href="" id="new-named-license"></a>**新的命名许可证**  
显示 "新建命名的许可证" 向导。 仅当许可证组没有无限许可证时，此选项才可用。 此向导包含以下页面：

1.  在 "**应用程序许可证组名称**" 字段中输入组名称，在 "**许可证过期警告**" 字段中输入一个值（以分钟为单位）。 （可以输入0到100之间的任何值。）您也可以使用向上键和向下键选择分钟数。

2.  在**许可证说明**中输入简短的描述性文本，然后选中 "**已启用**" 复选框。 或者，您可以使用 "**到期日期**" 字段指定许可证的到期日期。 你可以选中该复选框以使用显示的到期日期，或使用日历实用工具浏览到所需的到期日期。

3.  单击 "**添加**"、"**编辑**" 或 "**删除**已命名的用户"。

4.  单击 "**完成**" 以添加新许可证。

<a href="" id="new-window-from-here"></a>**从此处新建窗口**  
打开新的管理控制台，其中将选定的节点作为根节点。

<a href="" id="delete"></a>**删除**  
从列表中删除许可证组。

<a href="" id="rename"></a>**重命名**  
更改应用程序许可证组的名称。

<a href="" id="properties"></a>**属性**  
显示所选应用程序许可证组的 "**属性**" 对话框。 此对话框具有下列选项卡：

-   "**常规**" 选项卡-显示有关许可证组的常规信息。 在此选项卡中，您可以更改 "**许可证过期警告**" 字段中的时间值（以分钟为单位）。 你可以输入0到100之间的任何值。

-   "**应用程序**" 选项卡-显示与许可证组相关联的应用程序的列表。

<a href="" id="help"></a>**帮助**  
显示应用程序虚拟化服务器管理控制台帮助系统。

当 "**结果**" 窗格显示应用程序许可证组时，右键单击 "**结果**" 窗格中除许可证组之外的任何位置，以显示包含以下元素的弹出菜单。

<a href="" id="refresh"></a>**刷新**  
刷新服务器的视图。

<a href="" id="export-list"></a>**导出列表**  
创建一个制表符分隔的文本文件，其中包含 "**结果**" 窗格的内容。 此项显示一个标准的 "**文件保存**" 对话框，您可以在其中指定要创建的文本文件的位置。

<a href="" id="view"></a>**视图**  
更改 "**结果**" 窗格的外观和内容。

<a href="" id="arrange-line-up-icons"></a>**"排列/对齐" 图标**  
更改图标在 "**结果**" 窗格中的显示方式。

<a href="" id="help"></a>**帮助**  
显示应用程序虚拟化服务器管理控制台的帮助系统。

当 "**结果**" 窗格显示许可证时，右键单击任何应用程序许可证以显示包含以下元素的弹出菜单。

<a href="" id="delete"></a>**删除**  
从列表中删除许可证。

<a href="" id="rename"></a>**重命名**  
更改许可证的名称。

<a href="" id="properties"></a>**属性**  
显示所选应用程序许可证的 "**属性**" 对话框。

"**属性**" 对话框的 "**常规**" 选项卡显示有关许可证的信息，并允许您更改 "已启用状态"、"许可证到期日期" 和 "许可证密钥" 信息。

<a href="" id="help"></a>**帮助**  
显示服务器管理控制台帮助系统。

当 "**结果**" 窗格显示许可证时，请右键单击 "**结果**" 窗格中的任意位置（除许可证外），以显示包含以下元素的弹出菜单。

<a href="" id="export-list"></a>**导出列表**  
创建一个制表符分隔的文本文件，其中包含 "**结果**" 窗格的内容。 此项显示一个标准的 "**文件保存**" 对话框，您可以在其中指定要创建的文本文件的位置。

<a href="" id="view"></a>**视图**  
更改 "**结果**" 窗格的外观和内容。

<a href="" id="arrange-line-up-icons"></a>**"排列/对齐" 图标**  
更改图标在 "**结果**" 窗格中的显示方式。

<a href="" id="properties"></a>**属性**  
显示所选许可证的 "**属性**" 对话框。

"**属性**" 对话框的 "**常规**" 选项卡显示有关许可证的信息，并允许您更改 "已启用状态"、"许可证到期日期" 和 "许可证密钥" 信息。

<a href="" id="help"></a>**帮助**  
显示应用程序虚拟化服务器管理控制台的帮助系统。

## 相关主题


[关于应用程序授权](about-application-licensing.md)

[如何在 Server Management Console 中管理应用程序许可证](how-to-manage-application-licenses-in-the-server-management-console.md)

[Server Management Console：“应用程序许可证”节点](server-management-console-application-licenses-node.md)

 

 





