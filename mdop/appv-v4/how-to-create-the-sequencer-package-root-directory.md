---
title: 如何创建 Sequencer 程序包根目录
description: 如何创建 Sequencer 程序包根目录
author: dansimp
ms.assetid: 23fe28f1-c284-43ee-b8b7-1dfbed94eea5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5150e87915202794624b6c51510e56454d2c7d36
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10801488"
---
# 如何创建 Sequencer 程序包根目录


程序包 root 目录是运行应用程序-V 排序器文件的计算机上安装了序列化应用程序的文件的目录。 此目录还存在于将对序列化的应用程序进行流式处理的计算机上。 在监视新应用程序的安装之前，应创建程序包根目录。

创建程序包根目录后，即可开始对应用程序进行排序。 有关对新应用程序进行序列化的详细信息，请参阅[如何对应用程序进行](how-to-sequence-an-application.md)排序。

**创建程序包根目录**

1.  若要创建程序包根目录，请在运行 App-v Sequencer 的计算机上，将 Q:\\ 驱动器映射到指定的网络位置。 你指定的位置应该有足够的空间来保存你正在排序的应用程序。

2.  若要创建可用于新虚拟应用程序的目录，请在 Q:\\ 驱动器上创建一个文件夹，然后为其分配一个名称。

    **重要提示** 分配给将保存在程序包根目录中的虚拟应用程序文件的名称应使用8.3 命名格式。 文件名长度不应超过8个字符，并带有三个字符的文件扩展名。

     

## 相关主题


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[如何修改日志目录位置](how-to-modify-the-log-directory-location.md)

[如何修改暂存目录位置](how-to-modify-the-scratch-directory-location.md)

 

 





