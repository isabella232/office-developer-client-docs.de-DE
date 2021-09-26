---
title: 'Kapitel 15: Grundlegendes zu ADOX'
TOCTitle: 'Chapter 15: ADOX fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 952599694588c5535d8d6d9e205e45d67b8b3020
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627093"
---
# <a name="chapter-15-adox-fundamentals"></a>Kapitel 15: Grundlegendes zu ADOX

**Gilt für**: Access 2013, Office 2013

Microsoft ActiveX Data Objects Extensions für Datendefinitionssprache und Sicherheit (ADOX) ist eine Erweiterung der ADO-Objekte und des Programmiermodells. ADOX enthält Objekte zum Erstellen und Ändern von Schemas sowie zur Sicherheit. Da es sich um einen objektbasierten Ansatz zur Schemabearbeitung handelt, können Sie Code erstellen, der für verschiedene Datenquellen verwendet werden kann, ungeachtet der Unterschiede in der jeweiligen Syntax.

ADOX ist eine Begleitbibliothek zu ADO-Kernobjekten. Hiermit werden zusätzliche Objekte für das Erstellen, Ändern und Löschen von Schemaobjekten wie Tabellen und Prozeduren verfügbar gemacht. Außerdem enthält dieses Element Sicherheitsobjekte, um Benutzer und Gruppen zu warten und um Berechtigungen für Objekte zu erteilen und aufzuheben.

To use ADOX with your development tool, you should establish a reference to the ADOX type library. The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security." The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX". For more information about establishing references to libraries, see the documentation of your development tool.

Der Microsoft OLE DB-Anbieter für das Microsoft Jet-Datenbankmodul unterstützt ADOX vollständig. Abhängig vom jeweiligen Datenprovider werden bestimmte Features von ADOX möglicherweise nicht unterstützt. Weitere Informationen zu unterstützten Features mit dem Microsoft OLE DB-Anbieter für ODBC, dem Microsoft OLE DB-Anbieter für Oracle oder dem Microsoft SQL Server OLE DB-Anbieter finden Sie in der MDAC-Infodatei.

Dieses Dokument setzt Arbeitskenntnisse in der Programmiersprache Microsoft Visual Basic und allgemeine Kenntnisse von ADO voraus. Weitere Informationen zu ADO finden Sie im [ADO-Programmierhandbuch.](ado-programmer-s-guide.md)

In diesem Kapitel wird das folgende Thema behandelt:

- [Anbieterunterstützung für ADOX](provider-support-for-adox.md)

Weitere grundlegende Informationen zu ADOX finden Sie in den folgenden Themen:

- [ADOX-Objekte](adox-objects.md)
- [ADOX-Auflistungen](adox-collections.md)
- [ADOX-Eigenschaften](adox-properties.md)
- [ADOX-Methoden](adox-methods.md)
- [ADOX-Beispiele](adox-code-examples.md)

