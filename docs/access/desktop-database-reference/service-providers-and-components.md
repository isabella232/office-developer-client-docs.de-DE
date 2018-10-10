---
title: Dienstanbieter und Komponenten
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e7b099b7fda71f09e9e2a1bb3596c23106771fb3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475766"
---
# <a name="service-providers-and-components"></a>Dienstanbieter und Komponenten


**Betrifft**: Access 2013 | Office 2013

Dienstanbieter sind Komponenten, die die Funktionalität von Datenprovidern erweitern, indem erweiterte Schnittstellen implementiert werden, die vom Datenspeicher systemintern nicht unterstützt werden.

Microsoft Data Access bietet eine *Komponentenarchitektur* , die einzelne, spezialisierte Komponenten implementieren diskrete können Datenbankfunktionalität oder "Dienste" auf der Basis weniger leistungsfähige Speicher-Sätze. Auf diese Weise statt erzwingen jedes Datenspeicher auf eine eigenen Implementierung von erweiterten Funktionen bereit, oder erzwingen, dass generische Applications Datenbankfunktionalität intern implementieren, Dienstkomponenten eine allgemeine Implementierung bereit, die jeder Anwendung können Verwenden Sie beim Zugriff auf jeden beliebigen Datenspeicher. Die Tatsache, dass einige Funktionen systemintern vom Datenspeicher und durch allgemeine Komponenten implementiert wird, ist für die Anwendung transparent.

Beispielsweise ist ein Cursormodul wie z. B. der Microsoft Cursor Service für OLE DB eine Dienstkomponente, die Daten eines sequenziellen Vorwärtscursor-Datenspeichers verwenden kann, um Daten zu erstellen, für die ein Bildlauf ausgeführt werden kann. Weitere von ADO häufig verwendete Dienstanbieter sind der Microsoft OLE DB-Anbieter für Persistenz (zum Speichern von Daten in einer Datei), der Microsoft Data Shaping Dienst für OLE DB (für hierarchische **Recordset**-Objekte) und der Microsoft OLE DB-Anbieter für Remoting (zum Aufrufen von Datenprovidern auf einem Remotecomputer).

Weitere Informationen zu Dienstanbietern und Datenprovidern finden Sie in [Anhang A: Anbieter](appendix-a-providers.md).

