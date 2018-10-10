---
title: Konfigurieren von 'DataFactory' für den sicheren oder den uneingeschränkten Modus
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: abb461473d15f163fac6ea00f2af5d39f7b40d0a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475712"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a>Konfigurieren von "DataFactory" für den sicheren oder den uneingeschränkten Modus


**Betrifft**: Access 2013 | Office 2013

Standardmäßig wird ADO (ActiveX Data Objects) mit einer sicheren [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Konfiguration installiert. Der sichere Modus für RDS-Serverkomponenten (Remote Data Service) bedeutet, dass Folgendes gilt:

1.  Ein Handler ist für RDSServer.DataFactory erforderlich (dies ist durch die Einstellung für einen Registrierungsschlüssel festgelegt).

2.  Der Standardhandler msdfmap.handler ist registriert, in der Liste sicherer Handler aufgeführt und als Standardhandler gekennzeichnet.

3.  Die Datei Msdfmap.ini ist im Windows-Verzeichnis installiert. Sie müssen diese Datei nach Ihren Anforderungen konfigurieren, bevor Sie RDS im dreistufigen Modus verwenden.

Optional können Sie eine uneingeschränkte **DataFactory** -Installation konfigurieren. **DataFactory** kann direkt verwendet werden, ohne den benutzerdefinierten Handler. Benutzer können trotzdem einen benutzerdefinierten Handler verwenden, indem Sie die Verbindungszeichenfolgen ändern, aber dies ist nicht erforderlich. Weitere Informationen zu den Auswirkungen, die die Verwendung des **RDSServer.DataFactory** -Objekts hat, finden Sie unter [Sichern von RDS-Anwendungen](securing-rds-applications.md).

Die Registrierungsdatei handsafe.reg wurde bereitgestellt, um die Registrierungseinträge des Handlers für eine sichere Konfiguration einzurichten. Führen Sie für den sicheren Modus handsafe.reg aus. Die Registrierungsdatei handunsf.reg wurde bereitgestellt, um die Registrierungseinträge des Handlers für eine uneingeschränkte Konfiguration einzurichten. Führen Sie für den uneingeschränkten Modus handunsf.reg aus.

Nach der Ausführung von handsafe.reg oder handunsf.reg müssen Sie den WWW-Publishingdienst auf dem Webserver beenden und neu starten, indem Sie die folgenden Befehle an der Eingabeaufforderung eingeben: NET STOP W3SVC und NET START W3SVC.

Weitere Informationen zur Verwendung des Features zur Handleranpassung finden Sie im technischen Artikel zur Verwendung des Features zur Handleranpassung in RDS 2.1.

