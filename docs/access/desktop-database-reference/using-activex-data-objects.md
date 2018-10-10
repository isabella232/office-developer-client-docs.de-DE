---
title: Verwenden von ActiveX Data Objects (ADO)
TOCTitle: Using ActiveX Data Objects
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1f7c57ca785e115e9278145921bf50e8afe870ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473774"
---
# <a name="using-activex-data-objects"></a>Verwenden von ActiveX Data Objects (ADO)


**Betrifft**: Access 2013 | Office 2013

Microsoft Access enthält drei Objektmodelle, die Sie beim Erstellen, Warten und Verwalten Ihrer Access-Datenbanken und der zugehörigen Daten mit Visual Basic verwenden können.

## <a name="microsoft-activex-data-objects-ado"></a>Microsoft ActiveX Data-Objekte (ADO)

ADO enthält die Objekte, die zum Erstellen, Pflegen und Löschen von Datensätzen in einer bestimmten Datenquelle erforderlich sind.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext. for DDL and Security (ADOX)

ADOX stellt die DDL (Data Definition Language)-Objekte bereit, die zum Erstellen einer neuen Datenbank und der darin enthaltenen Objekte zusätzlich zu den zum Verwalten der Zugriffsrechte benötigten Objekten erforderlich sind.

**Microsoft Jet and Replication Objects 2.5 Library (JRO)**

Da ADO-Objekte für die Zusammenarbeit mit vielen Datenbanken neben den Microsoft Jet-Datenbanken konzipiert wurden, wurde die Jet-spezifische Funktionalität in die JRO-Bibliothek verlagert.

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
(Nur des MDB)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Erstellen von Datensatzgruppen</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten von Starteigenschaften</p></td>
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Unterstützung von ANSI92 SQL***</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Erstellen von Tabellen</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Erstellen einer neuen Datenbank</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten vorhandener Tabelleneigenschaften</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Erstellen von Tabellenbeziehungen</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten von Sicherheitseinstellungen</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Unterstützung des Attributs Compression für Spaltendaten</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten gespeicherter SQL-Standardabfragen oder -ansichten</p></td>
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
<td><p>Komprimieren/Verschlüsseln von Datenbanken</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Aktualisieren des Cachespeichers</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>Datenbank replizierbar machen</p></td>
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
<td><p>Bearbeiten von Datenbankeigenschaften</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Erstellen benutzerdefinierter Datenbankeigenschaften</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Bearbeiten von Tabellenspalteneigenschaften</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Nur verfügbar beim Arbeiten mit Microsoft Access-Datenbanken. Zukünftige Versionen des SQL-Providers stellen diese Funktionalität möglicherweise auch in Microsoft Access-Projekten (ADP) bereit.

\*\* Nur verfügbar beim Arbeiten mit Access-Projekten.

\*\*\* Obwohl das Access-Datenbankmodul ANSI 92 SQL teilweise unterstützt, ist es noch nicht vollständig ANSI92-kompatibel.

1Verweist mithilfe des **Connection** -Objekts auf Datenbank

2Verweist mithilfe des **Catalog** -Objekts auf Datenbank

3Verweist mithilfe des **Replica** -Objekts auf Datenbank

4Verweist mithilfe des **JetEngine** -Objekts auf Datenbank


> [!NOTE]
> <P>[!HINWEIS] Im Gegensatz zu DAO können ADO- and ADOX-Objekte die gekennzeichneten Aktionen in anderen Datenbanken als Jet-Datenbanken ausführen, sofern der Provider für diese Datenbanken die betreffende Aktion unterstützt.</P>


