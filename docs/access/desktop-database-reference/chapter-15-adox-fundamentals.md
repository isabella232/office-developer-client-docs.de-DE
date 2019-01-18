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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720975"
---
# <a name="chapter-15-adox-fundamentals"></a>Kapitel 15: Grundlegendes zu ADOX

**Betrifft**: Access 2013, Office 2013

Microsoft ActiveX Data Objects Extensions für Datendefinitionssprache und Sicherheit (ADOX) ist eine Erweiterung der ADO-Objekte und des Programmiermodells. ADOX enthält Objekte zum Erstellen und Ändern von Schemas sowie zur Sicherheit. Da es sich um einen objektbasierten Ansatz zur Schemabearbeitung handelt, können Sie Code erstellen, der für verschiedene Datenquellen verwendet werden kann, ungeachtet der Unterschiede in der jeweiligen Syntax.

ADOX ist eine Begleitbibliothek zu den ADO-Hauptobjekten. ADOX stellt zusätzliche Objekte zum Erstellen, Bearbeiten und Löschen von Schemaobjekten wie Tabellen und Prozeduren bereit. Es schließt außerdem Sicherheitsobjekte zum Verwalten von Benutzern und Gruppen und zum Erteilen und Aufheben von Berechtigungen für Objekte ein.

Zur Verwendung von ADOX mit einem Entwicklungstool sollten Sie einen Verweis zur ADOX-Typbibliothek einrichten. Die Beschreibung der ADOX-Bibliothek finden Sie unter "Microsoft ADO Ext. for DDL and Security." Der Dateiname der ADOX-Bibliothek ist Msadox.dll. Die Programm-ID (ProgID) lautet "ADOX". Weitere Informationen zum Erstellen von Verweisen zu Bibliotheken finden Sie in der Dokumentation Ihres Entwicklungstools.

Der Microsoft OLE DB-Anbieter für das Microsoft Jet-Datenbankmodul unterstützt ADOX vollständig. Abhängig vom jeweiligen Datenprovider werden bestimmte Features von ADOX möglicherweise nicht unterstützt. Weitere Informationen zu unterstützten Features mit dem Microsoft OLE DB-Anbieter für ODBC, dem Microsoft OLE DB-Anbieter für Oracle oder dem Microsoft SQL Server OLE DB-Anbieter finden Sie in der MDAC-Infodatei.

In diesem Dokument wird davon ausgegangen Kenntnisse in der Programmiersprache Microsoft Visual Basic sowie allgemeine Kenntnisse von ADO. Weitere Informationen zu ADO finden Sie in der [ADO-Programmierhandbuch](ado-programmer-s-guide.md).

In diesem Kapitel werden die folgenden Themen behandelt:

- [Anbieterunterstützung für ADOX](provider-support-for-adox.md)

Weitere grundlegende Informationen zu ADOX finden Sie in den folgenden Themen:

- [ADOX-Objekte](adox-objects.md)
- [ADOX-Auflistungen](adox-collections.md)
- [ADOX-Eigenschaften](adox-properties.md)
- [ADOX-Methoden](adox-methods.md)
- [ADOX-Beispiele](adox-code-examples.md)

