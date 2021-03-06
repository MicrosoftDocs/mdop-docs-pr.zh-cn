---
title: 如何对新的加载项或插件应用程序进行排序 (App-V 4.6 SP1)
description: 如何对新的加载项或插件应用程序进行排序 (App-V 4.6 SP1)
author: dansimp
ms.assetid: 2c018215-66e5-4301-8481-159891a6b35b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5c5bc1e96ead819459cda3879127ebdaf94f0ee7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10801124"
---
# 如何对新的加载项或插件应用程序进行排序 (App-V 4.6 SP1)


通过使用应用程序虚拟化（App-v） Sequencer，使用以下过程创建新的加载项或插件虚拟应用程序包。 加载项或插件应用程序是扩展应用程序功能的应用程序，例如 Microsoft Excel 的插件。 有关可进行序列化的应用程序类型的详细信息，请参阅[如何确定要序列的应用程序类型（app-v 4.6 SP1）](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)。

**重要提示**  
在执行以下过程之前，请在运行 sequencer 的计算机上本地安装父应用程序。 例如，如果要为 Microsoft Excel 的插件进行排序，请在运行 sequencer 的计算机上本地安装 Microsoft Excel。 还在目标计算机上安装应用程序的同一目录中安装父应用程序。 如果要对现有虚拟应用程序包使用插件或加载项，请在创建父虚拟应用程序包时使用的同一虚拟应用程序驱动器上安装该应用程序。



你还可以将现有虚拟应用程序包用作父应用程序。 若要使用现有虚拟应用程序包，请在对新加载项或插件进行排序之前使用以下过程。

1.  若要启动 app-v 排序器，请在运行 app-v 排序器的计算机上，单击 "**启动**  /  **所有程序**  /  **microsoft application virtualization**  /  **microsoft application virtualization Sequencer**"。

2.  若要将现有程序包扩展到运行 sequencer 的计算机，请单击 "**工具**" 将 "  /  **包展开到本地系统**"。

3.  通过浏览找到并选择要展开的程序包（**sprj**文件），然后单击 "**打开**"。 继续执行以下过程。

**对新加载项或插件应用程序进行排序**

1.  若要启动 app-v 排序器，请在运行 app-v 排序器的计算机上，单击 "**启动**  /  **所有程序**  /  **microsoft application virtualization**  /  **microsoft application virtualization Sequencer**"。

2.  若要启动 "**创建新程序包" 向导**，请单击 "**创建新的虚拟应用程序包**"。 若要创建程序包，请选择 "**创建程序包（默认）**"，然后单击 "**下一步**"。

3.  在 "**准备计算机**" 页面上，查看可能导致程序包创建失败的问题，或者查看程序包中是否包含不必要的数据。 我们强烈建议您先解决所有潜在问题，然后再继续。 修复冲突后，若要更新显示的信息，请单击 "**刷新**"。 解决所有潜在问题后，单击 "**下一步**"。

    **重要提示**  
    如果需要禁用病毒扫描软件，请扫描运行 sequencer 的计算机，以确保不会向程序包添加不需要的或恶意的文件。



4.  在 "**应用程序类型**" 页面上，选择 "加载项"**或 "插件**"，然后单击 "**下一步**"。

    有关可进行序列化的应用程序类型的详细信息，请参阅[如何确定要序列化的应用程序类型（app-v 4.6 SP1）](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)。

5.  在 "**选择安装程序**" 页面上，单击 "**浏览**" 并为加载项或插件指定安装文件。 如果应用程序没有关联的安装程序文件，并且你计划手动运行所有安装步骤，请选中 "**选择此选项以执行自定义安装**" 复选框，然后单击 "**下一步**"。

6.  在 "**选择主页**" 页面上，单击 "**浏览**" 并指定父应用程序。

    **重要提示**  
    如果你正在安装的加载项或插件所支持的父应用程序尚未在本地安装，请在此处停止并在运行 sequencer 的计算机上安装应用程序。 例如， **Excel.exe**程序文件必须在本地安装 Microsoft Excel 插件。



~~~
Click **Next**.
~~~

7. 在 "**程序包名称**" 页面上，指定将与程序包关联的名称。 使用有助于标识将添加到程序包的应用程序用途和版本的名称。 程序包名称还将显示在 App-v 管理控制台中。 **安装位置**显示应用程序虚拟化路径，应用程序虚拟化路径将安装在该应用程序中。 若要编辑此位置，请选择 "**编辑（高级）**"。

   **重要提示**  
   编辑应用程序虚拟化路径是一种高级配置任务。 你应该完全理解更改路径的含义。 对于大多数应用程序，我们建议默认路径。



