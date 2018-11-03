---
title: SQL-Datentypen (Access PC-Datenbank-Referenz)
TOCTitle: SQL Data Types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
ms.openlocfilehash: cfaecd26ebd3f747a0e2db2ec530c151928fec74
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936910"
---
# <a name="sql-data-types"></a>SQL-Datentypen


**Betrifft**: Access 2013, Office 2013

Microsoft Access-Datenbank-Engine SQL-Datentypen bestehen aus 13 vom Microsoft Jet-Datenbankmodul definierten primären Datentypen und mehreren gültigen Synonymen für diese Datentypen erkannt.

In der folgenden Tabelle werden die primären Datentypen aufgelistet. Die Synonyme werden unter [Reservierte Wörter für das Microsoft Access-Datenbankmodul SQL](sql-reserved-words.md) angegeben.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Datentyp</p></th>
<th><p>Speichergröße</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BINARY</p></td>
<td><p>1 Byte pro Zeichen</p></td>
<td><p>In einem Feld dieses Datentyps kann ein beliebiges Zeichen gespeichert werden. Es erfolgt keine Übersetzung der Daten (zum Beispiel in Text). Die Daten in einem binären Feld werden so angezeigt wie sie eingegeben wurden.</p></td>
</tr>
<tr class="even">
<td><p>BIT</p></td>
<td><p>1 Byte</p></td>
<td><p>Felder mit den Werten Ja oder Nein, die jeweils nur einen der beiden Werte enthalten können.</p></td>
</tr>
<tr class="odd">
<td><p>TINYINT</p></td>
<td><p>1 Byte</p></td>
<td><p>Ein Wert bestehend aus einer ganzen Zahl zwischen 0 und 255.</p></td>
</tr>
<tr class="even">
<td><p>MONEY</p></td>
<td><p>8 Bytes</p></td>
<td><p>Eine skalierte ganze Zahl zwischen – 922,337,203,685,477.5808 und 922,337,203,685,477.5807.</p></td>
</tr>
<tr class="odd">
<td><p>DATETIME (siehe DOUBLE)</p></td>
<td><p>8 Bytes</p></td>
<td><p>Ein Datum- oder Uhrzeitwert, der zwischen der Jahresangabe 100 und 9999 liegt.</p></td>
</tr>
<tr class="even">
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>128 Bit</p></td>
<td><p>Eine eindeutige ID-Nummer, die für Remoteprozeduraufrufe verwendet wird.</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>4 Bytes</p></td>
<td><p>Ein Wert, der aus einer Gleitkommazahl mit einfacher Genauigkeit besteht und für negative Werte in einem Bereich von – 3.402823E38 bis – 1.401298E-45, für positive Werte in einem Bereich von 1.401298E-45 bis 3.402823E38 liegt oder den Wert 0 annehmen kann.</p></td>
</tr>
<tr class="even">
<td><p>FLOAT</p></td>
<td><p>8 Bytes</p></td>
<td><p>Ein Wert, der aus einer Gleitkommazahl mit doppelter Genauigkeit besteht und für negative Werte in einem Bereich von – 1.79769313486232E308 bis – 4.94065645841247E-324, für positive Werte in einem Bereich von 4.94065645841247E-324 bis 1.79769313486232E308 liegt und den Wert 0 annehmen kann.</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>2 Bytes</p></td>
<td><p>Eine ganze Zahl vom Short Integer-Datentyp zwischen – 32,768 und 32,767. (Siehe Hinweise)</p></td>
</tr>
<tr class="even">
<td><p>INTEGER</p></td>
<td><p>4 Bytes</p></td>
<td><p>Eine ganze Zahl vom Long Integer-Datentyp zwischen – 2,147,483,648 und 2,147,483,647. (Siehe Hinweise)</p></td>
</tr>
<tr class="odd">
<td><p>DECIMAL</p></td>
<td><p>17 Bytes</p></td>
<td><p>Ein Datentyp zur Angabe eines exakten numerischen Werts von 1028 - 1 bis - 1028 - 1. Sie können für diesen Wert eine Genauigkeit (1 - 28) und eine Skala (0 - definierte Genauigkeit) definieren. Die Standardwerte für Genauigkeit und Skala sind jeweils 18 und 0.</p></td>
</tr>
<tr class="even">
<td><p>TEXT</p></td>
<td><p>2 Bytes pro Zeichen (Siehe Hinweise)</p></td>
<td><p>Null bis maximal 2,14 Gigabytes.</p></td>
</tr>
<tr class="odd">
<td><p>IMAGE</p></td>
<td><p>Wie erforderlich</p></td>
<td><p>Null bis maximal 2,14 Gigabytes. Verwendung für OLE-Objekte.</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER</p></td>
<td><p>2 Byte pro Zeichen. (Siehe Hinweise)</p></td>
<td><p>Null bis 255 Zeichen.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <UL>
> <LI>
> <P>Sowohl der Ausgangswert als auch der inkrementelle Werte können unter Verwendung der <A href="alter-table-statement-microsoft-access-sql.md">ALTER TABLE-Anweisung</A> geändert werden. Neue Zeilen, die in die Tabelle eingefügt werden, weisen Werte auf, die auf den neuen Ausgangs- bzw. inkrementellen Werten basieren und die automatisch für die Spalte generiert werden. Wenn basierend auf den neuen Ausgangs- bzw. inkrementellen Werten Werte generiert werden können, die auf vorhergehenden Ausgangs- bzw. inkrementellen Werten basieren, werden Duplikate generiert. Handelt es sich bei der Spalte um einen Primärschlüssel, kann beim Einfügen neuer Zeilen ein Fehler verursacht werden, wenn duplizierte Werte generiert wurden.</P>
> <LI>
> <P>Verwenden Sie die SELECT @@IDENTITY-Anweisung, um den letzten Wert zu ermitteln, der für automatisch inkrementierte Spalten generiert wurde. Es ist nicht möglich, einen Tabellennamen anzugeben. Der zurückgegebene Wert stammt aus der Tabelle mit einer automatisch inkrementierten Spalte, die zuletzt aktualisiert wurde.</P></LI></UL>


