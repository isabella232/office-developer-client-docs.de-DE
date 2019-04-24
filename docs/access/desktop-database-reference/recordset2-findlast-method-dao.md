---
title: Recordset2. FindLast-Methode (DAO)
TOCTitle: FindLast Method
ms:assetid: 6a31dd00-8e05-6226-ebd8-703d2562b5c7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195400(v=office.15)
ms:contentKeyID: 48545428
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e358459c1737cd6fff1484d1562dad02a7585337
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307322"
---
# <a name="recordset2findlast-method-dao"></a>Recordset2. FindLast-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Locates the last record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).

## <a name="syntax"></a>Syntax

*Ausdruck* . FindLast (***Kriterien***)

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Criteria</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Eine Zeichenfolge, die zum Suchen des Datensatzes verwendet wird. Sie ähnelt der WHERE-Klausel in einer SQL-Anweisung, allerdings ohne das Wort WHERE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Wenn Sie alle Datensätze in die Suche einschließen möchten (nicht nur die, die eine bestimmte Bedingung erfüllen), verwenden Sie die **Move**-Methoden, um zwischen Datensätzen zu wechseln. Um einen Datensatz in einem Tabellentyp-**Recordset** zu suchen, verwenden Sie die **Seek**-Methode.

Wenn ein Datensatz, der die Bedingungen erfüllt, nicht gefunden wird, ist der aktuelle Datensatzverweis unbekannt und die **NoMatch** -Eigenschaft wird auf **True** festgelegt. Wenn das Recordset mehrere Datensätze enthält, die die Kriterien erfüllen, sucht **FindFirst** das erste Auftreten, **FindNext** sucht das nächste Auftreten usw.

Jede der **Find**-Methoden beginnt die Suche an der Position und in der Richtung, die in der folgenden Tabelle angegeben sind.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Find-Methode</p></th>
<th><p>Suche ab</p></th>
<th><p>Suchrichtung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>FindFirst</strong></p></td>
<td><p>Anfang des Recordsets</p></td>
<td><p>Ende der Datensatzgruppe</p></td>
</tr>
<tr class="even">
<td><p><strong>FindLast</strong></p></td>
<td><p>Ende des Recordsets</p></td>
<td><p>Beginn der Datensatzgruppe</p></td>
</tr>
<tr class="odd">
<td><p><strong>FindNext</strong></p></td>
<td><p>Aktueller Datensatz</p></td>
<td><p>Ende der Datensatzgruppe</p></td>
</tr>
<tr class="even">
<td><p><strong>FindPrevious</strong></p></td>
<td><p>Aktueller Datensatz</p></td>
<td><p>Beginn der Datensatzgruppe</p></td>
</tr>
</tbody>
</table>


Wenn Sie die **FindLast**-Methode verwenden, füllt das Microsoft Access-Datenbankmodul das **Recordset** vor der Suche vollständig auf, falls noch nicht geschehen.

Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.

Überprüfen Sie stets den Wert der **NoMatch** -Eigenschaft, um zu bestimmen, ob der Find-Vorgang erfolgreich war. Wenn die Suche erfolgreich ist, ist **NoMatch** **False**. Bei einem Fehler ist **NoMatch** **True**, und der aktuelle Datensatz ist nicht definiert. In diesem Fall müssen Sie den aktuellen Datensatzzeiger wieder auf einem gültigen Datensatz positionieren.

Das Verwenden von **Find** -Methoden mit ODBC-Zugriffsrecordsets, die mit dem Microsoft Access-Datenbankmodul verbunden sind, kann ineffizient sein. Das Neuformulieren der Kriterien zum Suchen eines bestimmten Datensatzes kann schneller sein, besonders, wenn Sie mit großen Recordsets arbeiten.

Wenn Sie mit ODBC-Zugriffsrecordsets, die mit dem Microsoft Access-Datenbankmodul verbunden sind, und großen **Recordset** -Objekten vom Typ "Dynaset" arbeiten, bemerken Sie möglicherweise, dass das Verwenden der **Find** -Methoden oder der **Sort** - oder **Filter** -Eigenschaft langsam ist. Um die Leistung zu verbessern, verwenden Sie SQL-Abfragen mit angepassten ORDER BY- oder WHERE-Klauseln, Parameterabfragen oder **QueryDef** -Objekten, die bestimmte indizierte Datensätze abrufen.

Auch wenn Sie nicht mit der US-Version des Microsoft Access-Datenbankmoduls arbeiten, sollten Sie bei der Suche nach Feldern mit Datumsangaben das US-Datumsformat (Monat-Tag-Jahr) verwenden, da die Daten sonst evtl. nicht gefunden werden. Mit der Visual Basic-Funktion **Format** können Sie das Datum konvertieren. Beispiel:

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

> [!NOTE]
> Wenn criteria aus einer Zeichenfolge besteht, die mit einem nicht-ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht-U. S. Decimal-Zeichen wie ein Komma (beispielsweise strSQL = " \> Price" & lngPrice und lngPrice = 125, 50) angeben, tritt ein Fehler auf, wenn Sie versuchen, Rufen Sie die Methode auf. Der Grund ist, dass die Zahl bei der Verkettung mithilfe des Standarddezimalzeichens des Systems in eine Zeichenfolge umgewandelt wird und Microsoft Access SQL nur für die USA gültige Dezimalzeichen akzeptiert.

> [!NOTE]
> - Um eine optimale Leistung zu erzielen, sollten die *Kriterien** entweder im Format "*Feldwert* = **" enthalten sein, wobei *Field* ein indiziertes Feld in der zugrunde liegenden Basistabelle ist, oder "*Field* like *prefix*", wobei *Field* ein indiziertes Feld in der zugrunde liegenden Basistabelle und dem *Präfix* ist eine Suchzeichenfolge für das Präfix (beispielsweise "Art *").
> - In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.


