---
title: Verwenden von ADO (ActiveX Data Objects)
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access bietet drei Objektmodelle für die Erstellung, Verwaltung und Verwaltung Ihrer Access-Datenbanken und der zugehörigen Daten mithilfe von Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 7f17eb51a0cd1e7dbbafb145d64b2f66716d88f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588938"
---
# <a name="use-activex-data-objects"></a>Verwenden von ADO (ActiveX Data Objects)

**Gilt für**: Access 2013, Office 2013

Microsoft Access bietet drei Objektmodelle für die Erstellung, Verwaltung und Verwaltung Ihrer Access-Datenbanken und der zugehörigen Daten mithilfe von Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Microsoft ActiveX Data-Objekte (ADO)

ADO enthält die Objekte, die zum Erstellen, Pflegen und Löschen von Datensätzen in einer bestimmten Datenquelle erforderlich sind.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO ext. for DDL and security (ADOX)

ADOX stellt die Datendefinitionssprache -Objekte (Data Definition Language, DDL) bereit, die zum Erstellen einer neuen Datenbank und der darin enthaltenen Objekte zusätzlich zu den Objekten erforderlich sind, die zum Verwalten der Sicherheit erforderlich sind.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Microsoft Jet and Replication Objects 2.5 library (JRO)

Da ADO-Objekte für die Verwendung mit vielen Datenbanken zusätzlich zu Microsoft Jet-Datenbanken entwickelt wurden, wurde die jetspezifische Funktionalität in die JRO-Bibliothek aufgeteilt.

Die folgende Liste listet die von jedem der neuen Objektmodelle bereitgestellten Funktionen im Vergleich zu DAO auf.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Funktionalität</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
(nur MDBs)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Recordsets erstellen.</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten von Starteigenschaften.</p></td>
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Ansi92-SQL unterstützen.</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Tabellen erstellen.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Erstellen sie eine neue Datenbank.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten vorhandener Tabelleneigenschaften.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Tabellenbeziehungen erstellen.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Sicherheitseinstellungen bearbeiten.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Unterstützung des Komprimierungsattributs für Spaltendaten.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten gespeicherter, einfacher SQL Abfragen oder Ansichten.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Erstellen permanenter Abfragen, auf die nur über Code zugegriffen werden kann</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Erstellen von Abfragen, auf die über Datenbankcontainer/UI und Code zugegriffen werden kann</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Datenbank komprimieren/codieren.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Cache aktualisieren.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>Datenbank replizierbar machen.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Erstellen von Datenbankreplikaten.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Synchronisieren von Replikaten.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten von Datenbankeigenschaften.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Erstellen sie benutzerdefinierte Datenbankeigenschaften.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten von Tabellenspalteneigenschaften.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Nur verfügbar beim Arbeiten mit Microsoft Access-Datenbanken. Zukünftige Versionen des SQL-Providers stellen diese Funktionalität möglicherweise auch in Microsoft Access-Projekten (ADP) bereit.

\*\* Nur verfügbar beim Arbeiten mit Access-Projekten.

\*\*\*Obwohl das Access-Datenbankmodul einige ANSI 92-SQL unterstützt, ist es noch nicht vollständig ANSI92-kompatibel.

1 Verwendet **das Connection-Objekt,** um auf die Datenbank zu verweisen.

2 Verwendet **das Catalog-Objekt,** um auf die Datenbank zu verweisen.

3 Verwendet **das Replica-Objekt,** um auf die Datenbank zu verweisen.

4 Verwendet das **JetEngine-Objekt,** um auf die Datenbank zu verweisen.


> [!NOTE]
> Im Gegensatz zu DAO können ADO- und ADOX-Objekte die markierten Aktionen in anderen Datenbanken als Jet ausführen, solange der Anbieter für diese Datenbanken diese Aktion unterstützt.


