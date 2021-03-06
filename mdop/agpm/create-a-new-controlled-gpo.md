---
title: 创建新的受控 GPO
description: 创建新的受控 GPO
author: dansimp
ms.assetid: b43ce0f4-4519-4278-83c4-c7d5163ddd11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a64e22036bfe99e1d5012d732e3f2e081acdcca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10802879"
---
# 创建新的受控 GPO


通过 "**更改控制**" 节点创建的新组策略对象（gpo）将自动受控制，从而使你能够使用高级组策略管理（AGPM）管理这些对象。

需要具有审批者或 AGPM 管理员（完全控制）角色的用户帐户或高级组策略管理中的必要权限才能完成此过程。 查看本主题中 "其他注意事项" 中的详细信息。

**使用通过 AGPM 管理的更改控制创建新 GPO**

1.  在 "**组策略管理" 控制台**树中，单击要在其中管理 gpo 的林和域中的 "**更改控制**"。

2.  右键单击 "**更改控制**" 节点，然后单击 "**新建受控 GPO**"。

3.  在 "**新建受控 GPO** " 对话框中：

    1.  键入新 GPO 的名称。

    2.  可选：键入要在 GPO 的**历史记录**中显示的新 GPO 的注释。

    3.  要立即将新的 GPO 部署到生产环境，请单击 "**创建 live**"。 若要在不立即部署的情况下创建新的 GPO，请单击 "**脱机创建**"。

    4.  选择要用作新 GPO 的起始点的 GPO 模板。

    5.  单击“确定”****。

4.  当**进度**窗口指示整个进度完成时，单击 "**关闭**"。 新的 GPO 将显示在 "**受控**" 选项卡上的 gpo 列表中。

### 其他注意事项

-   默认情况下，你必须是审批者或 AGPM 管理员（完全控制）才能执行此过程。 具体而言，您必须拥有**列表内容**并为域**创建 GPO**权限。

### 其他参考资料

-   [创建、控制或导入 GPO](creating-controlling-or-importing-a-gpo-approver.md)

 

 





