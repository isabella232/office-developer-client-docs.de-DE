---
title: SQL-Datentypen (Access-Desktopdatenbankreferenz)
TOCTitle: SQL data types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: fb72a0090550692e7cf5028a6a58a078fc5d9d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308582"
---
# <a name="sql-data-types"></a>SQL-Datentypen

**Gilt für**: Access 2013, Office 2013

Die SQL-Datentypen für das Microsoft Access-Datenbankmodul bestehen aus 13 primären Datentypen. Diese Datentypen werden von dem Microsoft Jet-Datenbankmodul und verschiedenen gültigen Synonymen für diese Datentypen definiert.

In der folgenden Tabelle werden die primären Datentypen aufgeführt. Die Synonyme werden unter [Reservierte Wörter für das Microsoft Access-Datenbankmodul SQL](sql-reserved-words.md) angegeben.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Datentyp</p></th>
<th><p>Speicherbedarf</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BINARY</p></td>
<td><p>1 Byte pro Zeichen</p></td>
<td><p>In einem Feld dieses Typs können beliebige Datentypen gespeichert werden. Es erfolgt keine Konvertierung der Daten (z. B. in Text). Die Art und Weise, wie die Daten in ein binäres Feld eingegeben werden, bestimmt, wie sie als Ausgabe angezeigt werden.</p></td>
</tr>
<tr class="even">
<td><p>BIT</p></td>
<td><p>1 Byte</p></td>
<td><p>Ja- und Nein-Werte sowie Felder, die nur einen von zwei Werten enthalten.</p></td>
</tr>
<tr class="odd">
<td><p>TINYINT</p></td>
<td><p>1 Byte</p></td>
<td><p>Ein ganzzahliger Wert von 0 bis 255.</p></td>
</tr>
<tr class="even">
<td><p>MONEY</p></td>
<td><p>8 Bytes</p></td>
<td><p>Eine skalierte ganze Zahl zwischen – 922,337,203,685,477.5808 und 922,337,203,685,477.5807.</p></td>
</tr>
<tr class="odd">
<td><p>DATETIME (Siehe DOUBLE)</p></td>
<td><p>8 Bytes</p></td>
<td><p>Ein Datums- oder Uhrzeitwert zwischen den Jahren 100 und 9999.</p></td>
</tr>
<tr class="even">
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>128 Bits</p></td>
<td><p>Eine bei Remoteprozeduraufrufen verwendete eindeutige Identifikationsnummer.</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>4 Byte</p></td>
<td><p>Ein Gleitkommawert mit einfacher Genauigkeit von -3,402823E38 bis -1,401298E-45 für negative Wert und 1,401298E-45 bis 3,402823E38 für positive Werte und 0.</p></td>
</tr>
<tr class="even">
<td><p>FLOAT</p></td>
<td><p>8 Byte</p></td>
<td><p>Ein Gleitkommawert mit doppelter Genauigkeit von -1,79769313486232E308 bis -4,94065645841247E-324 für negative Werte und 4,94065645841247E-324 bis 1,79769313486232E308 für positive Werte und 0.</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>2 Byte</p></td>
<td><p>Eine ganze Zahl vom Short Integer-Datentyp zwischen – 32,768 und 32,767. (Siehe Hinweise)</p></td>
</tr>
<tr class="even">
<td><p>INTEGER</p></td>
<td><p>4 Byte</p></td>
<td><p>Eine ganze Zahl vom Long Integer-Datentyp zwischen – 2,147,483,648 und 2,147,483,647. (Siehe Hinweise)</p></td>
</tr>
<tr class="odd">
<td><p>DECIMAL</p></td>
<td><p>17 Byte</p></td>
<td><p>Ein genauer numerischer Datentyp, der Werte von 1028-1 bis -1028-1 enthält. Sie können die Genauigkeit (1-28) und die Dezimalstellen (0 - definierte Genauigkeit) definieren. Die Standardwerte für Genauigkeit und Dezimalstellen sind 18 und 0.</p></td>
</tr>
<tr class="even">
<td><p>TEXT</p></td>
<td><p>2 Bytes pro Zeichen (Siehe Hinweise)</p></td>
<td><p>0 bis maximal 2,14 Gigabyte.</p></td>
</tr>
<tr class="odd">
<td><p>IMAGE</p></td>
<td><p>Je nach Bedarf</p></td>
<td><p>0 bis maximal 2,14 Gigabyte. Wird für OLE-Objekte verwendet.</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER</p></td>
<td><p>2 Byte pro Zeichen. (Siehe Hinweise)</p></td>
<td><p>0 bis 255 Zeichen.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> - Sowohl der Ausgangswert als auch der inkrementelle Werte können unter Verwendung der [ALTER TABLE-Anweisung](alter-table-statement-microsoft-access-sql.md) geändert werden. Neue Zeilen, die in die Tabelle eingefügt werden, weisen Werte auf, die auf den neuen Ausgangs- bzw. inkrementellen Werten basieren und die automatisch für die Spalte generiert werden. Wenn basierend auf den neuen Ausgangs- bzw. inkrementellen  Werten Werte generiert werden können, die auf vorhergehenden Ausgangs- bzw. inkrementellen Werten basieren, werden Duplikate generiert. Handelt es sich bei der Spalte um einen Primärschlüssel, kann beim Einfügen neuer Zeilen ein Fehler verursacht werden, wenn duplizierte Werte generiert wurden.
> - Verwenden Sie die SELECT @@IDENTITY-Anweisung, um den letzten Wert zu ermitteln, der für automatisch inkrementierte Spalten generiert wurde. Es ist nicht möglich, einen Tabellennamen anzugeben. Der zurückgegebene Wert stammt aus der Tabelle mit einer automatisch inkrementierten Spalte, die zuletzt aktualisiert wurde.
