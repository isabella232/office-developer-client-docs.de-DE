---
title: Microsoft ActiveX Data Objects reference
TOCTitle: Microsoft ActiveX Data Objects Reference
ms:assetid: 235fc575-8a2e-913c-fa3d-bb86256733f9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249010(v=office.15)
ms:contentKeyID: 48543728
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5426dd17e174c0aa95517885fd43e7d00f21342b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474352"
---
# <a name="microsoft-activex-data-objects-reference"></a>Microsoft ActiveX Data Objects reference

**Betrifft**: Access 2013 | Office 2013

## <a name="purpose"></a>Zweck

Mit Microsoft ActiveX Data Objects (ADO) können Clientanwendungen über einen OLE DB-Anbieter auf Daten auf einem Datenbankserver zugreifen und diese bearbeiten. Die wichtigsten Vorteile sind einfache Handhabung, hohe Geschwindigkeit sowie geringer Arbeitsspeicher- und Speicherplatzbedarf. ADO unterstützt Schlüsselfeatures für das Erstellen von Client-/Server- und webbasierten Anwendungen.

## <a name="rds"></a>RDS

ADO bietet außerdem Remote Data Service (RDS). Hiermit können Sie Daten von einem Server in eine Clientanwendung oder auf eine Website verschieben, die Datei auf dem Client bearbeiten sowie Updates an den Server in einem einzelnen Roundtrip zurückgeben.

## <a name="ado-md"></a>ADO MD

Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) ermöglicht den einfachen Zugriff auf multidimensionale Daten in Sprachen wie z. B. Microsoft Visual Basic, Microsoft Visual C++ und Microsoft Visual J++. ADO MD erweitert Microsoft ActiveX Data Objects (ADO) um Objekte speziell für multidimensionale Daten, wie z. B. die CubeDef- und Cellset-Objekte. Mit ADO MD können Sie ein multidimensionales Schema durchsuchen, einen Cube abfragen und die Ergebnisse abrufen.

ADO MD verwendet wie ADO einen zugrunde liegenden OLE DB-Anbieter für den Zugriff auf Daten. Der Anbieter muss gemäß der OLE DB für OLAP-Spezifikation ein multidimensionaler Datenprovider (MDP) sein, um mit ADO MD arbeiten zu können. MDPs stellen Daten in multidimensionalen Ansichten dar. Tabulare Datenprovider (TDP) stellen Daten dagegen in tabularen Ansichten dar. In der Dokumentation zu Ihrem OLE DB für OLAP-Anbieter finden Sie ausführlichere Information zur Syntax und zu den Funktionen, die von Ihrem Anbieter unterstützt werden.

## <a name="adox"></a>ADOX

Microsoft ActiveX Data Objects Extensions für Datendefinitionssprache und Sicherheit (ADOX) ist eine Erweiterung der ADO-Objekte und des Programmiermodells. ADOX enthält Objekte zum Erstellen und Ändern von Schemas sowie zur Sicherheit. Da es sich um einen objektbasierten Ansatz zur Schemabearbeitung handelt, können Sie Code erstellen, der für verschiedene Datenquellen verwendet werden kann, ungeachtet der Unterschiede in der jeweiligen Syntax.

ADOX ist eine Begleitbibliothek zu ADO-Kernobjekten. Hiermit werden zusätzliche Objekte für das Erstellen, Ändern und Löschen von Schemaobjekten wie Tabellen und Prozeduren verfügbar gemacht. Außerdem enthält dieses Element Sicherheitsobjekte, um Benutzer und Gruppen zu warten und um Berechtigungen für Objekte zu erteilen und aufzuheben.

## <a name="ado-25-main-components"></a>ADO 2.5 Hauptkomponenten

- [Programmierhandbuch](ado-programmer-s-guide.md): eine Einführung in die Verwendung von ADO, RDS, ADO MD und ADOX.

- [Programmer's Reference](ado-programmer-s-reference-topics.md): in diesem Abschnitt der ADO-Dokumentation enthält Themen jede Auflistung von ADO, RDS, ADO MD und ADOX-Objekt, -Eigenschaft, dynamische Eigenschaft, -Methode, -Ereignis, und -Enumeration.

## <a name="feedback"></a>Feedback

Feedback zu ADO-Dokumentation oder Beispielen können Sie direkt an das ADO-Dokumentationsteam senden.

