---
title: 委派针对存档中单独 GPO 的访问权限
description: 委派针对存档中单独 GPO 的访问权限
author: dansimp
ms.assetid: 284d2aa2-7c10-4ffa-8978-bbe30867c1c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9da2a699568f961d030b05a966b76e08aef3aec8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10802856"
---
# 委派针对存档中单独 GPO 的访问权限


作为 AGPM 管理员（完全控制），你可以委派存档中受控制的组策略对象（GPO）的管理，以便所选组和编辑可以对其进行编辑，审阅者可以查看它，并且审批者可以批准它。

具有 AGPM 管理员（完全控制）角色的用户帐户、创建 GPO 的审批者的用户帐户，或者需要高级组策略管理（AGPM）中具有必要权限的用户帐户才能完成此过程。 查看本主题中 "其他注意事项" 中的详细信息。

**委派受控 GPO 的管理**

1.  在 "**组策略管理" 控制台**树中，单击要在其中管理 gpo 的林和域中的 "**更改控制**"。

2.  在 "详细信息" 窗格中的 "**目录**" 选项卡上，单击 "**受控**" 选项卡以显示 "受控 gpo"，然后单击要委派的 GPO：

    1.  若要为用户或组添加访问权限，请单击 "**添加**" 按钮，选择用户或组，然后单击 **"确定"**。 在 "**添加组" 或 "用户**" 对话框中，选择一个角色，然后单击 **"确定"**。

    2.  若要删除用户或组的访问权限，请选择该用户或组，然后单击 "**删除**" 按钮。

        **注意** 如果用户或组继承了域范围的访问权限，则 "**删除**" 按钮不可用。 可以在 "**域委派**" 选项卡上修改域范围的访问权限。

         

    3.  若要修改委派给用户或组的角色和权限，请单击 "**高级**" 按钮。 在 "**权限**" 对话框中，选择 "用户" 或 "组"，选中要分配给该用户或组的每个角色的复选框，然后单击 **"确定"**。

        **注意** 编辑者和审批者包括审阅者权限。

         

### 其他注意事项

-   默认情况下，你必须是创建或控制 GPO 的审批者或 AGPM 管理员（完全控制）才能执行此过程。 具体而言，您必须具有域的 "**列表内容**" 权限和 "修改 GPO 的**安全**权限"。

-   若要委派使用 AGPM 的组策略管理员的读取访问权限，必须授予它们**列表内容**和**读取设置**权限。 这使他们能够在 AGPM 的 "**目录**" 选项卡上查看 gpo。 其他权限必须明确委派。

-   对于已部署的 GPO 副本，编辑器必须具有 "**读取**" 权限，才能完全使用组策略软件安装。

-   组策略创建者所有者组的成员身份应受到限制，soit 不会用于绕过对 Gpo 的访问的 AGPM 管理。 （在**组策略管理控制台**中，单击要在其中管理 gpo 的林和域中的 "**组策略对象**"，单击 "**委派**"，然后配置设置以满足组织的需要。）

### 其他参考资料

-   [管理存档](managing-the-archive-agpm40.md)

 

 




