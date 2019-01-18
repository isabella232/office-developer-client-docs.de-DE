---
title: Verwenden von ADO (ActiveX Data Objects)
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access enthält drei Objektmodelle, verwenden Sie bei der Erstellung, warten und Verwalten Ihrer Access-Datenbanken und der zugehörigen Daten mithilfe von Visual Basic.
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719225"
---
# <a name="use-activex-data-objects"></a>Verwenden von ADO (ActiveX Data Objects)

**Betrifft**: Access 2013, Office 2013

Microsoft Access enthält drei Objektmodelle, verwenden Sie bei der Erstellung, warten und Verwalten Ihrer Access-Datenbanken und der zugehörigen Daten mithilfe von Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Microsoft ActiveX Data-Objekte (ADO)

ADO enthält die Objekte, die zum Erstellen, Pflegen und Löschen von Datensätzen in einer bestimmten Datenquelle erforderlich sind.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext Sicherheit (ADOX)

ADOX stellt die Datendefinitionssprache (Data Definition Language, DDL)-Objekte, die erforderlich sind, zum Erstellen einer neuen Datenbank und der darin enthaltenen Objekte zusätzlich zu den zum Verwalten der Sicherheit bereit.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Microsoft Jet and Replication Objects 2.5-Bibliothek (JRO)

Da ADO-Objekte für die Arbeit mit vielen Datenbanken neben den Microsoft Jet-Datenbanken konzipiert wurden, wurde die Jet-spezifische Funktionalität in die JRO-Bibliothek verlagert.

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
<th><p>Funktion</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
(Nur MDBs)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Erstellen von Datensatzgruppen.</p></td>
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
<td><p>Unterstützung von ANSI92 SQL.* **</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Erstellen von Tabellen.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Erstellen Sie neue Datenbank.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten Sie vorhandener Tabelleneigenschaften.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Erstellen von tabellenbeziehungen.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten von Sicherheitseinstellungen.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Unterstützung des Attributs Compression für Spaltendaten.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten Sie gespeicherter SQL-Standardabfragen oder-Ansichten.</p></td>
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
<td><p>Codieren Sie komprimieren/Datenbank.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Aktualisieren des Cachespeichers.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>Machen Sie Datenbank replizierbar.</p></td>
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
<td><p>Erstellen Sie benutzerdefinierter Datenbankeigenschaften.</p></td>
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

\*\*\*Obwohl das Access-Datenbankmodul ANSI 92 SQL unterstützt werden, ist es noch nicht vollständig ANSI92-kompatibel.

1 verwendet **Connection** -Objekts auf Datenbank.

2 verwendet **Catalog** -Objekts auf Datenbank.

3 verwendet **Replikat** -Objekts auf Datenbank.

4 verwendet **JetEngine** -Objekts auf Datenbank.


> [!NOTE]
> Im Gegensatz zu DAO können ADO- and ADOX-Objekte die gekennzeichneten Aktionen in Datenbanken als Jet ausführen, solange der Provider für diese Datenbanken die betreffende Aktion unterstützt.


