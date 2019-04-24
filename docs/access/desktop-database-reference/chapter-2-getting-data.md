---
title: 'Kapitel 2: Abrufen von Daten'
TOCTitle: 'Chapter 2: Getting data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f059e5dfe064442f10972fd36344e64f84fe7ea5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296444"
---
# <a name="chapter-2-getting-data"></a>Kapitel 2: Abrufen von Daten

**Gilt für**: Access 2013, Office 2013

Im vorangegangenen Kapitel wurden vier wichtige Vorgänge zum Erstellen einer ADO-Anwendung vorgestellt: Abrufen von Daten, Überprüfen von Daten, Bearbeiten von Daten sowie Aktualisieren von Daten. Dieses Kapitel befasst sich mit den Konzepten im Zusammenhang mit dem ersten Vorgang, also dem Abrufen von Daten.

Mehrere ADO-Objekte können bei diesem Vorgang eine Rolle spielen. Zunächst stellen Sie mithilfe eines **Connection** -Objekts von ADO (das manchmal impliziert erstellt wird) eine Verbindung mit der Datenquelle her. Danach übergeben Sie mit einem **Command** -Objekt von ADO (das auch implizit erstellt werden kann) Anweisungen an die Datenquelle, welche Schritte ausgeführt werden sollen. Das Ergebnis des Übergebens eines Befehls an eine Datenquelle und das Empfangen der Antwort wird gewöhnlich in einem **Recordset** -Objekt von ADO dargestellt.

Zum Abrufen von Daten muss die Anwendung mit einer Datenquelle kommunizieren, wie z. B. einem DBMS, einem Dateispeicher oder einer durch Trennzeichen getrennten Textdatei. Diese Kommunikation stellt eine *Verbindung* dar – die erforderliche Umgebung für den Austausch von Daten.

Das ADO-Objektmodell stellt das Konzept einer Verbindung mit dem **Connection** -Objekt dar, also die Grundlage, auf der ein Großteil der ADO-Funktionalität basiert. Ein **Connection** -Objekt hat folgenden Zweck:

- Definieren der Informationen, die ADO zum Kommunizieren mit Datenquellen und zum Erstellen von Sitzungen benötigt.

- Definieren der Transaktionsfunktionen der Sitzung.

- Ermöglichen des Erstellens und Ausführens von Befehlen für die Datenquelle.

- Bereitstellen von Informationen zum Entwurf der zugrunde liegenden Datenquelle in Form von Schemarowsets. Weitere Informationen zu Schemarowsets finden Sie unter [OpenSchema-Methode](openschema-method-ado.md).

In diesem Kapitel werden die folgenden Themen behandelt:

- [Herstellen einer Verbindung](making-a-connection.md)
- [Verwenden der Connection-Objektreferenz (ADO)](using-the-connection-object-access.md)
- [Verwenden des Command-Objektverweises (ADO)](using-the-command-object-access.md)
- [Hinzufügen von Daten zu einem Recordset (ADO)](adding-data-to-a-recordset.md)
