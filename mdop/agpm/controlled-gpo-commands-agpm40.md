---
title: 受控 GPO 命令
description: 受控 GPO 命令
author: dansimp
ms.assetid: 370d3db9-4efc-4799-983d-e29ba5f32b07
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 65e9d06beb4c36762e845e452bab497a8d3da747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10802888"
---
# 受控 GPO 命令


"**受控**" 选项卡：

-   显示由高级组策略管理（AGPM）管理的组策略对象（Gpo）的列表。

-   提供快捷菜单，其中包含用于管理 Gpo 的命令和用于显示 Gpo 的历史记录和报告的命令。

-   显示具有访问选定 GPO 的权限的组和用户的列表。

右键单击此选项卡上的 "**组策略对象**" 列表，显示快捷菜单。 此菜单包含以下任何适用选项。

## 控件和历史记录


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">命令</th>
<th align="left">作用</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>新的受控 GPO</strong></p></td>
<td align="left"><p>通过 AGPM 管理更改控制来创建新的 GPO，并将其部署到域的生产环境中。 如果你没有创建 GPO 的权限，系统将提示你提交请求。 （如果右键单击 <strong> 时未选择任何 GPO，则显示此选项组策略对象 </strong> 列表。）</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>历史记录</strong></p></td>
<td align="left"><p>打开一个窗口，列出存档中保存的选定 GPO 的所有版本。 从历史记录中，你可以获取 GPO 中的设置报告、比较 GPO 的两个版本、将 GPO 与模板进行比较或回退到早期版本的 GPO。</p></td>
</tr>
</tbody>
</table>

 

## 报告


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">命令</th>
<th align="left">作用</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>设置</strong></p></td>
<td align="left"><p>生成基于 HTML 或基于 XML 的报表，显示所选 GPO 中的设置，或显示从组织单位到 GPO 最近控制、导入或签入时的选定 GPO 的链接。</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>不同之处</strong></p></td>
<td align="left"><p>生成用于比较两个选定 Gpo 或所选 GPO 和模板内的设置的基于 HTML 或基于 XML 的报表。</p></td>
</tr>
</tbody>
</table>

 

## 编辑


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">命令</th>
<th align="left">作用</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>编辑</strong></p></td>
<td align="left"><p>打开 <strong> 组策略管理编辑器 </strong> 窗口，更改所选 GPO。</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>退房</strong></p></td>
<td align="left"><p>从存档中获取所选 GPO 的副本，以便脱机编辑，并禁止任何其他人编辑 GPO，直到将其签回存档。 签出可由 AGPM 管理员（完全控制）替代。</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>登记</strong></p></td>
<td align="left"><p>将所选 GPO 的已编辑版本签入存档，以便其他授权的编辑人员可以进行更改，或者审批者可以将 GPO 部署到域的生产环境。</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>撤消签出</strong></p></td>
<td align="left"><p>将已签出的 GPO 返回到存档，不进行任何更改。</p></td>
</tr>
</tbody>
</table>

 

## 版本管理


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">命令</th>
<th align="left">作用</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>从生产导入</strong></p></td>
<td align="left"><p>对于选定的 GPO，将域的生产环境中的版本复制到存档。</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>从文件导入</strong></p></td>
<td align="left"><p>将所选的已签出 GPO 的策略设置替换为 GPO 备份文件中的 GPO。</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>删除</strong></p></td>
<td align="left"><p>将所选 GPO 移动到回收站，并指示是否在生产中保留已部署的版本（如果存在），或者删除已部署的版本以及存档中的版本。 如果你没有删除 GPO 的权限，系统将提示你提交请求。</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>部署</strong></p></td>
<td align="left"><p>将已签入存档的选定 GPO 移动到域的生产环境中。 此操作将使其在网络上处于活动状态，并覆盖以前活动版本的 GPO （如果存在）。 如果你没有部署 GPO 的权限，系统将提示你提交请求。</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>导出到</strong></p></td>
<td align="left"><p>将所选 GPO 保存到备份文件，以便可以将其复制到其他域。</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>标签</strong></p></td>
<td align="left"><p>将所选 GPO 标记为描述性标签（如 " &quot; 已知正常" &quot; ），并使用注释保留记录。 标签显示在 " <strong> 状态" </strong> 列中，注释显示在 <strong> </strong> " <strong> 历史记录" 窗口 </strong> 的 "备注" 列中。 它们帮助你识别 GPO 的早期版本，以便你可以在出现问题时回滚。</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>重命名</strong></p></td>
<td align="left"><p>更改所选 GPO 的名称。 如果 GPO 已部署，则重新部署 GPO 时，将在域的生产环境中更新该名称。</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>另存为模板</strong></p></td>
<td align="left"><p>基于所选 GPO 的设置创建新模板。</p></td>
</tr>
</tbody>
</table>

 

## 杂项


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">命令</th>
<th align="left">作用</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>刷新</strong></p></td>
<td align="left"><p>更新组策略管理控制台（GPMC）的显示以合并任何更改。 在刷新显示之前，某些更改不可见。</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>帮助</strong></p></td>
<td align="left"><p>显示 AGPM 的帮助。</p></td>
</tr>
</tbody>
</table>

 

### 其他参考资料

-   [“内容”选项卡](contents-tab-agpm40.md)

-   [执行编辑者任务](performing-editor-tasks-agpm40.md)

-   [执行审批者任务](performing-approver-tasks-agpm40.md)

-   [执行审阅者任务](performing-reviewer-tasks-agpm40.md)

 

 





