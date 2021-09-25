---
title: DataFactory-Objekt (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6e7b7ad54677a24149a3d48b378fdb53d30cee76
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606849"
---
# <a name="datafactory-object-rdsserver"></a>DataFactory-Objekt (RDSServer)


**Gilt für**: Access 2013, Office 2013

Dieses serverseitige Standardgeschäftsobjekt implementiert Methoden, die Lese-/Schreibzugriff auf festgelegte Datenquellen für clientseitige Anwendungen bereitstellen.

## <a name="remarks"></a>HinwBemerkungeneise

Das **RDSServer.DataFactory** -Objekt ist als serverseitiges Automatisierungsobjekt konzipiert, das Clientanforderungen empfängt. In einer Internetimplementierung befindet sie sich auf einem Webserver und wird von der ADISAPI-Komponente instanziiert. Das **RDSServer.DataFactory** -Objekt bietet Lese-/Schreibzugriff auf angegebene Datenquellen, enthält aber keine Gültigkeitsprüfung oder Logik für Geschäftsregeln.

Wenn Sie eine Methode verwenden, die sowohl im **RDSServer.DataFactory** - als auch im [RDS.DataControl](datacontrol-object-rds.md)-Objekt verfügbar ist, verwendet Remote Data Service standardmäßig die **RDS.DataControl** -Version. Der Standard geht von einem grundlegenden Programmierszenario aus, bei dem das **RDSServer.DataFactory** -Objekt als generisches serverseitiges Geschäftsobjekt dient.

Wenn Ihre Webanwendung die aufgabenspezifische serverseitige Verarbeitung verarbeiten soll, können Sie **RDSServer.DataFactory** durch ein benutzerdefiniertes Geschäftsobjekt ersetzen.

Sie können serverseitige Geschäftsobjekte erstellen, die die **RDSServer.DataFactory** -Methoden aufrufen, wie etwa [Query](query-method-rds.md) und [CreateRecordset](createrecordset-method-rds.md). Dies ist nützlich, wenn Sie den Geschäftsobjekten eine bestimmte Funktionalität hinzufügen und gleichzeitig vorhandene Remote Data Service-Technologien nutzen wollen.

Die Klassen-ID für das **RDSServer.DataFactory** -Objekt lautet 9381D8F5-0288-11D0-9501-00AA00B911A5.

