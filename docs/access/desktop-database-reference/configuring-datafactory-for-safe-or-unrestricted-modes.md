---
title: Konfigurieren von 'DataFactory' für den sicheren oder den uneingeschränkten Modus
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a3f551e4c377a0c24a0b733ff094e19d1b75d725
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606402"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a><span data-ttu-id="ad2eb-102">Konfigurieren von "DataFactory" für den sicheren oder den uneingeschränkten Modus</span><span class="sxs-lookup"><span data-stu-id="ad2eb-102">Configuring DataFactory for Safe or Unrestricted Modes</span></span>


<span data-ttu-id="ad2eb-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad2eb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ad2eb-p101">Standardmäßig wird ADO (ActiveX Data Objects) mit einer sicheren [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Konfiguration installiert. Der sichere Modus für RDS-Serverkomponenten (Remote Data Service) bedeutet, dass Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="ad2eb-p101">By default, ADO is installed with a "safe" [RDSServer.DataFactory](datafactory-object-rdsserver.md) configuration. Safe mode for RDS Server components means that the following are true:</span></span>

1.  <span data-ttu-id="ad2eb-106">Ein Handler ist für RDSServer.DataFactory erforderlich (dies ist durch die Einstellung für einen Registrierungsschlüssel festgelegt).</span><span class="sxs-lookup"><span data-stu-id="ad2eb-106">Handler is required with the RDSServer.DataFactory (this is mandated by a registry key setting).</span></span>

2.  <span data-ttu-id="ad2eb-107">Der Standardhandler msdfmap.handler ist registriert, in der Liste sicherer Handler aufgeführt und als Standardhandler gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="ad2eb-107">The default handler, msdfmap.handler, is registered, present in the safe-handler list, and marked as the default handler.</span></span>

3.  <span data-ttu-id="ad2eb-p102">Die Datei Msdfmap.ini ist im Windows-Verzeichnis installiert. Sie müssen diese Datei nach Ihren Anforderungen konfigurieren, bevor Sie RDS im dreistufigen Modus verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad2eb-p102">Msdfmap.ini file is installed in the Windows directory. You must configure this file according to your needs, before using RDS in three-tier mode.</span></span>

<span data-ttu-id="ad2eb-p103">Optional können Sie eine uneingeschränkte **DataFactory** -Installation konfigurieren. **DataFactory** kann direkt verwendet werden, ohne den benutzerdefinierten Handler. Benutzer können trotzdem einen benutzerdefinierten Handler verwenden, indem Sie die Verbindungszeichenfolgen ändern, aber dies ist nicht erforderlich. Weitere Informationen zu den Auswirkungen, die die Verwendung des **RDSServer.DataFactory** -Objekts hat, finden Sie unter [Sichern von RDS-Anwendungen](securing-rds-applications.md).</span><span class="sxs-lookup"><span data-stu-id="ad2eb-p103">Optionally, you can configure an unrestricted **DataFactory** installation. **DataFactory** can be used directly without the custom handler. Users can still use a custom handler by modifying the connection strings, but it is not required. For more information on the implications of using the **RDSServer.DataFactory** object, see [Securing RDS Applications](securing-rds-applications.md).</span></span>

<span data-ttu-id="ad2eb-p104">Die Registrierungsdatei handsafe.reg wurde bereitgestellt, um die Registrierungseinträge des Handlers für eine sichere Konfiguration einzurichten. Führen Sie für den sicheren Modus handsafe.reg aus. Die Registrierungsdatei handunsf.reg wurde bereitgestellt, um die Registrierungseinträge des Handlers für eine uneingeschränkte Konfiguration einzurichten. Führen Sie für den uneingeschränkten Modus handunsf.reg aus.</span><span class="sxs-lookup"><span data-stu-id="ad2eb-p104">The registry file handsafe.reg has been provided to set up the handler registry entries for a safe configuration. To run in safe mode, run handsafe.reg. The registry file handunsf.reg has been provided to set up the handler registry entries for an unrestricted configuration. To run in unrestricted mode, run handunsf.reg.</span></span>

<span data-ttu-id="ad2eb-117"><<<<<<< HEAD nach der Ausführung handsafe.reg oder handunsf.reg, müssen Sie beenden und erneutes Starten der WWW-Publishingdienst auf dem Webserver durch Eingabe der folgenden Befehle in einem Befehlsfenster: "NET STOP W3SVC" und "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="ad2eb-117"><<<<<<< HEAD After running either handsafe.reg or handunsf.reg, you must stop and restart the World Wide Web Publishing Service on the Web server by typing the following commands in a command window: "NET STOP W3SVC" and "NET START W3SVC".</span></span>
<span data-ttu-id="ad2eb-118">=== Nach handsafe.reg oder handunsf.reg ausführen, müssen Sie beenden und erneutes Starten der WWW-Publishingdienst auf dem Webserver durch Eingabe der folgenden Befehle in einem Befehlsfenster: "NET STOP W3SVC" und "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="ad2eb-118">======= After running either handsafe.reg or handunsf.reg, you must stop and restart the World Wide Web Publishing Service on the web server by typing the following commands in a command window: "NET STOP W3SVC" and "NET START W3SVC".</span></span>
>>>>>>> <span data-ttu-id="ad2eb-119">master</span><span class="sxs-lookup"><span data-stu-id="ad2eb-119">master</span></span>

<span data-ttu-id="ad2eb-120">Weitere Informationen zur Verwendung des Features zur Handleranpassung finden Sie im technischen Artikel zur Verwendung des Features zur Handleranpassung in RDS 2.1.</span><span class="sxs-lookup"><span data-stu-id="ad2eb-120">For more information about using the customization handler feature of RDS, see the technical article Using the Customization Handler Feature in RDS 2.1.</span></span>

