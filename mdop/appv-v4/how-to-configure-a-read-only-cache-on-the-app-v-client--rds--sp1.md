---
title: 如何在 App-V Client (RDS) 上配置只读缓存
description: 如何在 App-V Client (RDS) 上配置只读缓存
author: dansimp
ms.assetid: b6607fe2-6f92-4567-99f1-d8e3c8a591e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a44844ae9ffc3497151be7713f6a43fda0ccd8fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/26/2020
ms.locfileid: "10801620"
---
# 如何在 App-V Client (RDS) 上配置只读缓存


**重要提示** 必须运行 App-v 4.6、SP1 才能使用此过程。

 

你可以通过使用由所有用户所需的所有应用程序填充的共享缓存来部署 app-v 客户端。 然后，将 App-v 远程桌面服务（RDS）客户端配置为使用同一缓存文件。 用户通过使用 App-v 发布过程向用户授予对特定应用程序的访问权限。 由于缓存已预加载了所有应用程序，因此当用户启动应用程序时，不会发生流。 但是，用于预填充缓存的程序包必须放置在支持实时流协议（RTSP）流的 app-v 服务器上，并且授予对 App-v 客户端的访问权限。 如果使用 App-v 管理服务器发布应用程序，则可以使用它来提供此流函数。

**注意** 这些过程中概述的详细信息仅用作示例。 你可以使用不同的方法来完成整个过程。

 

## 在 RDS 方案中部署 app-v 客户端


部署过程由四个主要任务组成：

-   创建和填充主共享缓存文件

-   将共享缓存文件复制到服务器存储

-   配置 App-v 客户端软件

-   在初始部署后管理共享缓存文件的更新部署周期

这些任务需要仔细规划。 我们建议你为你的组织准备并记录可重复执行的流程。 这对于主共享缓存文件的准备和部署尤其重要，并且对于应用程序更新的持续管理，每个更新都需要更新到主共享缓存。 使用以下过程完成这些主要任务。

**注意** 虽然你可以使用多种不同的方法发布应用程序，但以下过程基于你使用的 app-v 管理服务器进行发布。

 

**为初始部署配置只读缓存**

1. 设置和配置 app-v 管理服务器，以提供用户身份验证和发布支持。

2. 将此管理服务器的内容文件夹填充给所有用户所需的所有应用程序包。

3. 设置已安装 App-v 客户端的暂存计算机。 使用具有对所有应用程序的访问权限的帐户登录到暂存计算机，以便将整个应用程序集发布到计算机，然后将应用程序流式传输到缓存，以便完全加载这些应用程序。

   **重要提示**  
   暂存计算机必须使用与应用 V 客户端将运行的 Vm 所使用的相同操作系统类型和系统体系结构。

     

4. 在安全模式下重新启动暂存计算机以确保驱动程序未启动，因为这会锁定缓存文件。

   **注意**  
   或者，您可以停止和禁用应用程序虚拟化服务，然后重新启动计算机。 复制文件后，请记住启用并再次启动服务。

     

5. 将 Sftfs 缓存文件复制到 SAN，其中所有 RDS 服务器都可以访问它，例如在共享文件夹中。 将组的 "文件夹访问权限" 设置为 "对所有人只读"，并对将管理缓存文件更新的管理员拥有 "完全控制"。 可以从注册表中获取缓存文件的位置 AppFS\\FileName。

   **重要提示**  
   你必须将 FSD 文件放在具有等于本地附加的存储性能（例如 SAN）的响应性和可靠性的位置。

     

6. 在每个 RDS 服务器上安装 app-v RDS 客户端，然后将其配置为使用只读缓存，方法是将以下注册表项值添加到客户端上的 AppFS 项。 AppFS 键位于32位计算机的 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS 中，64位计算机的 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS。

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">项</th>
   <th align="left">类型</th>
   <th align="left">值</th>
   <th align="left">用途</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>FileName</p></td>
   <td align="left"><p>字符串</p></td>
   <td align="left"><p>FSD 的路径</p></td>
   <td align="left"><p>指定共享缓存文件的路径，例如 \RDSServername\Sharefolder\SFTFS。FSD （必需）。</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReadOnlyFSD</p></td>
   <td align="left"><p>DWORD</p></td>
   <td align="left"><p>raid-1</p></td>
   <td align="left"><p>将客户端配置为以只读模式运行。 这可确保客户端不会尝试将更新传输到程序包缓存。 （必需）</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ErrorLogLocation</p></td>
   <td align="left"><p>字符串</p></td>
   <td align="left"><p>错误日志（.etl）文件的路径</p></td>
   <td align="left"><p>用于指定错误日志路径的条目。 建议您使用. 使用本地路径，如 C:\Logs\Sftfs.etl）。</p></td>
   </tr>
   </tbody>
   </table>

     

