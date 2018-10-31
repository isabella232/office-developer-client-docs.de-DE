---
title: OLE DB-Anbieter (Access PC-Datenbank-Referenz)
TOCTitle: OLE DB Providers
ms:assetid: ef412198-eac5-bf86-73fd-574e67276408
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250215(v=office.15)
ms:contentKeyID: 48548576
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab2a2ca391927b3ae338910af544d99e01309b06
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861799"
---
# <a name="ole-db-providers"></a>OLE DB-Anbieter


**Betrifft**: Access 2013 | Office 2013

In der [Einführung](introduction-to-ado-programming.md) im ADO-Programmierhandbuch wird die Beziehung zwischen ADO und der restlichen Microsoft Data Access-Architektur behandelt. OLE DB definiert eine Reihe von COM-Schnittstellen, um Anwendungen einen einheitlichen Zugriff auf Daten zu ermöglichen, die in verschiedenen Datenquellen gespeichert sind. Auf diese Weise können die Daten einer Datenquelle in Schnittstellen verwendet werden, die die entsprechende DBMS-Funktionalität unterstützen. Die leistungsfähige OLE DB-Architektur basiert auf der Verwendung eines flexiblen, komponentenbasierten Dienstmodells. Anstelle einer vorgeschriebenen Anzahl von Zwischenkomponenten zwischen der Anwendung und den Daten benötigt OLE DB nur so viele Komponenten, wie zum Ausführen einer bestimmten Aufgabe erforderlich sind.

Angenommen, ein Benutzer möchte eine Abfrage ausführen. Betrachten Sie dazu die folgenden Szenarien:

  - Die Daten sind in einer relationalen Datenbank gespeichert, für die derzeit ein ODBC-Treiber, aber kein systemeigener OLE DB-Anbieter vorhanden ist: ADO wird von der Anwendung für die Kommunikation mit dem OLE DB-Anbieter für ODBC verwendet, der dann den entsprechenden ODBC-Treiber lädt. Der Treiber übergibt die SQL-Anweisung an das DBMS, das die Daten abruft.

  - Die Daten sind in Microsoft SQL Server gespeichert, wofür es einen systemeigenen OLE DB-Anbieter gibt: Die Anwendung verwendet ADO für die direkte Kommunikation mit dem OLE DB-Anbieter für Microsoft SQL Server. Es sind keine Zwischenkomponenten erforderlich.

  - Die Daten sind in Microsoft Exchange Server gespeichert, wofür es einen OLE DB-Anbieter gibt, der jedoch kein Modul zum Verarbeiten von SQL-Abfragen verfügbar macht: Die Anwendung verwendet ADO für die Kommunikation mit dem OLE DB-Anbieter für Microsoft Exchange und ruft eine OLE DB-Abfrageprozessorkomponente zum Verarbeiten der Abfragen auf.

  - Die Daten sind im Microsoft NTFS-Dateisystem in Form von Dokumenten gespeichert: Auf die Daten wird mit einem systemeigenen OLE DB-Anbieter over Microsoft Indexing Service zugegriffen, der den Inhalt und die Eigenschaften von Dokumenten im Dateisystem indiziert, um effiziente Suchvorgänge für Inhalt zu ermöglichen.

In allen vorangegangenen Beispielen können die Daten von der Anwendung abgefragt werden. Die Anforderungen des Benutzers werden mit einer minimalen Anzahl von Komponenten erfüllt. In jedem Fall werden zusätzliche Komponenten nur bei Bedarf verwendet, und nur die erforderlichen Komponenten werden aufgerufen. Durch das Laden im Bedarfsfall von wiederverwendbaren und gemeinsam nutzbaren Komponenten kann die Leistung bei der Verwendung von OLE DB erheblich optimiert werden.

Die Anbieter können in zwei Kategorien unterteilt werden: Anbieter, die Daten bereitstellen, und Anbieter, die Dienste bereitstellen. Ein [Datenprovider](data-providers.md) besitzt seine eigenen Daten und macht sie im Tabellenformat für die Anwendung verfügbar. Ein [Dienstanbieter](service-providers-and-components.md) kapselt einen Dienst durch Erstellen und Verwenden von Daten, wodurch in Ihren ADO-Anwendungen mehr Features bereitstehen. Ein Dienstanbieter kann außerdem weiterhin als [Dienstkomponente](service-providers-and-components.md) bezeichnet werden, die in Verbindung mit anderen Dienstanbietern oder -komponenten verwendet wird.

ADO stellt den verschiedenen OLE DB-Anbietern eine konsistente Schnittstelle auf hoher Ebene bereit.

Dieser Abschnitt enthält die folgenden Themen:

- [Data Providers](data-providers.md)

- [Dienstanbieter und Komponenten](service-providers-and-components.md)