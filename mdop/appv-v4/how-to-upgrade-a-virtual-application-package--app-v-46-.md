---
title: 如何升级虚拟应用程序包 (App-V 4.6)
description: 如何升级虚拟应用程序包 (App-V 4.6)
author: dansimp
ms.assetid: 3566227e-f3dc-4c32-af1f-e0211588118c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac722dc0e9ce1650f53d8dd22db5428d33cfcf13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10801024"
---
# 如何升级虚拟应用程序包 (App-V 4.6)


使用以下过程，通过使用应用程序虚拟化（App-v） Sequencer 升级现有虚拟应用程序。 你还可以使用 App-v Sequencer 控制台对现有虚拟应用程序进行更改，但不执行升级，但不能通过使用此方法对虚拟应用程序的文件系统进行修改，因为 App-v Sequencer 不会实际解码关联的 sft 文件。 有关编辑现有程序包的详细信息，请参阅[如何修改虚拟应用程序包（app-v 4.6）](how-to-modify-a-virtual-application-package--app-v-46-.md)。

**升级现有虚拟应用程序**

1.  若要启动 app-v sequencer 控制台，请在运行 app-v 排序器的计算机上，选择 "**开始**  /  **程序**  /  **microsoft application virtualization**  /  **microsoft application virtualization Sequencer**"。

2.  若要打开现有虚拟应用程序包并启动**顺序向导**，请选择 "**升级程序包**"。 找到要升级的程序包，然后单击 "**打开**"。 在 "**浏览文件夹**" 对话框中，指定将放置程序包升级版本的位置。 指定的此位置必须位于指定为应用程序虚拟化驱动器（通常是 Q:\\ 驱动器）的驱动器上。 若要创建新文件夹，请选择 "创建**新文件夹**"。

    **警告** 必须指定现有虚拟应用程序的根文件夹。 不要手动创建子文件夹，否则升级将失败。

     

3.  在 "**程序包信息**" 页面上，指定将分配给更新的程序包的**程序包名称**。 要生成关联的 Windows Installer 文件，需要程序包名称。 你还应添加一个可选注释，该注释将分配给程序包并提供有关虚拟应用程序的详细信息（例如版本号）。 要显示 "**高级选项**" 页面，请选择 "**显示高级监视选项**"，然后单击 "**下一步**"。否则，请继续执行步骤5。

4.  在 "**高级选项**" 页面上，若要允许 microsoft 更新按顺序更新应用程序，请选择 "**允许 microsoft 更新在监视期间运行**"。 如果选择此选项，将允许在监视阶段中安装 Microsoft 更新，你需要接受相关更新才能安装这些更新。 若要重新映射受支持的动态链接库（.dll）文件，以便它们使用 RAM 的连续空间，请选择 "**变基 dll**"。 选择此选项可以保留内存并帮助提高性能。 单击“下一步”****。

5.  在 "**监视器安装**" 页面上，当你准备好更新应用程序时，单击 "**开始监视**"。

    应用了应用程序的更新后，单击 "**停止监视**"。 单击“下一步”****。

6.  在 "**配置应用程序**" 页面上，如有必要，请配置将与虚拟应用程序关联的快捷方式和文件类型关联。 若要添加新的文件类型关联或快捷方式，请单击 "**添加**"，然后在 "**添加应用程序**" 对话框中，指定新元素。 若要删除现有快捷方式或文件类型关联，请单击 "**删除**"。 若要编辑现有元素，请选择要修改的元素，然后单击 "**编辑**"。 在 "**编辑应用程序**" 对话框中指定配置。 单击 **“保存”**。 单击“下一步”****。

7.  在 "**启动应用程序**" 页面上，若要启动应用程序以确保程序包已正确安装且已针对流式处理进行了优化，请选择程序包，然后单击 "**启动**"。 此步骤可用于配置应用程序最初在目标计算机上运行的方式，以及在将程序包提供给 App-v 客户端之前接受任何关联的许可协议。 如果有多个应用程序与此程序包关联，则可以选择 "**全部启动**" 以打开所有应用程序。 若要对程序包进行排序，请单击 "**下一步**"。

8.  若要关闭排序向导，请单击 "**完成**"。 若要保存已更新的程序包，请在 Sequencer 控制台中选择 "**文件**  /  **保存**"。

    如果你计划使用 Windows Installer 文件（.msi）部署更新的程序包，则必须创建新程序包，如下所示：在 Sequencer 控制台中，选择 "**工具**  /  **创建 msi**"。 将创建新的 Windows Installer 文件，并将其保存在保存已更新虚拟应用程序包的目录中。

## 相关主题


[如何对新应用程序进行排序 (App-V 4.6)](how-to-sequence-a-new-application--app-v-46-.md)

 

 





