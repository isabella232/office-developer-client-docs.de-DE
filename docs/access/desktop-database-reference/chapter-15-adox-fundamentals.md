---
title: 'Kapitel 15: Grundlegendes zu ADOX'
TOCTitle: 'Chapter 15: ADOX fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e46920ba47dba018944768ff61c970781e37a02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296451"
---
# <a name="chapter-15-adox-fundamentals"></a>Kapitel 15: Grundlegendes zu ADOX

**Gilt für**: Access 2013, Office 2013

Microsoft ActiveX Data Objects Extensions für Datendefinitionssprache und Sicherheit (ADOX) ist eine Erweiterung der ADO-Objekte und des Programmiermodells. ADOX enthält Objekte zum Erstellen und Ändern von Schemas sowie zur Sicherheit. Da es sich um einen objektbasierten Ansatz zur Schemabearbeitung handelt, können Sie Code erstellen, der für verschiedene Datenquellen verwendet werden kann, ungeachtet der Unterschiede in der jeweiligen Syntax.

ADOX ist eine Begleitbibliothek zu ADO-Kernobjekten. Hiermit werden zusätzliche Objekte für das Erstellen, Ändern und Löschen von Schemaobjekten wie Tabellen und Prozeduren verfügbar gemacht. Außerdem enthält dieses Element Sicherheitsobjekte, um Benutzer und Gruppen zu warten und um Berechtigungen für Objekte zu erteilen und aufzuheben.

To use ADOX with your development tool, you should establish a reference to the ADOX type library. The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security." The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX". For more information about establishing references to libraries, see the documentation of your development tool.

Der Microsoft OLE DB-Anbieter für das Microsoft Jet-Datenbankmodul unterstützt ADOX vollständig. Abhängig vom jeweiligen Datenprovider werden bestimmte Features von ADOX möglicherweise nicht unterstützt. Weitere Informationen zu unterstützten Features mit dem Microsoft OLE DB-Anbieter für ODBC, dem Microsoft OLE DB-Anbieter für Oracle oder dem Microsoft SQL Server OLE DB-Anbieter finden Sie in der MDAC-Infodatei.

In diesem Dokument werden Kenntnisse der Microsoft Visual Basic-Programmiersprache und allgemeine ADO-Kenntnisse vorausgesetzt. Weitere Informationen zu ADO finden Sie im [ADO-Programmierhandbuch](ado-programmer-s-guide.md).

In diesem Kapitel wird Folgendes Thema behandelt:

- [Anbieterunterstützung für ADOX](provider-support-for-adox.md)

Weitere grundlegende Informationen zu ADOX finden Sie in den folgenden Themen:

- [ADOX-Objekte](adox-objects.md)
- [ADOX-Auflistungen](adox-collections.md)
- [ADOX-Eigenschaften](adox-properties.md)
- [ADOX-Methoden](adox-methods.md)
- [ADOX-Beispiele](adox-code-examples.md)

