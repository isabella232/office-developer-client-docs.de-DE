---
title: Recordset2.FindFirst-Methode (DAO)
TOCTitle: FindFirst Method
ms:assetid: 2a18e81a-a9e5-cc1a-50b2-40c1f1b7fa06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192064(v=office.15)
ms:contentKeyID: 48543902
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c3458829dde3be3dbee83289ee111221d006b06c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605967"
---
# <a name="recordset2findfirst-method-dao"></a>Recordset2.FindFirst-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Sucht den ersten Datensatz in einem **Recordset**-Objekt vom "dynaset"- oder "snapshot"-Typ, der die angegebenen Kriterien erfüllt, und macht den Datensatz zum aktuellen Datensatz (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* .FindFirst (***Kriterien***)

*Ausdruck* Eine Variable, die ein **Recordset2-Objekt** darstellt.

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
<td><p><em>Kriterium</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Eine Zeichenfolge, die zum Suchen des Datensatzes verwendet wird. Sie ähnelt der WHERE-Klausel in einer SQL-Anweisung, allerdings ohne das Wort WHERE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Wenn Sie alle Datensätze in die Suche einschließen möchten (nicht nur die, die eine bestimmte Bedingung erfüllen), verwenden Sie die **Move**-Methoden, um zwischen Datensätzen zu wechseln. Um einen Datensatz in einem Tabellentyp-**Recordset** zu suchen, verwenden Sie die **Seek**-Methode.

Wenn ein Datensatz, der die Bedingungen erfüllt, nicht gefunden wird, ist der aktuelle Datensatzverweis unbekannt und die **NoMatch**-Eigenschaft wird auf **True** festgelegt. Wenn das Recordset mehrere Datensätze enthält, die die Kriterien erfüllen, sucht **FindFirst** das erste Auftreten, **FindNext** sucht das nächste Auftreten usw.

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
<th><p>Beginnt die Suche bei</p></th>
<th><p>Suchrichtung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>FindFirst</strong></p></td>
<td><p>Anfang des Recordsets</p></td>
<td><p>Ende des Recordsets</p></td>
</tr>
<tr class="even">
<td><p><strong>FindLast</strong></p></td>
<td><p>Ende des Recordsets</p></td>
<td><p>Anfang des Recordsets</p></td>
</tr>
<tr class="odd">
<td><p><strong>FindNext</strong></p></td>
<td><p>Aktueller Datensatz</p></td>
<td><p>Ende des Recordsets</p></td>
</tr>
<tr class="even">
<td><p><strong>FindPrevious</strong></p></td>
<td><p>Aktueller Datensatz</p></td>
<td><p>Anfang des Recordsets</p></td>
</tr>
</tbody>
</table>


Das Verwenden einer der **Find**-Methoden entspricht jedoch nicht dem Verwenden einer **Move**-Methode, die einfach den ersten, letzten, nächsten oder vorherigen Datensatz zum aktuellen Datensatz macht, ohne eine Bedingung anzugeben. Sie können auf einen Find-Vorgang einen Move-Vorgang folgen lassen.

Überprüfen Sie stets den Wert der **NoMatch**-Eigenschaft, um zu bestimmen, ob der Find-Vorgang erfolgreich war. Wenn die Suche erfolgreich ist, ist **NoMatch****False**. Bei einem Fehler ist **NoMatch****True**, und der aktuelle Datensatz ist nicht definiert. In diesem Fall müssen Sie den aktuellen Datensatzzeiger wieder auf einem gültigen Datensatz positionieren.

Das Verwenden von **Find**-Methoden mit ODBC-Zugriffsrecordsets, die mit dem Microsoft Access-Datenbankmodul verbunden sind, kann ineffizient sein. Das Neuformulieren der Kriterien zum Suchen eines bestimmten Datensatzes kann schneller sein, besonders, wenn Sie mit großen Recordsets arbeiten.

Wenn Sie mit ODBC-Zugriffsrecordsets, die mit dem Microsoft Access-Datenbankmodul verbunden sind, und großen **Recordset**-Objekten vom Typ "Dynaset" arbeiten, bemerken Sie möglicherweise, dass das Verwenden der **Find**-Methoden oder der **Sort**- oder **Filter**-Eigenschaft langsam ist. Um die Leistung zu verbessern, verwenden Sie SQL-Abfragen mit angepassten ORDER BY- oder WHERE-Klauseln, Parameterabfragen oder **QueryDef**-Objekten, die bestimmte indizierte Datensätze abrufen.

Auch wenn Sie nicht mit der US-Version des Microsoft Access-Datenbankmoduls arbeiten, sollten Sie bei der Suche nach Feldern mit Datumsangaben das US-Datumsformat (Monat-Tag-Jahr) verwenden, da die Daten sonst evtl. nicht gefunden werden. Mit der Visual Basic-Funktion **Format** können Sie das Datum konvertieren. Beispiel:

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Wenn die Kriterien aus einer Zeichenfolge bestehen, die mit einem nicht ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht für die USA gültiges Dezimalzeichen, z. B. ein Komma, angeben (Beispiel: strSQL = "PRICE \> " & lngPrice und lngPrice = 125,50), tritt beim Versuch, die Methode aufzurufen, ein Fehler auf. Der Grund ist, dass die Zahl bei der Verkettung mithilfe des Standarddezimalzeichens des Systems in eine Zeichenfolge umgewandelt wird und Microsoft Access SQL nur für die USA gültige Dezimalzeichen akzeptiert.

> [!NOTE]
> - Um eine optimale Leistung zu erzielen, sollten die *Kriterien** entweder im Format "*Feldwert*" liegen,  =  wobei *Feld* ein indiziertes Feld in der zugrunde liegenden Basistabelle ist, oder "*Feld* LIKE *Präfix*", wobei *Feld* ein indiziertes Feld in der zugrunde liegenden Basistabelle ist und *Präfix* eine Präfixsuchzeichenfolge ist (z. B. "ART*").
> - Allgemein stellt die **Seek**-Methode für ähnliche Suchtypen eine bessere Leistung als die **Find**-Methoden bereit. Dabei wird angenommen, dass nur Tabellentyp-**Recordset**-Objekte Ihre Anforderungen erfüllen können.


