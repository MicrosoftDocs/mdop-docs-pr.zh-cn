---
title: 还原已删除的 GPO
description: 还原已删除的 GPO
author: dansimp
ms.assetid: e6953296-7b7d-4d1e-ad82-d4a23044cdd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2cba097ecd651a91f828901d8115a7020d6da819
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10801807"
---
# 还原已删除的 GPO


高级组策略管理（AGPM）允许审批者从回收站还原已删除的组策略对象（GPO），并将其返回到存档。

必须具有编辑者、审批者或 AGPM 管理员（完全控制）角色的用户帐户或高级组策略管理中的必需权限才能完成此过程。 查看本主题中 "其他注意事项" 中的详细信息。

**还原已删除的 GPO**

1.  在 "**组策略管理" 控制台**树中，单击要在其中管理 gpo 的林和域中的 "**更改控制**"。

2.  在 "**目录**" 选项卡上，单击 "**回收站**" 选项卡以显示已删除的 gpo。

3.  右键单击要还原的 GPO，然后单击 "**还原**"。

4.  键入要在 GPO 的历史记录中显示的注释，然后单击 **"确定"**。

5.  当**进度**窗口指示整个进度完成时，单击 "**关闭**"。 该 GPO 将从 "**回收站**" 选项卡中删除，并显示在 "**受控**" 选项卡上。

**注意** 如果从生产环境中删除了某个 GPO，则将其还原到存档不会自动将其重新部署到生产环境。 若要将 GPO 返回到生产环境，请部署 GPO。 有关信息，请参阅[部署 GPO](deploy-a-gpo.md)。

 

### 其他注意事项

-   默认情况下，你必须是编辑者、审批者或 AGPM 管理员（完全控制）才能执行此过程。 具体而言，您必须具有**列表内容**，并且可以**编辑设置**、**部署 GPO**或删除 gpo 的**gpo**权限。

### 其他参考资料

-   [删除、还原或销毁 GPO](deleting-restoring-or-destroying-a-gpo.md)

 

 





