---
title: 如何添加程序包版本
description: 如何添加程序包版本
author: dansimp
ms.assetid: dbb829c1-e5cb-4a2f-bc17-9a9bb50c671c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a60252e8b43af61ad548df30a93d8fbc9bae0cb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10802961"
---
# 如何添加程序包版本


在应用程序虚拟化服务器管理控制台中，当你 resequence 程序包时，可以使用以下过程将新版本添加到服务器以进行流式处理。

**注意** 使用新版本升级程序包时，可以保留现有版本或将其删除，仅保留最新版本。 你可能希望保留旧版本以实现与旧版文档的兼容性，以便你可以在将新版本提供给所有用户之前对其进行测试。

 

**添加程序包版本**

1.  将新的 SFT 文件复制到应用服务器的内容文件夹。 如果 resequencing 未将更改添加到打开的软件描述符（OSD）、图标（.ICO）或 Sequencer 项目（SPRJ）文件中，则无需复制这些更改。 如果您希望所有文件都显示相同的日期，则可以包含这些文件。

2.  在应用程序虚拟化服务器管理控制台的左窗格中，展开 "**程序包**" 节点。

3.  右键单击要升级的程序包，然后选择 "**添加版本**"。

4.  在 "**添加程序包版本**" 对话框中，在 "**程序包文件的完整路径**" 字段中浏览或键入新应用程序文件的路径名称。 这必须是一个 SFT 文件。

5.  单击“下一步”****。

6.  "**摘要**" 对话框显示文件位置，并提示您将文件复制到该位置（如果尚未执行此操作）。 验证信息后，单击 "**完成**"。

    新版本现已完成，准备好流。

## 相关主题


[如何删除程序包](how-to-delete-a-packageserver.md)

[如何在 Server Management Console 中管理程序包](how-to-manage-packages-in-the-server-management-console.md)

 

 





