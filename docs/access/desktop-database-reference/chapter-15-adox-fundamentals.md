---
title: 'Kapitel 15: Grundlegendes zu ADOX'
TOCTitle: 'Chapter 15: ADOX Fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 362fd0784ee596852af7b16fae5636330a52ed59
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863745"
---
# <a name="chapter-15-adox-fundamentals"></a>Kapitel 15: Grundlegendes zu ADOX


**Betrifft**: Access 2013 | Office 2013

Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) ist eine Erweiterung des ADO-Objekt- und Programmiermodells. ADOX umfasst Objekte für die Schemaerstellung und -bearbeitung sowie Sicherheitsobjekte. Da es sich um einen objektbasierten Ansatz für die Schemamanipulation handelt, können Sie Code schreiben, der für verschiedene Datenquellen verwendbar ist, unabhängig von Unterschieden der jeweiligen systemeigenen Syntax.

ADOX ist eine Begleitbibliothek zu den ADO-Hauptobjekten. ADOX stellt zusätzliche Objekte zum Erstellen, Bearbeiten und Löschen von Schemaobjekten wie Tabellen und Prozeduren bereit. Es schließt außerdem Sicherheitsobjekte zum Verwalten von Benutzern und Gruppen und zum Erteilen und Aufheben von Berechtigungen für Objekte ein.

Zur Verwendung von ADOX mit einem Entwicklungstool sollten Sie einen Verweis zur ADOX-Typbibliothek einrichten. Die Beschreibung der ADOX-Bibliothek finden Sie unter "Microsoft ADO Ext. for DDL and Security." Der Dateiname der ADOX-Bibliothek ist Msadox.dll. Die Programm-ID (ProgID) lautet "ADOX". Weitere Informationen zum Erstellen von Verweisen zu Bibliotheken finden Sie in der Dokumentation Ihres Entwicklungstools.

Der Microsoft OLE DB-Anbieter für das Microsoft Jet-Datenbankmodul unterstützt ADOX vollständig. Abhängig vom jeweiligen Datenprovider werden bestimmte Features von ADOX möglicherweise nicht unterstützt. Weitere Informationen zu unterstützten Features mit dem Microsoft OLE DB-Anbieter für ODBC, dem Microsoft OLE DB-Anbieter für Oracle oder dem Microsoft SQL Server OLE DB-Anbieter finden Sie in der MDAC-Infodatei.

Dieses Dokument setzt Erfahrung in der Verwendung der Programmiersprache Microsoft® Visual Basic® und grundlegende ADO-Kenntnisse voraus. Weitere Informationen zu ADO finden Sie im [ADO-Programmierhandbuch](ado-programmer-s-guide.md).

In diesem Kapitel werden die folgenden Themen behandelt:

- [Anbieterunterstützung für ADOX](provider-support-for-adox.md)

Weitere grundlegende Informationen zu ADOX finden Sie in den folgenden Themen:

- [ADOX-Objekte ](adox-objects.md)

- [ADOX-Auflistungen](adox-collections.md)

- [ADOX-Eigenschaften ](adox-properties.md)

- [ADOX-Methoden ](adox-methods.md)

- [ADOX-Beispiele ](adox-code-examples.md)

