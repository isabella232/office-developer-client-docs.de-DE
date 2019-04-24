---
title: Konfigurieren von 'DataFactory' für den sicheren oder den uneingeschränkten Modus
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4313d48359499eaf249a68eb97408c8ed4ecb88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295996"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a><span data-ttu-id="20609-102">Konfigurieren von 'DataFactory' für den sicheren oder den uneingeschränkten Modus</span><span class="sxs-lookup"><span data-stu-id="20609-102">Configuring DataFactory for Safe or Unrestricted Modes</span></span>


<span data-ttu-id="20609-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20609-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20609-p101">Standardmäßig wird ADO (ActiveX Data Objects) mit einer sicheren [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Konfiguration installiert. Der sichere Modus für RDS-Serverkomponenten (Remote Data Service) bedeutet, dass Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="20609-p101">By default, ADO is installed with a "safe" [RDSServer.DataFactory](datafactory-object-rdsserver.md) configuration. Safe mode for RDS Server components means that the following are true:</span></span>

1.  <span data-ttu-id="20609-106">Handler is required with the RDSServer.DataFactory (this is mandated by a registry key setting).</span><span class="sxs-lookup"><span data-stu-id="20609-106">Handler is required with the RDSServer.DataFactory (this is mandated by a registry key setting).</span></span>

2.  <span data-ttu-id="20609-107">The default handler, msdfmap.handler, is registered, present in the safe-handler list, and marked as the default handler.</span><span class="sxs-lookup"><span data-stu-id="20609-107">The default handler, msdfmap.handler, is registered, present in the safe-handler list, and marked as the default handler.</span></span>

3.  <span data-ttu-id="20609-p102">Msdfmap.ini file is installed in the Windows directory. You must configure this file according to your needs, before using RDS in three-tier mode.</span><span class="sxs-lookup"><span data-stu-id="20609-p102">Msdfmap.ini file is installed in the Windows directory. You must configure this file according to your needs, before using RDS in three-tier mode.</span></span>

<span data-ttu-id="20609-110">Optional können Sie eine uneingeschränkte **DataFactory** -Installation konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="20609-110">Optionally, you can configure an unrestricted **DataFactory** installation.</span></span> <span data-ttu-id="20609-111">**DataFactory** kann direkt verwendet werden, ohne den benutzerdefinierten Handler.</span><span class="sxs-lookup"><span data-stu-id="20609-111">**DataFactory** can be used directly without the custom handler.</span></span> <span data-ttu-id="20609-112">Benutzer können trotzdem einen benutzerdefinierten Handler verwenden, indem Sie die Verbindungszeichenfolgen ändern, aber dies ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="20609-112">Users can still use a custom handler by modifying the connection strings, but it is not required.</span></span> <span data-ttu-id="20609-113">Weitere Informationen zu den Auswirkungen der Verwendung des **RDSServer. DataFactory** -Objekts finden Sie unter [Sichern von RDS-Anwendungen](securing-rds-applications.md).</span><span class="sxs-lookup"><span data-stu-id="20609-113">For more information about the implications of using the **RDSServer.DataFactory** object, see [Securing RDS Applications](securing-rds-applications.md).</span></span>

<span data-ttu-id="20609-p104">The registry file handsafe.reg has been provided to set up the handler registry entries for a safe configuration. To run in safe mode, run handsafe.reg. The registry file handunsf.reg has been provided to set up the handler registry entries for an unrestricted configuration. To run in unrestricted mode, run handunsf.reg.</span><span class="sxs-lookup"><span data-stu-id="20609-p104">The registry file handsafe.reg has been provided to set up the handler registry entries for a safe configuration. To run in safe mode, run handsafe.reg. The registry file handunsf.reg has been provided to set up the handler registry entries for an unrestricted configuration. To run in unrestricted mode, run handunsf.reg.</span></span>

<span data-ttu-id="20609-117">Nachdem Sie entweder handsafe. reg oder handunsf. reg ausführen, müssen Sie den WWW-Publishing Dienst auf dem Webserver beenden und neu starten, indem Sie die folgenden Befehle in einem Befehlsfenster eingeben: "NET STOP W3SVC" und "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="20609-117">After running either handsafe.reg or handunsf.reg, you must stop and restart the World Wide Web Publishing Service on the web server by typing the following commands in a command window: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

<span data-ttu-id="20609-118">Weitere Informationen zur Verwendung des Features zur Handleranpassung finden Sie im technischen Artikel zur Verwendung des Features zur Handleranpassung in RDS 2.1.</span><span class="sxs-lookup"><span data-stu-id="20609-118">For more information about using the customization handler feature of RDS, see the technical article Using the Customization Handler Feature in RDS 2.1.</span></span>

