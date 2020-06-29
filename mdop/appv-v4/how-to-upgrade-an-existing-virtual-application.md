---
title: 如何升级现有的虚拟应用程序
description: 如何升级现有的虚拟应用程序
author: dansimp
ms.assetid: ec531576-2423-4c2c-9b9f-da74174a6858
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 71fb096c103a0bcb9913d4eea33b1259a33a54ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798973"
---
# 如何升级现有的虚拟应用程序


你可以使用应用程序虚拟化（App-v） Sequencer 将现有虚拟应用程序升级到新版本。 升级过程类似于创建新的虚拟应用程序。 必须打开现有虚拟应用程序进行升级，进行必要的更新，然后将已更新的虚拟应用程序保存到程序包根目录中的新位置。

你还可以使用 App-v Sequencer 控制台对现有虚拟应用程序进行更改，而无需执行升级。 但是，不能通过使用此方法对虚拟应用程序的文件系统进行修改，因为 App-v 排序器不会实际解码关联的 sft 文件。 例如，你可以通过选择 "**文件**" 菜单上的 "**打开**"，在 app-v Sequencer 控制台中打开现有虚拟应用程序。 你可以更新**程序包名称**和关联的**注释**，并且可以对虚拟文件系统和虚拟注册表进行更改。 您也可以创建一个 Windows 安装程序文件。

使用以下过程升级现有虚拟应用程序。

**升级现有虚拟应用程序**

1.  若要启动 app-v sequencer 控制台，请在运行 app-v 排序器的计算机上，选择 "**开始** / **程序** / **microsoft application virtualization** / **microsoft application virtualization Sequencer**"。

2.  若要打开现有虚拟应用程序，请在 app-v 控制台中，选择 "**文件** / **打开" 以进行程序包升级**。 使用 "**打开 For 程序包升级**" 对话框找到要为升级打开的关联 SPRJ 文件。

3.  若要指定程序包的解码位置，请单击 "**浏览文件夹**" 并指定 Q:\\。 这是将根据关联的 SFT 文件中的指定创建程序包根目录的位置。 当你创建程序包的更新版本时，它将使用目录名称的顺序添加来表示，例如，"**.1**" 将添加到 Q:\\ 驱动器上的目录名称中。

4.  若要打开排序向导，请选择 "**工具** / **序列化向导**"。 在 "**程序包信息**" 页面上，选择指定新的**程序包名称**，并添加将与已更新的虚拟应用程序关联的可选注释。 单击“下一步”****。

5.  在 "**监视器安装**" 页面上，要开始监视新安装，请单击 "**开始监视**"。 虚拟环境完成加载后，安装应用程序的更新版本，或将更新应用于现有应用程序。 完成虚拟应用程序的更新后，单击 "**停止监视**"，然后单击 "**下一步**"。

6.  在 "**要映射到虚拟文件系统（vfs）的其他文件**" 页面上，若要指定要添加到虚拟文件系统（vfs）的其他文件，请单击 "**添加**"。 通过浏览找到要添加的文件，然后单击 "**打开**"。 若要清除已添加的现有文件，请单击 "**重置**"，然后单击 "**下一步**"。

7.  在 "**配置应用程序**" 页面上，配置将与已更新的虚拟应用程序关联的快捷方式和文件类型关联。 选择要更新的元素，然后单击 "**编辑位置**"。 在 "**快捷方式位置**" 对话框中指定配置，然后单击 "**下一步**"。

8.  在 "**启动应用程序**" 页面上，若要启动应用程序以确保程序包针对流进行优化，请选择程序包，然后单击 "**启动**"。 此步骤可用于配置应用程序最初在目标计算机上运行的方式，以及在将程序包提供给客户之前接受任何关联的许可协议。 如果有多个应用程序与此程序包关联，则可以选择 "**全部启动**" 以打开所有应用程序。 若要对新版本的虚拟应用程序进行排序，请单击 "**下一步**"。

9.  若要完成并关闭排序向导，请在 "**序列包**" 页面上，单击 "**完成**"。

10. 成功更新虚拟应用程序后，若要保存程序包，请在 App-v Sequencer 控制台中的 "**文件**" 菜单上，选择 "**保存**"。 可以在步骤3中指定的目录中访问虚拟应用程序。

## 相关主题


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[如何使用命令行升级虚拟应用程序](how-to-upgrade-a-virtual-application-by-using-the-command-line.md)

 

 