7. 将服务器场中的每个 RDS 服务器配置为使用发布服务器，并在用户登录时使用发布更新。 当用户登录到 RDS 服务器时，发布更新周期出现，并发布其帐户已获得授权的所有应用程序。 这些应用程序从共享缓存中运行。

**为程序包升级配置 RDS 客户端**

1.  完成应用程序包的升级和测试。

2.  升级 app-v 服务器上的程序包。 然后，将新版本的应用程序发布并流式传输到暂存计算机上的客户端，以便它们完全加载到缓存中。

3.  在安全模式下重新启动暂存计算机，以确保驱动程序未启动。

    **注意** 或者，你可以先停止，然后在 services.msc 中禁用应用程序虚拟化服务，然后重新启动计算机。 复制文件后，请记住启用并再次启动服务。

     

4.  将 Sftfs 缓存文件复制到 SAN，其中所有 RDS 服务器都可以访问它，例如在共享文件夹中。 你可以使用不同的文件名，例如，SFTFS \ _V2。FSD，以区分新版本。

5.  若要在服务器场中的每个 RDS 服务器上配置 app-v RDS 客户端以使用更新的共享缓存文件，请将 AppFS 注册表项文件名值更改为指向已更新文件的位置，例如，\\\\RDSServername\\Sharefolder\\SFTFS\ _V2。FSD. 这可确保每个 RDS 服务器在应用 Vclient 驱动程序重启时收到缓存的更新副本。

    **重要提示** 必须重新启动 RDS 服务器才能使用更新的共享缓存文件。

     

## 升级缓存时如何使用符号链接


不必在每次部署包含新的或已升级的程序包的新缓存文件时更改 AppFS 项文件名，您可以使用以下操作系统中的符号链接： Windows Vista、Windows 7 和 Windows Server 2008。 有关符号链接的详细信息，请参阅[符号链接](https://go.microsoft.com/fwlink/?LinkId=157626)（ https://go.microsoft.com/fwlink/?LinkId=157626) 。 相比之下，Windows XP 不支持使用符号链接，您必须改用交接点。 有关联接的详细信息，请参阅 Microsoft 知识库中的[文章 205524](https://go.microsoft.com/fwlink/?LinkId=182553) （ https://go.microsoft.com/fwlink/?LinkId=182553) 以及工具[连接 v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) （） https://go.microsoft.com/fwlink/?LinkId=182554) 。

**配置符号链接以引用缓存**

1.  在初始部署阶段，在 RDS 服务器主机操作系统上以本地管理员身份打开命令提示符窗口。

2.  使用 MKLINK 命令创建符号链接，然后将其配置为指向 Sftfs 文件。

    **     mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd**

3.  在 VDI 主 VM 映像上，使用 "以**管理员身份运行**" 选项打开命令提示符窗口，并授予远程链接权限，以便 VM 可以访问 VDI 主机操作系统上的符号链接。 默认情况下，禁用远程链接权限。

    **fsutil behavior set SymlinkEvaluation R2R：1**

    **注意** 在存储服务器上，必须启用相应的链接权限。 根据 link 和 Sftfs 文件的位置，权限为**L2L： 1**或**L2R： 1**或**R2L** ： 1**或 R2R：1。**

     

4.  配置 App-v RDS 客户端时，请将 AppFS 项文件名值设置为等于使用符号链接的 FSD 文件的 UNC 路径。 例如，将文件名设置为 \\\\VDIHostserver\\Symlinkname。 当 App-v 客户端首次访问缓存时，符号链接将向客户端传递一个指向缓存文件的句柄。 只要客户端运行，客户端就会继续使用该句柄。 即使现有客户端已打开旧的共享缓存，符号链接的值也可以安全更新。

5.  当必须升级程序包或将新程序包添加到缓存时，请按照升级过程中的步骤1到步骤4操作。 然后，删除符号链接并重新创建以指向共享缓存文件的新版本。 这可保证当 App-v 客户端驱动程序重启时，每个 RDS 服务器都会收到更新的缓存副本。 当重新启动 RDS 服务器时，App-v 客户端将收到缓存的更新副本的句柄，因为客户端使用包含更新符号链接的路径。 然后，用户有权访问新的和更新的应用程序。

## 相关主题


[如何安装 Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)

[如何手动安装 Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[如何使用命令行安装客户端](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





