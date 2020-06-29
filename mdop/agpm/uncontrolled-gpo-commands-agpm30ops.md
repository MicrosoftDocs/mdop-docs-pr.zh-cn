---
title: 不受控 GPO 命令
description: 不受控 GPO 命令
author: dansimp
ms.assetid: 94c07b09-cb96-4ff2-b963-b25f103e73e9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 58177ef902a2f010e43fb5f33ae85f147eea11dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10802487"
---
# <span data-ttu-id="67079-103">不受控 GPO 命令</span><span class="sxs-lookup"><span data-stu-id="67079-103">Uncontrolled GPO Commands</span></span>


<span data-ttu-id="67079-104">"不**受控制**" 选项卡：</span><span class="sxs-lookup"><span data-stu-id="67079-104">The **Uncontrolled** tab:</span></span>

-   <span data-ttu-id="67079-105">显示不受高级组策略管理（AGPM）管理的组策略对象（Gpo）的列表。</span><span class="sxs-lookup"><span data-stu-id="67079-105">Displays a list of Group Policy Objects (GPOs) not managed by Advanced Group Policy Management (AGPM).</span></span>

-   <span data-ttu-id="67079-106">提供快捷菜单，其中包含用于将不受管理的 Gpo 引入到 AGPM 管理的命令以及用于显示 Gpo 的历史记录和报告的命令。</span><span class="sxs-lookup"><span data-stu-id="67079-106">Provides a shortcut menu with commands for bringing uncontrolled GPOs under the management of AGPM and for displaying the history and reports for GPOs.</span></span>

-   <span data-ttu-id="67079-107">显示具有访问选定 GPO 的权限的组和用户的列表。</span><span class="sxs-lookup"><span data-stu-id="67079-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="67079-108">右键单击此选项卡上的 "**组策略对象**" 列表，将显示快捷菜单，包括以下任何适用选项。</span><span class="sxs-lookup"><span data-stu-id="67079-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="67079-109">控件和历史记录</span><span class="sxs-lookup"><span data-stu-id="67079-109">Control and history</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="67079-110">命令</span><span class="sxs-lookup"><span data-stu-id="67079-110">Command</span></span></th>
<th align="left"><span data-ttu-id="67079-111">作用</span><span class="sxs-lookup"><span data-stu-id="67079-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="67079-112">历史记录</span><span class="sxs-lookup"><span data-stu-id="67079-112">History</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="67079-113">打开一个窗口，列出存档中保存的选定 GPO 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="67079-113">Open a window listing all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="67079-114">从历史记录中，你可以获取 GPO 中的设置报告、比较 GPO 的两个版本、将 GPO 与模板进行比较或回退到 GPO 的早期版本。</span><span class="sxs-lookup"><span data-stu-id="67079-114">From the history, you can obtain a report of the settings within a GPO, compare two versions of a GPO, compare a GPO to a template, or roll back to a previous version of a GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="67079-115">控件</span><span class="sxs-lookup"><span data-stu-id="67079-115">Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="67079-116">在 AGPM 的 "更改控制管理" 下，将所选的非受控 GPO 置入。</span><span class="sxs-lookup"><span data-stu-id="67079-116">Bring the selected uncontrolled GPO under the change control management of AGPM.</span></span> <span data-ttu-id="67079-117">如果你没有控制 GPO 的权限，系统将提示你提交请求。</span><span class="sxs-lookup"><span data-stu-id="67079-117">If you do not have permission to control a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="67079-118">另存为模板</span><span class="sxs-lookup"><span data-stu-id="67079-118">Save as Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="67079-119">基于所选 GPO 的设置创建新模板。</span><span class="sxs-lookup"><span data-stu-id="67079-119">Create a new template based on the settings of the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="67079-120">报告</span><span class="sxs-lookup"><span data-stu-id="67079-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="67079-121">命令</span><span class="sxs-lookup"><span data-stu-id="67079-121">Command</span></span></th>
<th align="left"><span data-ttu-id="67079-122">作用</span><span class="sxs-lookup"><span data-stu-id="67079-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="67079-123">设置</span><span class="sxs-lookup"><span data-stu-id="67079-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="67079-124">生成用于显示选定 GPO 中的设置的基于 HTML 的报表或基于 XML 的报表。</span><span class="sxs-lookup"><span data-stu-id="67079-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="67079-125">不同之处</span><span class="sxs-lookup"><span data-stu-id="67079-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="67079-126">生成用于比较两个选定 Gpo 或所选 GPO 和模板内的设置的基于 HTML 或基于 XML 的报表。</span><span class="sxs-lookup"><span data-stu-id="67079-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="67079-127">杂项</span><span class="sxs-lookup"><span data-stu-id="67079-127">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="67079-128">命令</span><span class="sxs-lookup"><span data-stu-id="67079-128">Command</span></span></th>
<th align="left"><span data-ttu-id="67079-129">作用</span><span class="sxs-lookup"><span data-stu-id="67079-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="67079-130">刷新</span><span class="sxs-lookup"><span data-stu-id="67079-130">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="67079-131">更新组策略管理控制台（GPMC）的显示以合并任何更改。</span><span class="sxs-lookup"><span data-stu-id="67079-131">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="67079-132">在刷新显示之前，某些更改不可见。</span><span class="sxs-lookup"><span data-stu-id="67079-132">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="67079-133">帮助</span><span class="sxs-lookup"><span data-stu-id="67079-133">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="67079-134">显示 AGPM 的帮助。</span><span class="sxs-lookup"><span data-stu-id="67079-134">Display help for AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="67079-135">其他参考资料</span><span class="sxs-lookup"><span data-stu-id="67079-135">Additional references</span></span>

-   [<span data-ttu-id="67079-136">“内容”选项卡</span><span class="sxs-lookup"><span data-stu-id="67079-136">Contents Tab</span></span>](contents-tab-agpm30ops.md)

-   [<span data-ttu-id="67079-137">执行编辑者任务</span><span class="sxs-lookup"><span data-stu-id="67079-137">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="67079-138">执行审批者任务</span><span class="sxs-lookup"><span data-stu-id="67079-138">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="67079-139">执行审阅者任务</span><span class="sxs-lookup"><span data-stu-id="67079-139">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 




