---
title: Dienstanbieter und Komponenten
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0241d5acc866ef69469fedbfb27694ed13e683da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593565"
---
# <a name="service-providers-and-components"></a>Dienstanbieter und Komponenten


**Gilt für**: Access 2013, Office 2013

Dienstanbieter sind Komponenten, die die Funktionalität von Datenprovidern erweitern, indem erweiterte Schnittstellen implementiert werden, die vom Datenspeicher systemintern nicht unterstützt werden.

Microsoft Data Access stellt eine *Komponentenarchitektur* bereit, mit der einzelne, spezialisierte Komponenten für weniger leistungsfähige Datenspeicher eigenständige Datenbankfunktionalität oder "Dienste" implementieren können. Anstatt also für jeden Datenspeicher eine eigene Implementierung erweiterter Funktionalität bzw. für einfache Anwendungen die interne Implementierung von Datenbankfunktionalität zu erzwingen, stellen Dienstkomponenten eine allgemeine Implementierung bereit, die von jeder Anwendung beim Zugriff auf einen beliebigen Datenspeicher verwendet werden kann. Die Tatsache, dass bestimmte Funktionen systemintern durch den Datenspeicher sowie durch allgemeine Komponenten implementiert werden, ist im Hinblick auf die Anwendung transparent.

Beispielsweise ist ein Cursormodul wie z. B. der Microsoft Cursor Service für OLE DB eine Dienstkomponente, die Daten eines sequenziellen Vorwärtscursor-Datenspeichers verwenden kann, um Daten zu erstellen, für die ein Bildlauf ausgeführt werden kann. Weitere von ADO häufig verwendete Dienstanbieter sind der Microsoft OLE DB-Anbieter für Persistenz (zum Speichern von Daten in einer Datei), der Microsoft Data Shaping Dienst für OLE DB (für hierarchische **Recordset**-Objekte) und der Microsoft OLE DB-Anbieter für Remoting (zum Aufrufen von Datenprovidern auf einem Remotecomputer).

Weitere Informationen zu Dienstanbietern und Datenprovidern finden Sie in [Anhang A: Anbieter](appendix-a-providers.md).

