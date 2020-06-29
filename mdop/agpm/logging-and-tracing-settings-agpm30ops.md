---
title: 记录和跟踪设置
description: 记录和跟踪设置
author: dansimp
ms.assetid: 858b6fbf-65b4-42fa-95a9-69b04e5734d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 078bda16b5fcf968d45e0c4890487471105e8c44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10802679"
---
# <span data-ttu-id="d892e-103">记录和跟踪设置</span><span class="sxs-lookup"><span data-stu-id="d892e-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="d892e-104">通过高级组策略管理（AGPM）的管理模板设置，你可以为已应用了组策略对象（GPO）的 AGPM 服务器和客户集中配置日志记录和跟踪选项。</span><span class="sxs-lookup"><span data-stu-id="d892e-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="d892e-105">编辑 GPO 时，"计算机 Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM" 下提供以下设置。</span><span class="sxs-lookup"><span data-stu-id="d892e-105">The following setting is available under Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<span data-ttu-id="d892e-106">**跟踪文件位置**：</span><span class="sxs-lookup"><span data-stu-id="d892e-106">**Trace file locations**:</span></span>

-   <span data-ttu-id="d892e-107">客户端：%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="d892e-107">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="d892e-108">服务器：%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="d892e-108">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d892e-109">设置</span><span class="sxs-lookup"><span data-stu-id="d892e-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="d892e-110">作用</span><span class="sxs-lookup"><span data-stu-id="d892e-110">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d892e-111">AGPM：配置日志记录</span><span class="sxs-lookup"><span data-stu-id="d892e-111">AGPM: Configure logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d892e-112">通过此策略设置，你可以为 AGPM 启用和配置日志记录。</span><span class="sxs-lookup"><span data-stu-id="d892e-112">This policy setting allows you to turn on and configure logging for AGPM.</span></span> <span data-ttu-id="d892e-113">此设置会影响 AGPM 的客户端和服务器组件。</span><span class="sxs-lookup"><span data-stu-id="d892e-113">This setting affects both client and server components of AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="d892e-114">其他参考资料</span><span class="sxs-lookup"><span data-stu-id="d892e-114">Additional references</span></span>

-   [<span data-ttu-id="d892e-115">“管理模板”文件夹</span><span class="sxs-lookup"><span data-stu-id="d892e-115">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm30ops.md)

 

 





