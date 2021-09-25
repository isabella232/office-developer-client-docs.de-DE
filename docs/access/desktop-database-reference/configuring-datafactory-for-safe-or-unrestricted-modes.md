---
title: Konfigurieren von 'DataFactory' für den sicheren oder den uneingeschränkten Modus
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aa371dd98d61bd23b33c83bf4ce9b78947e10600
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577563"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a>Konfigurieren von 'DataFactory' für den sicheren oder den uneingeschränkten Modus


**Gilt für**: Access 2013, Office 2013

Standardmäßig wird ADO (ActiveX Data Objects) mit einer sicheren [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Konfiguration installiert. Der sichere Modus für RDS-Serverkomponenten (Remote Data Service) bedeutet, dass Folgendes gilt:

1.  Handler is required with the RDSServer.DataFactory (this is mandated by a registry key setting).

2.  The default handler, msdfmap.handler, is registered, present in the safe-handler list, and marked as the default handler.

3.  Msdfmap.ini file is installed in the Windows directory. You must configure this file according to your needs, before using RDS in three-tier mode.

Optional können Sie eine uneingeschränkte **DataFactory** -Installation konfigurieren. **DataFactory** kann direkt verwendet werden, ohne den benutzerdefinierten Handler. Benutzer können trotzdem einen benutzerdefinierten Handler verwenden, indem Sie die Verbindungszeichenfolgen ändern, aber dies ist nicht erforderlich. Weitere Informationen zu den Auswirkungen der Verwendung des **RDSServer.DataFactory** -Objekts finden Sie unter [Sichern von RDS-Anwendungen](securing-rds-applications.md).

The registry file handsafe.reg has been provided to set up the handler registry entries for a safe configuration. To run in safe mode, run handsafe.reg. The registry file handunsf.reg has been provided to set up the handler registry entries for an unrestricted configuration. To run in unrestricted mode, run handunsf.reg.

Nachdem Sie "handsafe.reg" oder "handunsf.reg" ausgeführt haben, müssen Sie den World Wide Web Publishing Service auf dem Webserver beenden und neu starten, indem Sie die folgenden Befehle in ein Befehlsfenster eingeben: "NET STOP W3SVC" und "NET START W3SVC".

Weitere Informationen zur Verwendung des Features zur Handleranpassung finden Sie im technischen Artikel zur Verwendung des Features zur Handleranpassung in RDS 2.1.

