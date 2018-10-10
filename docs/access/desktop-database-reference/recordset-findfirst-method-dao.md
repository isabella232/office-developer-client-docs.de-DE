---
title: Recordset.FindFirst-Methode (DAO)
TOCTitle: FindFirst Method
ms:assetid: 5fcf78cd-7d2c-2e47-14e5-996f2e14ff51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194787(v=office.15)
ms:contentKeyID: 48545170
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b98fcc1ce31bd854d1e74f4f650ba5b453b8f39a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475594"
---
# <a name="recordsetfindfirst-method-dao"></a>Recordset.FindFirst-Methode (DAO)

**Betrifft**: Access 2013 | Office 2013

Sucht den ersten Datensatz in einem **Recordset** -Objekt vom "dynaset"- oder "snapshot"-Typ, der die angegebenen Kriterien erfüllt, und macht den Datensatz zum aktuellen Datensatz (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . FindFirst (***Kriterien***)

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

### <a name="parameters"></a>Parameter

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
<th><p>Erforderlich/Optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Kriterium</p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Eine Zeichenfolge, die zum Suchen des Datensatzes verwendet wird. Sie ähnelt der WHERE-Klausel in einer SQL-Anweisung, allerdings ohne das Wort WHERE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Wenn Sie alle Datensätze in die Suche einschließen möchten (nicht nur die, die eine bestimmte Bedingung erfüllen), verwenden Sie die **Move** -Methoden, um zwischen Datensätzen zu wechseln. Um einen Datensatz in einem Tabellentyp- **Recordset** zu suchen, verwenden Sie die **Seek** -Methode.

Wenn ein Datensatz, der die Bedingungen erfüllt, nicht gefunden wird, ist der aktuelle Datensatzverweis unbekannt und die **NoMatch** -Eigenschaft wird auf **True** festgelegt. Wenn das Recordset mehrere Datensätze enthält, die die Kriterien erfüllen, sucht **FindFirst** das erste Auftreten, **FindNext** sucht das nächste Auftreten usw.

Jede der **Find** -Methoden beginnt die Suche an der Position und in der Richtung, die in der folgenden Tabelle angegeben sind.

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


Das Verwenden einer der **Find** -Methoden entspricht jedoch nicht dem Verwenden einer **Move** -Methode, die einfach den ersten, letzten, nächsten oder vorherigen Datensatz zum aktuellen Datensatz macht, ohne eine Bedingung anzugeben. Sie können auf einen Find-Vorgang einen Move-Vorgang folgen lassen.

Überprüfen Sie stets den Wert der **NoMatch** -Eigenschaft, um zu bestimmen, ob der Find-Vorgang erfolgreich war. Wenn die Suche erfolgreich ist, ist **NoMatch** **False**. Bei einem Fehler ist **NoMatch** **True**, und der aktuelle Datensatz ist nicht definiert. In diesem Fall müssen Sie den aktuellen Datensatzzeiger wieder auf einem gültigen Datensatz positionieren.

Das Verwenden von **Find** -Methoden mit ODBC-Zugriffsrecordsets, die mit dem Microsoft Access-Datenbankmodul verbunden sind, kann ineffizient sein. Das Neuformulieren der Kriterien zum Suchen eines bestimmten Datensatzes kann schneller sein, besonders, wenn Sie mit großen Recordsets arbeiten.

Wenn Sie mit ODBC-Zugriffsrecordsets, die mit dem Microsoft Access-Datenbankmodul verbunden sind, und großen **Recordset** -Objekten vom Typ "Dynaset" arbeiten, bemerken Sie möglicherweise, dass das Verwenden der **Find** -Methoden oder der **Sort** - oder **Filter** -Eigenschaft langsam ist. Um die Leistung zu verbessern, verwenden Sie SQL-Abfragen mit angepassten ORDER BY- oder WHERE-Klauseln, Parameterabfragen oder **QueryDef** -Objekten, die bestimmte indizierte Datensätze abrufen.

Sie sollten das amerikanische Datumsformat (Monat-Tag-Jahr) verwenden, wenn Sie nach Feldern mit Datumsangaben suchen, auch wenn Sie nicht die US-amerikanische Version des Microsoft Access-Datenbankmoduls verwenden. Andernfalls werden die Daten möglicherweise nicht gefunden. Verwenden Sie die **Format** -Funktion von Visual Basic, um das Datum zu konvertieren. Beispiel:

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Wenn Kriterien besteht aus einer Zeichenfolge mit einem nicht-Integer-Wert verkettet und die Systemparameter einer US-decimal Zeichen wie etwa ein Komma angeben (beispielsweise StrSQL = "PRICE \> " & LngPrice, und LngPrice = 125,50), ein Fehler tritt auf, wenn Sie versuchen, Rufen Sie die-Methode. Das geschieht, weil die Zahl während der Verkettung mithilfe des standardmäßigen Dezimalzeichens des Systems in eine Zeichenfolge konvertiert wird und Microsoft Access SQL nur US-amerikanische Dezimalzeichen akzeptiert.


> [!NOTE]
> - Für eine optimale Leistung der *Kriterien* sollte entweder in das Formular "*Feld* = *Wert*", in dem *Feld* einem indizierten Feld befindet sich in der zugrunde liegenden Basistabelle oder "*Feld* wie *Präfix*", in *das Feld* ist, ein indizierte Feld in der zugrunde liegenden Basistabelle und das *Präfix* ist eine Suchzeichenfolge Präfix (beispielsweise "ClipArt *").
> 
> - Allgemein stellt die **Seek**-Methode für ähnliche Suchtypen eine bessere Leistung als die **Find**-Methoden bereit. Dabei wird angenommen, dass nur Tabellentyp-**Recordset**-Objekte Ihre Anforderungen erfüllen können.


## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt das Verwenden der FindFirst- und FindNext-Methoden zum Suchen eines Datensatzes in einem Recordset.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```
