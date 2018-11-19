---
title: Aggregatfunktionen, die CALC-Funktion und das NEUE Schlüsselwort
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb3e667a23d5bfd1d3dda5b4eb8dbd60a47e36ba
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025987"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a>Aggregatfunktionen, die CALC-Funktion und das NEUE Schlüsselwort


**Betrifft**: Access 2013, Office 2013

Die Datenstrukturierung unterstützt die folgenden Funktionen. Der Name, der dem Kapitel mit der zu bearbeitenden Spalte zugewiesen wird, ist der *Kapitelalias*.

Ein Kapitelalias kann vollqualifiziert sein und aus den verschiedenen Kapitelspaltennamen bestehen, die zu dem jeweiligen Kapitel führen, das den Spaltennamen enthält, wobei alle Elemente durch Punkte voneinander getrennt werden. Wenn z. B. das übergeordnete Kapitel chap1 das untergeordnete Kapitel chap2 mit einer Spalte für den Betrag (amt) enthält, würde der qualifizierte Name chap1.chap2.amt lauten.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aggregatfunktionen</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SUM (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</p></td>
<td><p>Berechnet die Summe aller Werte in der angegebenen Spalte.</p></td>
</tr>
<tr class="even">
<td><p>AVG (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</p></td>
<td><p>Berechnet den Mittelwert aller Werte in der angegebenen Spalte.</p></td>
</tr>
<tr class="odd">
<td><p>MAX (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</p></td>
<td><p>Berechnet den Maximalwert in der angegebenen Spalte.</p></td>
</tr>
<tr class="even">
<td><p>MIN (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</p></td>
<td><p>Berechnet den Minimalwert in der angegebenen Spalte.</p></td>
</tr>
<tr class="odd">
<td><p>COUNT (<em>Kapitel-Alias</em>[.<em> Spaltenname</em>])</p></td>
<td><p>Berechnet die Anzahl von Zeilen im angegebenen Alias. Falls eine Spalte angegeben wird, werden nur Zeilen, für die diese Spalte ungleich NULL ist, in die Anzahl eingeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>STDEV (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</p></td>
<td><p>Berechnet die Standardabweichung in der angegebenen Spalte.</p></td>
</tr>
<tr class="odd">
<td><p>Alle (<em>Kapitel-Alias</em>.<em> Spaltenname</em>)</p></td>
<td><p>Ein Wert der angegebenen Spalte. ANY hat nur dann einen vorhersagbaren Wert, wenn der Wert der Spalte für alle Zeilen im Kapitel identisch ist.
</p><p><strong>Hinweis</strong>: Wenn die Spalte nicht den gleichen Wert für alle Zeilen im Kapitel enthält, gibt der SHAPE-Befehl willkürlich einen der Werte der Wert der ANY-Funktion werden.</p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Berechneter Ausdruck</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CALC(<em>Ausdruck</em>)</p></td>
<td><p>Berechnet einen beliebigen Ausdruck, jedoch nur in der Zeile des <strong>Recordset</strong>-Objekts, das die CALC-Funktion enthält. Jeder Ausdruck, der diese <a href="visual-basic-for-applications-functions.md">VIA-Funktionen (Visual Basic für Applikationen)</a> verwendet, ist zulässig.</p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>NEW-Schlüsselwort</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NEW <em>Feldtyp</em> [(<em>Breite</em> | <em>Skalierung</em> | <em>Genauigkeit</em> | <em>Fehler</em> [, <em>Scale</em> | <em>Fehler</em>])]</p></td>
<td><p>Fügt dem <strong>Recordset</strong> eine leere Spalte des angegebenen Typs hinzu.</p></td>
</tr>
</tbody>
</table>

<br/>

Für den mit dem NEW-Schlüsselwort übergebenen *Feldtyp* sind die folgenden Datentypen möglich.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>OLE DB-Datentypen</p></th>
<th><p>ADO-Datentypentsprechung(en)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBTYPE_BSTR</p></td>
<td><p>adBSTR</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_BOOL</p></td>
<td><p>adBoolean</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DECIMAL</p></td>
<td><p>adDecimal</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI1</p></td>
<td><p>adUnsignedTinyInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_I1</p></td>
<td><p>adTinyInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI2</p></td>
<td><p>adUnsignedSmallInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI4</p></td>
<td><p>adUnsignedInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_I8</p></td>
<td><p>adBigInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI8</p></td>
<td><p>adUnsignedBigInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_GUID</p></td>
<td><p>adGuid</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_BYTES</p></td>
<td><p>AdBinary, AdVarBinary, adLongVarBinary</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_STR</p></td>
<td><p>AdChar, AdVarChar, adLongVarChar</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_WSTR</p></td>
<td><p>AdWChar, AdVarWChar, adLongVarWChar</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_NUMERIC</p></td>
<td><p>adNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBDATE</p></td>
<td><p>adDBDate</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_DBTIME</p></td>
<td><p>adDBTime</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBTIMESTAMP</p></td>
<td><p>adDBTimeStamp</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_VARNUMERIC ENTSPRECHENDE</p></td>
<td><p>adVarNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_FILETIME</p></td>
<td><p>adFileTime</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_ERROR</p></td>
<td><p>adError</p></td>
</tr>
</tbody>
</table>


Wenn das neue Feld vom Typ Decimal ist (in OLE DB DATENBANKTYP\_Dezimal oder AdDecimal in ADO), müssen Sie die Genauigkeit und einem festen Maßstab Werte angeben.

