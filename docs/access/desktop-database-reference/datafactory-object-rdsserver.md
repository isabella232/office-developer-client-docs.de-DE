---
title: DataFactory-Objekt (RDSServer)
TOCTitle: DataFactory Object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba705854fc27a18fd0d3d7a7c6fd7acdefb3830f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472911"
---
# <a name="datafactory-object-rdsserver"></a>DataFactory-Objekt (RDSServer)


**Betrifft**: Access 2013 | Office 2013

Dieses serverseitige Standardgeschäftsobjekt implementiert Methoden, die Lese-/Schreibzugriff auf festgelegte Datenquellen für clientseitige Anwendungen bereitstellen.

## <a name="remarks"></a>Hinweise

Das **RDSServer.DataFactory** -Objekt ist als serverseitiges Automatisierungsobjekt konzipiert, das Clientanforderungen empfängt. In einer Internet-Implementierung befindet es sich auf einem Webserver und wird von der ADISAPI-Komponente instanziiert. Das **RDSServer.DataFactory** -Objekt bietet Lese-/Schreibzugriff auf angegebene Datenquellen, enthält aber keine Gültigkeitsprüfung oder Logik für Geschäftsregeln.

Wenn Sie eine Methode verwenden, die sowohl im **RDSServer.DataFactory** - als auch im [RDS.DataControl](datacontrol-object-rds.md)-Objekt verfügbar ist, verwendet Remote Data Service standardmäßig die **RDS.DataControl** -Version. Der Standard geht von einem grundlegenden Programmierszenario aus, bei dem das **RDSServer.DataFactory** -Objekt als generisches serverseitiges Geschäftsobjekt dient.

Wenn die Webanwendung eine aufgabenspezifische serverseitige Verarbeitung erfordert, können Sie das **RDSServer.DataFactory** -Objekt durch ein angepasstes Geschäftsobjekt ersetzen.

Sie können serverseitige Geschäftsobjekte erstellen, die die **RDSServer.DataFactory** -Methoden aufrufen, wie etwa [Query](query-method-rds.md) und [CreateRecordset](createrecordset-method-rds.md). Dies ist nützlich, wenn Sie den Geschäftsobjekten eine bestimmte Funktionalität hinzufügen und gleichzeitig vorhandene Remote Data Service-Technologien nutzen wollen.

Die Klassen-ID für das **RDSServer.DataFactory** -Objekt lautet 9381D8F5-0288-11D0-9501-00AA00B911A5.

