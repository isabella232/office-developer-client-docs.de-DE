---
title: Referenz zu Microsoft ActiveX Data Objects
TOCTitle: Microsoft ActiveX Data Objects Reference
ms:assetid: 235fc575-8a2e-913c-fa3d-bb86256733f9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249010(v=office.15)
ms:contentKeyID: 48543728
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c1fee657c0d6ecd319157f704df2b1c5a900be3b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289119"
---
# <a name="microsoft-activex-data-objects-reference"></a>Referenz zu Microsoft ActiveX Data Objects

**Gilt für**: Access 2013, Office 2013

## <a name="purpose"></a>Zweck

Mit Microsoft ActiveX Data Objects (ADO) können Clientanwendungen über einen OLE DB-Anbieter auf Daten auf einem Datenbankserver zugreifen und diese bearbeiten. Die wichtigsten Vorteile sind einfache Handhabung, hohe Geschwindigkeit sowie geringer Arbeitsspeicher- und Speicherplatzbedarf. ADO unterstützt Schlüsselfeatures für das Erstellen von Client-/Server- und webbasierten Anwendungen.

## <a name="rds"></a>RDS

ADO bietet außerdem Remote Data Service (RDS). Hiermit können Sie Daten von einem Server in eine Clientanwendung oder auf eine Website verschieben, die Datei auf dem Client bearbeiten sowie Updates an den Server in einem einzelnen Roundtrip zurückgeben.

## <a name="ado-md"></a>ADO MD

Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the CubeDef and Cellset objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.

ADO MD verwendet wie ADO einen zugrunde liegenden OLE DB-Anbieter für den Zugriff auf Daten. Der Anbieter muss gemäß der OLE DB für OLAP-Spezifikation ein multidimensionaler Datenprovider (MDP) sein, um mit ADO MD arbeiten zu können. MDPs stellen Daten in multidimensionalen Ansichten dar. Tabulare Datenprovider (TDP) stellen Daten dagegen in tabularen Ansichten dar. In der Dokumentation zu Ihrem OLE DB für OLAP-Anbieter finden Sie ausführlichere Information zur Syntax und zu den Funktionen, die von Ihrem Anbieter unterstützt werden.

## <a name="adox"></a>ADOX

Microsoft ActiveX Data Objects Extensions für Datendefinitionssprache und Sicherheit (ADOX) ist eine Erweiterung der ADO-Objekte und des Programmiermodells. ADOX enthält Objekte zum Erstellen und Ändern von Schemas sowie zur Sicherheit. Da es sich um einen objektbasierten Ansatz zur Schemabearbeitung handelt, können Sie Code erstellen, der für verschiedene Datenquellen verwendet werden kann, ungeachtet der Unterschiede in der jeweiligen Syntax.

ADOX ist eine Begleitbibliothek zu ADO-Kernobjekten. Hiermit werden zusätzliche Objekte für das Erstellen, Ändern und Löschen von Schemaobjekten wie Tabellen und Prozeduren verfügbar gemacht. Außerdem enthält dieses Element Sicherheitsobjekte, um Benutzer und Gruppen zu warten und um Berechtigungen für Objekte zu erteilen und aufzuheben.

## <a name="ado-25-main-components"></a>ADO 2.5-Hauptkomponenten

- [Leitfaden für Programmierer](ado-programmer-s-guide.md): Eine Einführung in die Verwendung von ADO, RDS, ADO MD und ADOX.

- [Referenz für Programmierer](ado-programmer-s-reference-topics.md)Dieser Abschnitt der ADO-Dokumentation behandelt Themen zu den verschiedenen Objekten, Auflistungen, Eigenschaften, dynamischen Eigenschaften, Methoden, Ereignissen und Aufzählungen von ADO, RDS, ADO MD und ADOX.

## <a name="feedback"></a>Feedback

Feedback zu ADO-Dokumentation oder Beispielen können Sie direkt an das ADO-Dokumentationsteam senden.

