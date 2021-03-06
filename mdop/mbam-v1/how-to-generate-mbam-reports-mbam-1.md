---
title: 如何生成 MBAM 报告
description: 如何生成 MBAM 报告
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10803586"
---
# 如何生成 MBAM 报告


Microsoft BitLocker 管理和监视（MBAM）生成各种报告以监控 BitLocker 加密的使用情况和合规性。 本主题介绍了如何打开 MBAM 管理网站以及如何生成有关企业合规性、单独计算机、硬件兼容性和密钥恢复活动的 MBAM 报告。 有关 MBAM 报表的详细信息，请参阅[了解 MBAM 报表](understanding-mbam-reports-mbam-1.md)。

**注意** 若要运行报表，您必须是已安装管理和监视服务器功能、合规性和审核数据库以及合规性和审核报告的计算机上的**报表用户**角色的成员。

 

**打开 MBAM 管理网站**

1.  打开 web 浏览器并导航到 MBAM 网站。 网站的默认 URL 是 Microsoft BitLocker 管理和监视服务器的*http:// &lt; computername &gt; * 。

    **注意** 如果 MBAMadministration 网站安装在除端口80之外的其他端口上，则必须在 URL 中指定该端口号。 例如， *http:// &lt; computername &gt; ： &lt; port &gt; *。 如果在安装期间为 MBAMadministration 网站指定了一个主机名，URL 将为*http:// &lt; 主机 &gt; *名。

     

2.  在导航窗格中，单击 "**报表**"。 在主窗格中，单击报表类型的选项卡：**企业合规性报告**、**计算机合规性报告**、**硬件审核报告**或**恢复审核报告**。

    **注意** 历史 MBAM 客户端数据保留在合规性数据库中。 如果计算机丢失或被盗，可能需要这些保留的数据。 运行企业报表时，应使用相应的开始和结束日期将报表的时间范围从一到两周范围范围内，以增加报告数据的准确性。

     

**生成企业合规性报告**

1.  在 MBAMadministration 网站上，单击导航窗格中的 "**报表**"，然后单击 "**企业合规性报告**" 选项卡，为报表选择相应的筛选器。 对于企业合规性报告，你可以设置以下筛选器。

    -   **合规性状态**。 使用此筛选器指定要包括在报表中的合规性状态类型（例如，合规性或不符合）。

    -   **错误状态**。 使用此筛选器指定要包含在报表中的错误状态类型，如 "无错误" 或 "错误"。

2.  单击 "**查看报表**" 以显示指定的报表。

    可以使用多种可用文件格式（如 HTML、Microsoft Word 和 Microsoft Excel）保存报表结果。

    **注意** 企业合规性报告由每6个小时运行的 SQL 作业生成。 因此，第一次尝试查看报表时，您可能会发现某些数据丢失。

     

3.  若要查看计算机合规性报告中有关计算机的信息，请选择计算机名称。

4.  选择计算机名称旁边的加号（+）以查看有关计算机上的卷的信息。

**生成计算机合规性报告**

1.  在 MBAMadministration 网站中，在导航窗格中选择 "**报表**" 节点，然后选择 "**计算机合规性报告**"。 使用 "计算机合规性报告" 搜索**用户名**或**计算机名称**。

2.  单击 "**查看报表**" 以查看计算机报告。

    可使用多种可用文件格式（如 HTML、Microsoft Word 和 Microsoft Excel）保存结果。

3.  若要在计算机合规性报告中显示有关计算机的详细信息，请选择计算机名称。

4.  选择计算机名称旁边的加号（+）以查看有关计算机上的卷的信息。

    **注意** 如果计算机满足 MBAM 策略设置的要求，或者计算机的硬件模型设置为不兼容，MBAM 客户端计算机将视为合规性。 因此，当你查看与计算机相关联的磁盘卷的详细信息时，由于设备的驱动器卷加密状态显示为不符合规则，因此不受硬件兼容性阻止 BitLocker 加密的计算机也会显示为合规。

     

**生成硬件兼容性审核报告**

1.  从 MBAMadministration 网站上，从导航窗格中选择 "**报表**" 节点，然后选择 "**硬件审核报表**"。 为你的硬件审核报告选择相应的筛选器。 硬件审核报告提供以下可用筛选器：

    -   **User （Domain\\User）**。 指定进行更改的用户的姓名。

    -   **更改类型**。 指定要查找的更改类型。

    -   **开始日期**。 指定要报告的日期范围的开始日期部分。

    -   **结束日期**。 指定要报告的日期范围的结束日期部分。

2.  单击 "**查看报表**" 以查看报表。

    可通过多种可用的文件格式（如 HTML、Microsoft Word 和 Microsoft Excel）保存结果。

**生成恢复密钥审核报告**

1.  从 MBAMadministration 网站上，选择 "导航" 窗格中的 "**报表**" 节点，然后选择 "**恢复审核报告**"。 为恢复密钥审核报告选择筛选器。 用于恢复密钥审核的可用筛选器如下所示：

    -   **请求**程序。 指定请求者的用户名。 请求者是帮助台中代表用户访问密钥的人员。

    -   **Requestee**。 指定 requestee 的用户名。 Requestee 是呼叫支持人员以获取恢复密钥的人员。

    -   **请求结果**指定请求结果类型，如：成功或失败。 例如，你可能希望查看失败的键访问尝试。

    -   **键类型**。 指定密钥类型，如：恢复密钥密码或 TPM 密码哈希。

    -   **开始日期**。 指定日期范围的开始日期部分。

    -   **结束日期**。 指定日期范围的结束日期部分。

2.  单击 "**查看报表**" 以显示报表。

    可通过多种可用的文件格式（如 HTML、Microsoft Word 和 Microsoft Excel）保存结果。

## 相关主题


[使用 MBAM 1.0 监视和报告 BitLocker 符合性](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





