---
title: Recordset.FindNext-Methode (DAO)
TOCTitle: FindNext Method
ms:assetid: 5457dfc8-e561-5624-74d0-34278ba2e7cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194099(v=office.15)
ms:contentKeyID: 48544893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a9ef8f1714244b02ed5423a38cf3fb8fa328ec1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300637"
---
# <a name="recordsetfindnext-method-dao"></a>Recordset.FindNext-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Sucht den nächsten Datensatz in einem **[Recordset](recordset-object-dao.md)**-Objekt vom Typ Dynaset oder Snapshot, der den angegebenen Kriterien entspricht, und macht diesen Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* .FindNext(***Kriterien***)

*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.

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

Das Verwenden der **Find**-Methoden kann für Datensätze, auf die über mit dem Microsoft Access-Datenbankmodul verbundene ODBC-Datenbanken zugegriffen wird, ineffizient sein. Es geht vermutlich schneller, insbesondere bei großen Datensatzgruppen, einen bestimmten Datensatz durch Umformulieren von criteria zu suchen.

In einem ODBCDirect-Arbeitsbereich sind die **Find**- und **Seek**-Methoden nicht für jeden **Recordset**-Objekttyp verfügbar, da das Ausführen einer **Find**- oder **Seek**-Methode mit einer ODBC-Verbindung über das Netzwerk nicht sehr effizient ist. Stattdessen sollten Sie beim Abfrageentwurf (d. h. Verwenden des Arguments source für die **OpenRecordset**-Methode) eine entsprechende WHERE-Klausel einfügen, um nur die Datensätze zurückzugeben, die den Kriterien entsprechen, die Sie sonst in einer **Find**- oder **Seek**-Methode verwenden würden.

Wenn Sie mit einem Microsoft Access-Datenbankmodul verbundene ODBC-Datenbanken sowie große Objekte vom Typ Dynaset verwenden, kann es sein, dass das Arbeiten mit den **Find**-Methoden oder den **Sort**- bzw. **Filter**-Eigenschaften langsam ist. Sie können die Leistung verbessern, indem Sie SQL-Abfragen mit benutzerdefinierten ORDER BY- oder WHERE-Klauseln, Parameterabfragen oder **QueryDef**-Objekte verwenden, die bestimmte indizierte Datensätze abrufen.

Auch wenn Sie nicht mit der US-Version des Microsoft Access-Datenbankmoduls arbeiten, sollten Sie bei der Suche nach Feldern mit Datumsangaben das US-Datumsformat (Monat-Tag-Jahr) verwenden, da die Daten sonst evtl. nicht gefunden werden. Mit der Visual Basic-Funktion **Format** können Sie das Datum konvertieren. Beispiel:

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Wenn die Kriterien aus einer Zeichenfolge bestehen, die mit einem nicht ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht für die USA gültiges Dezimalzeichen, z. B. ein Komma, angeben (Beispiel: strSQL = "PRICE \> " & lngPrice und lngPrice = 125,50), tritt beim Versuch, die Methode aufzurufen, ein Fehler auf. Der Grund ist, dass die Zahl bei der Verkettung mithilfe des Standarddezimalzeichens des Systems in eine Zeichenfolge umgewandelt wird und Microsoft Access SQL nur für die USA gültige Dezimalzeichen akzeptiert.

> [!NOTE]
> - Um die bestmögliche Leistung zu erzielen, sollten die *Kriterien* in der Form "*Feld*  =  *Wert*" vorliegen, wobei *Feld* ein indiziertes Feld in der zugrunde liegenden Basistabelle ist, oder in der Form "*Feld* LIKE *Präfix*", wobei *Feld* ein indiziertes Feld in der zugrunde liegenden Basistabelle und *Präfix* eine Präfixsuchzeichenfolge ist (z. B. "ART*").
> 
> - Allgemein stellt die **Seek**-Methode für ähnliche Suchtypen eine bessere Leistung als die **Find**-Methoden bereit. Dabei wird angenommen, dass nur Tabellentyp-**Recordset**-Objekte Ihre Anforderungen erfüllen können.


## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt das Verwenden der FindFirst- und FindNext-Methoden zum Suchen eines Datensatzes in einem Recordset.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


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