~~~
Click **Next**.
~~~

8. 在 "**安装**" 页面上，当 sequencer 和应用程序安装准备就绪时，请安装插件或加载项应用程序，以便排序器可以监视安装过程。 使用应用程序的安装过程执行安装。 如果必须在安装过程中运行其他安装文件，请单击 "**运行**"，然后找到并运行其他安装文件。 完成安装后，选择 "**我已完成安装**"，然后单击 "**下一步**"。

9. 在 "**安装报告**" 页面上，您可以查看刚刚排序的虚拟应用程序包的相关信息。 有关**其他信息**中显示的信息的更多详细说明，请双击该事件。 查看信息后，单击 "**下一步**"。

10. 在 "**自定义**" 页面上，如果已完成安装和配置虚拟应用程序，请选择 "**立即停止**"，然后跳到此过程的步骤14。 如果要自定义下表中的任何项目，请选择 "**自定义**"。

    -   编辑与应用程序相关联的文件类型关联。

    -   准备用于流式处理的虚拟包。 流改进了在目标计算机上运行虚拟应用程序包时的体验。

    -   指定可以运行此程序包的操作系统。

    单击“下一步”****。

11. 在 "**编辑快捷方式**" 页面上，你可以选择配置将与程序包中的各种应用程序关联的文件类型关联（FTA）。 若要创建新的 FTA，请在左窗格中，选择并展开要自定义的应用程序，然后单击 "**添加**"。 在 "**添加文件类型关联**" 对话框中，为新的 FTA 提供必要的信息。 在 "应用程序" 下，选择 "**快捷方式**" 以查看与应用程序相关联的快捷方式信息。 在 "**位置**" 窗格中，您可以查看图标文件信息。 若要编辑现有 FTA，请单击 "**编辑**"。 若要删除 FTA，请选择 "FTA"，然后单击 "**删除**"。 单击“下一步”****。

12. 在 "**流**" 页面上，运行每个程序，以便可以在目标计算机上对其进行优化和更高效地运行。 运行所有应用程序可能需要几分钟的时间。 在所有应用程序运行后，关闭每个应用程序，然后单击 "**下一步**"。

   **注意**  
   如果要在此步骤中停止应用程序的加载，请在 "**应用程序启动**" 对话框中，单击 "**停止**"，然后选择其中一个复选框、"**停止所有应用程序**" 或 "**停止此应用程序**"。



13. 在 "**目标操作系统**" 页面上，指定可运行此程序包的操作系统。 若要在你的环境中启用所有支持的操作系统以运行此程序包，请选中 "**允许此程序包在任何操作系统上运行**" 复选框。 若要将此程序包配置为仅在特定操作系统上运行，请选中 "**仅允许此程序包在下列操作系统上运行**" 复选框，然后选择可以运行此程序包的操作系统。 单击“下一步”****。

14. 在 "**创建程序包**" 页面上，若要在不保存的情况下修改程序包，请选择 **"继续使用程序包编辑器修改程序包而不**保存" 复选框。 选择此选项将在 Sequencer 控制台中打开程序包，以便你可以在保存包之前对其进行修改。 单击“下一步”****。

   若要立即保存程序包，请选中 "**立即保存程序包**" 默认值。 （可选）选择 "**注释**" 以添加将与程序包相关联的注释。 对于标识版本以及有关程序包的其他信息，评论非常有用。 还会显示默认**保存位置**。 若要更改默认位置，请单击 "**浏览**" 并指定新位置。 将显示未压缩的程序包大小。 如果程序包大小超过 4 GB （未压缩），并且你打算将程序包流式传输到目标计算机，则必须选择 "**压缩程序包**"。 单击“创建”****。

15. 在 "**完成**" 页面上，在查看 "**成功的虚拟应用程序包" 报表**窗格中显示的信息后，单击 "**关闭**"。 "**成功的虚拟应用程序包报告**" 窗格中显示的信息也可在此过程的步骤14中指定的目录中提供，该目录位于名为**Reports.xml**的文件中。

   程序包现在在 sequencer 中可用。 单击 "**编辑 \ [包名称 \]** " 以编辑程序包属性。 有关修改程序包的详细信息，请参阅[如何修改现有虚拟应用程序包（app-v 4.6 SP1）](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)。

   **重要提示**  
   成功创建虚拟应用程序包后，不能在运行 sequencer 的计算机上运行虚拟应用程序包。



## 相关主题


[Application Virtualization Sequencer 的任务 (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[如何确定要序列化的应用程序类型（App-v 4.6 SP1）](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









