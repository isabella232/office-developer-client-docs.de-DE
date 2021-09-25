---
title: Die ADO-Bibliotheksfamilie
TOCTitle: The ADO family of libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6d3160a8cc0c21c8aa0a4714d48a5e1d16b62256
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593495"
---
# <a name="the-ado-family-of-libraries"></a>Die ADO-Bibliotheksfamilie

**Gilt für**: Access 2013, Office 2013

Die ADO-Familie besteht aus drei Hauptbibliotheken: ADO (einschließlich RDS), ADO MD und ADOX.

## <a name="ado"></a>ADO

Mit ADO können Clientanwendungen über einen OLE DB-Anbieter auf Daten auf einem Datenbankserver zugreifen und diese bearbeiten. Die wichtigsten Vorteile von ADO sind einfache Handhabung, hohe Geschwindigkeit sowie geringer Arbeitsspeicher- und Speicherplatzbedarf. ADO unterstützt Schlüsselfeatures für das Erstellen von Client-/Server- und webbasierten Anwendungen.

ADO bietet außerdem Remote Data Service (RDS). Hiermit können Sie Daten von einem Server in eine Clientanwendung oder auf eine Website verschieben, die Datei auf dem Client bearbeiten sowie Updates an den Server in einem einzelnen Roundtrip zurückgeben.

## <a name="ado-md"></a>ADO MD

Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) ermöglicht den einfachen Zugriff auf multidimensionale Daten in Sprachen wie z. B. Microsoft Visual Basic, Microsoft Visual C++ und Microsoft Visual J++. ADO MD erweitert ADO um Objekte speziell für multidimensionale Daten, wie z. B. die Objekte **CubeDef** und **Cellset**. Mit ADO MD können Sie ein multidimensionales Schema durchsuchen, einen Cube abfragen und die Ergebnisse abrufen.

ADO MD verwendet wie ADO einen zugrunde liegenden OLE DB-Anbieter für den Zugriff auf Daten. Der Anbieter muss gemäß der OLE DB für OLAP-Spezifikation ein multidimensionaler Datenprovider (MDP) sein, um mit ADO MD arbeiten zu können. MDPs stellen Daten in multidimensionalen Ansichten dar. Tabulare Datenprovider (TDP) stellen Daten dagegen in tabularen Ansichten dar. In der Dokumentation zu Ihrem OLE DB für OLAP-Anbieter finden Sie ausführlichere Information zur Syntax und zu den Funktionen, die von Ihrem Anbieter unterstützt werden.

## <a name="adox"></a>ADOX

Microsoft ActiveX Data Objects Extensions für Datendefinitionssprache und Sicherheit (ADOX) ist eine Erweiterung der ADO-Objekte und des Programmiermodells. ADOX enthält Objekte zum Erstellen und Ändern von Schemas sowie zur Sicherheit. Da es sich um einen objektbasierten Ansatz zur Schemabearbeitung handelt, können Sie Code erstellen, der für verschiedene Datenquellen verwendet werden kann, ungeachtet der Unterschiede in der jeweiligen Syntax.

ADOX ist eine Begleitbibliothek zu ADO-Kernobjekten. Hiermit werden zusätzliche Objekte für das Erstellen, Ändern und Löschen von Schemaobjekten wie Tabellen und Prozeduren verfügbar gemacht. Außerdem enthält dieses Element Sicherheitsobjekte, um Benutzer und Gruppen zu warten und um Berechtigungen für Objekte zu erteilen und aufzuheben.

