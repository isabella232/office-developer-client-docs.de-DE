---
title: Gleichwertige ANSI SQL-Datentypen
TOCTitle: Equivalent ANSI SQL Data Types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e44ae29014870dcd4fc95629081d50191d6ff184
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863986"
---
# <a name="equivalent-ansi-sql-data-types"></a>Gleichwertige ANSI SQL-Datentypen


**Betrifft**: Access 2013 | Office 2013

In der folgenden Tabelle werden ANSI SQL-Datentypen, die gleichwertigen Datentypen für das Microsoft Access-Datenbankmodul SQL sowie die gültigen Synonyme aufgelistet. Zusätzlich werden die gleichwertigen Microsoft® SQL Server-Datentypen aufgelistet.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ANSI SQL-Datentyp</p></th>
<th><p>Microsoft Access SQL-Datentyp</p></th>
<th><p>
Synonym</p></th>
<th><p>Microsoft SQL Server-Datentyp</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BIT, BIT VARYING</p></td>
<td><p>BINARY (Siehe Hinweise)</p></td>
<td><p>VARBINARY, BINARY VARYING BIT VARYING</p></td>
<td><p>BINARY, VARBINARY</p></td>
</tr>
<tr class="even">
<td><p>Nicht unterstützt</p></td>
<td><p>BIT (Siehe Hinweise)</p></td>
<td><p>BOOLEAN, LOGICAL, LOGICAL1, YESNO</p></td>
<td><p>BIT</p></td>
</tr>
<tr class="odd">
<td><p>Nicht unterstützt</p></td>
<td><p>TINYINT</p></td>
<td><p>INTEGER1, BYTE</p></td>
<td><p>TINYINT</p></td>
</tr>
<tr class="even">
<td><p>Nicht unterstützt</p></td>
<td><p>COUNTER (Siehe Hinweise)</p></td>
<td><p>AUTOINCREMENT</p></td>
<td><p>(Siehe Hinweise)</p></td>
</tr>
<tr class="odd">
<td><p>Nicht unterstützt</p></td>
<td><p>MONEY</p></td>
<td><p>CURRENCY</p></td>
<td><p>MONEY</p></td>
</tr>
<tr class="even">
<td><p>DATE, TIME, TIMESTAMP</p></td>
<td><p>DATETIME</p></td>
<td><p>DATE, TIME (siehe Hinweise)</p></td>
<td><p>DATETIME</p></td>
</tr>
<tr class="odd">
<td><p>Nicht unterstützt</p></td>
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>GUID</p></td>
<td><p>UNIQUEIDENTIFIER</p></td>
</tr>
<tr class="even">
<td><p>DECIMAL</p></td>
<td><p>DECIMAL</p></td>
<td><p>NUMERIC, DEC</p></td>
<td><p>DECIMAL</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>REAL</p></td>
<td><p>SINGLE, FLOAT4, IEEESINGLE</p></td>
<td><p>REAL</p></td>
</tr>
<tr class="even">
<td><p>DOUBLE PRECISION, FLOAT</p></td>
<td><p>FLOAT</p></td>
<td><p>DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (Siehe Hinweise)</p></td>
<td><p>FLOAT</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>SMALLINT</p></td>
<td><p>SHORT, INTEGER2</p></td>
<td><p>SMALLINT</p></td>
</tr>
<tr class="even">
<td><p>INTEGER</p></td>
<td><p>INTEGER</p></td>
<td><p>LONG, INT, INTEGER4</p></td>
<td><p>INTEGER</p></td>
</tr>
<tr class="odd">
<td><p>INTERVAL</p></td>
<td><p>Nicht unterstützt</p></td>
<td><p></p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td><p>Nicht unterstützt</p></td>
<td><p>IMAGE</p></td>
<td><p>LONGBINARY GENERAL, OLEOBJECT</p></td>
<td><p>IMAGE</p></td>
</tr>
<tr class="odd">
<td><p>Nicht unterstützt</p></td>
<td><p>TEXT (siehe Hinweise)</p></td>
<td><p>LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (Siehe Hinweise)</p></td>
<td><p>TEXT</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</p></td>
<td><p>CHAR (Siehe Hinweise)</p></td>
<td><p>Text (n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (siehe Hinweise)</p></td>
<td><p>CHAR, VARCHAR, NCHAR, NVARCHAR</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - Der ANSI SQL BIT-Datentyp entspricht nicht dem Microsoft Access SQL BIT-Datentyp, sondern dem BINARY-Datentyp. Es gibt keinen gleichwertigen ANSI SQL-Datentyp für den Microsoft Access SQL BIT-Datentyp.
> - Der TIMESTAMP-Datentyp wird nicht mehr als ein Synonym des DATETIME-Datentyps unterstützt.
> - Der NUMERIC-Datentyp wird nicht mehr als ein Synonym der Datentypen FLOAT oder DOUBLE unterstützt. Der NUMERIC-Datentyp wird jetzt als ein Synonym des DECIMAL-Datentyps unterstützt.
> - Ein LONGTEXT-Feld wird immer im Unicode-Darstellungsformat gespeichert.
> - Wird der TEXT-Datentypname ohne Angabe der optionalen Länge verwendet, zum Beispiel TEXT(25), wird ein LONGTEXT-Feld erstellt. Auf diese Weise können [CREATE TABLE-Anweisungen](create-table-statement-microsoft-access-sql.md) geschrieben werden, die Microsoft SQL Server-konsistente Datentypen generieren.
> - Ein CHAR-Feld wird immer im Unicode-Darstellungsformat gespeichert, das gleichwertig mit dem ANSI SQL NATIONAL CHAR-Datentyp ist.
> - Wird der TEXT-Datentypname unter Angabe der optionalen Länge verwendet, zum Beispiel TEXT(25), ist der Datentyp des Felds gleichwertig mit dem CHAR-Datentyp. Auf diese Weise wird die Abwärtskompatibilität für die meisten Microsoft Jet-Anwendungen gewährleistet und ermöglicht, dass der TEXT-Datentyp (ohne Längenangabe) auf Microsoft SQL Server ausgerichtet werden kann.


