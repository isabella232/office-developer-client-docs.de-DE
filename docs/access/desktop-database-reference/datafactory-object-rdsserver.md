---
title: DataFactory-Objekt (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77cd06992ef0062859d0a1372d115f8e65246a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294477"
---
# <a name="datafactory-object-rdsserver"></a>DataFactory-Objekt (RDSServer)


**Gilt für**: Access 2013, Office 2013

Dieses serverseitige Standardgeschäftsobjekt implementiert Methoden, die Lese-/Schreibzugriff auf festgelegte Datenquellen für clientseitige Anwendungen bereitstellen.

## <a name="remarks"></a>Bemerkungen

Das **RDSServer.DataFactory** -Objekt ist als serverseitiges Automatisierungsobjekt konzipiert, das Clientanforderungen empfängt. In einer Internet-Implementierung befindet Sie sich auf einem Webserver und wird von der Komponente "ISAPI" instanziiert. Das **RDSServer.DataFactory** -Objekt bietet Lese-/Schreibzugriff auf angegebene Datenquellen, enthält aber keine Gültigkeitsprüfung oder Logik für Geschäftsregeln.

Wenn Sie eine Methode verwenden, die sowohl im **RDSServer.DataFactory** - als auch im [RDS.DataControl](datacontrol-object-rds.md)-Objekt verfügbar ist, verwendet Remote Data Service standardmäßig die **RDS.DataControl** -Version. Der Standard geht von einem grundlegenden Programmierszenario aus, bei dem das **RDSServer.DataFactory** -Objekt als generisches serverseitiges Geschäftsobjekt dient.

Wenn die Webanwendung aufgabenspezifische serverseitige Verarbeitung verarbeiten soll, können Sie die **RDSServer. DataFactory** durch ein benutzerdefiniertes Geschäftsobjekt ersetzen.

Sie können serverseitige Geschäftsobjekte erstellen, die die **RDSServer.DataFactory** -Methoden aufrufen, wie etwa [Query](query-method-rds.md) und [CreateRecordset](createrecordset-method-rds.md). Dies ist nützlich, wenn Sie den Geschäftsobjekten eine bestimmte Funktionalität hinzufügen und gleichzeitig vorhandene Remote Data Service-Technologien nutzen wollen.

Die Klassen-ID für das **RDSServer.DataFactory** -Objekt lautet 9381D8F5-0288-11D0-9501-00AA00B911A5.

