---
title: 如何手动添加应用程序
description: 如何手动添加应用程序
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10801280"
---
# 如何手动添加应用程序


将应用程序添加到应用程序虚拟化管理服务器时，建议将其导入。 你可以手动添加应用程序，但你必须提供本部分中所述的有关应用程序的确切详细信息。

**手动添加新的应用程序**

1.  在左窗格中，右键单击 "**应用程序**" 节点，然后选择 "**新建应用程序**"。

2.  在 "**新建应用程序" 向导**中，完成 "**常规信息**" 对话框：

    1.  "**应用程序名称**" —键入希望用户看到的名称。

    2.  **版本**-键入应用程序版本。

    3.  **已启用**-在创建应用程序后，必须选中此框以流式传输应用程序。

    4.  **说明**—键入管理使用的可选说明。

    5.  **OSD 路径**-浏览网络到应用程序的开放式软件描述符（OSD）文件。 此文件必须位于共享网络文件夹中。

    6.  **图标路径**-浏览到应用程序的 .ico 文件。

    7.  **应用程序许可证组**-如果已设置许可证组，则可以通过在下拉列表中选择应用程序来将其分配给该应用程序。

    8.  **服务器组**-如果你有多个 Application Virtualization 服务器，则可以通过在下拉列表中选择应用程序来将其分配给一个应用程序。

3.  单击“下一步”****。

4.  在 "**选择程序包**" 对话框中，选择相关程序包，然后单击 "**下一步**"。

5.  在 "**已发布的快捷方式**" 屏幕上，选择要在客户端计算机上显示应用程序快捷方式的位置的框，然后单击 "**下一步**"。

6.  在 "**文件关联**" 屏幕中，可以向此应用程序添加新的类型文件关联。 若要执行此操作，请单击 "**添加**"，输入扩展名（不带上点），输入说明，然后单击 **"确定"**。

7.  单击“下一步”****。

8.  在 "**访问权限**" 对话框中，单击 "**添加**"。

9.  在 "**添加/编辑用户组**" 对话框中，导航到 "用户" 组。 您也可以通过在相应字段中键入信息来输入域和组。 完成后，单击 **"确定"**。 您可以添加具有相同页面的其他组。

10. 单击“下一步”****。

11. 在 "**摘要**" 屏幕上，您可以查看导入设置。 单击 "**完成**" 以添加应用程序，单击 "**返回**" 以更改信息，或单击 "**取消**"。

## 相关主题


[如何在 Server Management Console 中管理应用程序](how-to-manage-applications-in-the-server-management-console.md)

 

 





