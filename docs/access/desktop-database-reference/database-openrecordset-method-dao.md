---
title: Database.OpenRecordset-Methode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 09/04/2019
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b8a6e9a2204a60ecff33555d31f39591308f9b67
ms.sourcegitcommit: 27a9f3568318470e7ee09ad93a90c3f80d3ef0cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2019
ms.locfileid: "36790764"
---
# <a name="databaseopenrecordset-method-dao"></a>Database.OpenRecordset-Methode (DAO)

**Gilt für:** Access 2013 | Office 2013

Erstellt ein neues **[Recordset](recordset-object-dao.md)**-Objekt und fügt es an die **Recordsets**-Auflistung an.

## <a name="syntax"></a>Syntax

*Ausdruck*.**OpenRecordset** (_Name_, _ Typ_, _Optionen_, _LockEdit_)

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

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
<td><p><em>Name</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Die Quelle der Datensätze für das neue  <strong>Recordset</strong>. Die Quelle kann ein Tabellenname, ein Abfragename oder eine SQL-Anweisung sein, die Datensätze zurückgibt. Für <strong>Recordset</strong>-Objekte vom "table"-Typ in Microsoft Access-Datenbankmodul-Datenbanken kann die Quelle nur ein Tabellenname sein.</p></td>
</tr>
<tr class="even">
<td><p><em>Typ</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>-Konstante gibt den Typ des zu öffnenden <strong>Recordset</strong> an.</p><p><strong>Hinweis</strong>: Wenn Sie ein <strong>Recordset</strong> in einem Microsoft Access-Arbeitsbereich öffnen und keinen Typ angeben, erstellt <strong>OpenRecordset</strong>, wenn möglich, ein tabellenartiges <strong>Recordset</strong>. If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>Optionen</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Kombination aus <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>-Konstanten, die Merkmale des neuen <strong>Recordset</strong> angeben.</p><p><strong>Hinweis</strong>: Die Konstanten <strong>dbConsistent</strong> und <strong>dbInconsistent</strong>schließen sich gegenseitig aus, und die Verwendung beider verursacht einen Fehler. Das Bereitstellen eines LockEdit-Arguments, wenn Optionen die Konstante <strong>dbReadOnly</strong> verwendet, führt ebenfalls zu einem Fehler. </p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong>-Konstante, die die Sperre für das <strong>Recordset</strong> bestimmt.</p><p><strong>Hinweis</strong>: Sie können <strong>dbReadOnly</strong> im Options-Argument oder im LockedEdit-Argument verwenden, aber nicht in beiden. Wenn Sie es für beide Argumente verwenden, tritt ein Laufzeitfehler auf.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Recordset

## <a name="remarks"></a>Hinweise

Wenn der Benutzer diesen Fehler beim Aktualisieren eines Datensatzes erhält, sollte Ihr Code normalerweise die Inhalte der Felder aktualisieren und die neu geänderten Werte abrufen. Wenn der Fehler beim Löschen eines Datensatzes auftritt, könnte Ihr Code dem Benutzer die neuen Datensatzdaten und eine Meldung anzeigen, dass die Daten kürzlich geändert wurden. An diesem Punkt kann Ihr Code eine Bestätigung anfordern, dass der Benutzer den Datensatz immer noch löschen möchte.

Sie sollten auch die **dbSeeChanges**-Konstante verwenden, wenn Sie ein **Recordset** in einem ODBC-Arbeitsbereich mit verbundenem Microsoft Access-Datenbankmodul für eine Microsoft SQL Server 6.0-Tabelle (oder neuer) öffnen, die über eine  IDENTITY-Spalte verfügt. Andernfalls kann ein Fehler auftreten.

Wenn Sie mehr als ein **Recordset** in einer ODBC-Datenquelle öffnen, kann die Datenquelle ausfallen, da die Verbindung mit einem vorherigen **OpenRecordset**-Aufruf beschäftigt ist. Eine Lösungsmöglichkeit besteht im vollständigen Ausfüllen des **Recordset** mithilfe der **MoveLast**-Methode, sobald das **Recordset** geöffnet wird.

Durch das Schließen eines **Recordset** mit der **[Close](connection-close-method-dao.md)**-Methode wird es automatisch aus der **Recordsets**-Auflistung gelöscht.


> [!NOTE]
> Wenn sich *source* auf eine SQL-Anweisung bezieht, die aus einer Zeichenfolge besteht, die mit einem nicht ganzzahligen Wert verkettet ist, und die Systemparameter ein nicht für die USA gültiges Dezimalzeichen, z. B. ein Komma, angeben (Beispiel: strSQL = "PRICE &gt; " &amp; lngPrice, und lngPrice = 125,50), tritt beim Versuch, das **Recordset** zu öffnen, ein Fehler auf. Der Grund ist, dass die Zahl bei der Verkettung mithilfe des Standarddezimalzeichens des Systems in eine Zeichenfolge umgewandelt wird und SQL nur für die USA gültige Dezimalzeichen akzeptiert.

**Link zur Verfügung gestellt von: ** [UtterAccess](https://www.utteraccess.com)-Community. UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.

- [Übertragen von Daten aus Access in Excel](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer Parameterabfrage basiert.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qdf = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer Tabelle oder Abfrage basiert.

```vb 
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer SQL-Anweisung (Structured Query Language) basiert.

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

Das folgende Beispiel zeigt das Verwenden der Filter-Eigenschaft zum Ermitteln der Datensätze, die in einem danach geöffneten Recordset enthalten sein sollen.

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rst = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```



