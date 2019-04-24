---
title: Verwenden von ADO (ActiveX Data Objects)
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access bietet drei Objektmodelle, die Sie bei der Erstellung, Wartung und Verwaltung Ihrer Access-Datenbanken und der dazugehörigen Daten mithilfe von Visual Basic verwenden können.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3b530db43a816e66b9fbef254984142aadf0b841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312740"
---
# <a name="use-activex-data-objects"></a>Verwenden von ADO (ActiveX Data Objects)

**Gilt für**: Access 2013, Office 2013

Microsoft Access bietet drei Objektmodelle, die Sie bei der Erstellung, Wartung und Verwaltung Ihrer Access-Datenbanken und der dazugehörigen Daten mithilfe von Visual Basic verwenden können.

## <a name="microsoft-activex-data-objects-ado"></a>Microsoft ActiveX Data-Objekte (ADO)

ADO enthält die Objekte, die zum Erstellen, Pflegen und Löschen von Datensätzen in einer bestimmten Datenquelle erforderlich sind.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO extern für DDL und Sicherheit (ADOX)

ADOX stellt die DDL-Objekte (Data Definition Language) bereit, die zum Erstellen einer neuen Datenbank und der enthaltenen Objekte zusätzlich zu den zum Verwalten der Sicherheit erforderlichen Objekten erforderlich sind.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Microsoft Jet-und Replication Objects 2,5-Bibliothek (JRO)

Da ADO-Objekte zusätzlich zu Microsoft Jet-Datenbanken für die Zusammenarbeit mit vielen Datenbanken entworfen wurden, wurde die Jet-Funktionalität in die JRO-Bibliothek aufgeteilt.

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
(Nur MDBs)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Erstellen Sie Recordsets.</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten von Starteigenschaften.</p></td>
<td><p>X</p></td>
<td><p>X * *</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Unterstützung von ANSI92 SQL. * * *</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Erstellen Sie Tabellen.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Erstellen Sie eine neue Datenbank.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
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
<td><p>Erstellen von Tabellenbeziehungen.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten von Sicherheitseinstellungen</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Unterstützung für das Komprimierungsattribut für Spaltendaten.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten gespeicherter, einfacher SQL-Abfragen oder-Ansichten.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Erstellen permanenter Abfragen, auf die nur über Code zugegriffen werden kann</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
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
<td><p>Komprimieren/Codieren der Datenbank.</p></td>
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
<td><p>Erstellen von Datenbankreplikaten</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Synchronisieren von Replikaten</p></td>
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
<td><p>Erstellen benutzerdefinierter Datenbankeigenschaften.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Tabellenspalteneigenschaften bearbeiten.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Nur verfügbar beim Arbeiten mit Microsoft Access-Datenbanken. Zukünftige Versionen des SQL-Providers stellen diese Funktionalität möglicherweise auch in Microsoft Access-Projekten (ADP) bereit.

\*\* Nur verfügbar beim Arbeiten mit Access-Projekten.

\*\*\*Obwohl das Access-Datenbankmodul einige ANSI 92 SQL unterstützt, ist es noch nicht vollständig ANSI92-kompatibel.

1 verwendet **Connection** -Objekt, um auf Datenbank zu verweisen.

2 verwendet das **catalog** -Objekt, um auf Datenbank zu verweisen.

3 verwendet das **Replica** -Objekt, um auf Datenbank zu verweisen.

4 verwendet das **JetEngine** -Objekt, um auf Datenbank zu verweisen.


> [!NOTE]
> Im Gegensatz zu DAO können ADO-und ADOX-Objekte die markierten Aktionen in anderen Datenbanken als Jet ausführen, sofern der Anbieter dieser Datenbanken diese Aktion unterstützt.


