---
title: Recordset.Index-Eigenschaft (DAO)
TOCTitle: Index Property
ms:assetid: 54626de0-eb51-31f2-bf24-e29cbfbbaa02
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194103(v=office.15)
ms:contentKeyID: 48544895
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052906
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: a2e8b58d60a733e95f23a843cf8c15d3910640ec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602073"
---
# <a name="recordsetindex-property-dao"></a>Recordset.Index-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der den Namen des aktuellen **[Index](index-object-dao.md)**-Objekts in einem **[Recordset](recordset-object-dao.md)**-Objekt vom Typ "Tabelle" angibt, oder gibt einen solchen Wert zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* .Index

*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Datensätze in Basistabellen werden nicht in einer bestimmten Reihenfolge gespeichert. Durch Festlegen der **Index**-Eigenschaft wird die Reihenfolge der von der Datenbank zurückgegebenen Datensätze geändert. Auf die Speicherreihenfolge der Datensätze hat dies keine Auswirkungen.

Das angegebene **Index**-Objekt muss bereits definiert sein. Wenn Sie die **Index**-Eigenschaft auf ein **Index**-Objekt festlegen, das nicht vorhanden ist, oder wenn die **Index**-Eigenschaft nicht festgelegt ist, tritt bei Verwendung der **[Seek](recordset-seek-method-dao.md)**-Methode ein abfangbarer Fehler auf.

Untersuchen Sie die **Indexes**-Sammlung eines **TableDef**-Objekts, um zu bestimmen, welche **Index**-Objekte für **Recordset**-Objekte vom Typ "Tabelle" zur Verfügung stehen, die aus diesem **TableDef**-Objekt erstellt werden.

Sie können einen neuen Index für die Tabelle erstellen, indem Sie ein neues **Index**-Objekt erstellen, die zugehörigen Eigenschaften festlegen, es an die **Indexes**-Sammlung des zugrunde liegenden **TableDef**-Objekts anfügen und anschließend das **Recordset**-Objekt erneut öffnen.

Datensätze, die von einem **Recordset**-Objekt vom Typ "Tabelle" zurückgegeben werden, können nur nach den Indizes angeordnet werden, die für das zugrunde liegende **TableDef**-Objekt definiert sind. Um Datensätze in einer anderen Reihenfolge zu sortieren, können Sie ein **Recordset**-Objekt vom Typ "Dynaset", "Snapshot" oder "Forward-only" öffnen, indem Sie eine SQL-Anweisung mit einer ORDER BY-Klausel verwenden.


> [!NOTE]
> - Sie müssen keine Indizes für Tabellen erstellen. Bei großen Tabellen ohne Index kann der Zugriff auf einen bestimmten Datensatz oder das Erstellen eines **Recordset**-Objekts sehr lange dauern. Andererseits kann die Erstellung zu vieler Indizes Update-, Anfüge- und Löschvorgänge verlangsamen, da alle Indizes automatisch aktualisiert werden.
> - Datensätze, die aus Tabellen ohne Indizes gelesen werden, werden in keiner bestimmten Reihenfolge zurückgegeben.
> - Die **[Attributes](field-attributes-property-dao.md)**-Eigenschaft jedes **[Field](field-object-dao.md)**-Objekts im **Index**-Objekt bestimmt die Reihenfolge der Datensätze und folglich die geeigneten Methoden zum Zugreifen auf diesen Index.
> - Ein eindeutiger Index trägt zur Optimierung der Suche nach Datensätzen bei.
> - Indizes wirken sich nicht auf die physische Reihenfolge einer Basistabelle aus, sondern beeinflussen nur, wie vom **Recordset**-Objekt des Typs "Tabelle" auf die Datensätze zugegriffen wird, wenn ein bestimmter Index ausgewählt oder ein **Recordset** geöffnet wird.


## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Index**-Eigenschaft verwendet, um verschiedene Datensatzreihenfolgen für ein **Recordset** vom Typ "Tabelle" festzulegen.

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset 
       Dim idxLoop As Index 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
       Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
       With rstEmployees 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In tdfEmployees.Indexes 
             .Index = idxLoop.Name 
             Debug.Print "Index = " & .Index 
             Debug.Print "  EmployeeID - PostalCode - Name" 
             .MoveFirst 
     
             ' Enumerate Recordset to show the order of records. 
             Do While Not .EOF 
                Debug.Print "    " & !EmployeeID & " - " & _ 
                   !PostalCode & " - " & !FirstName & " " & _ 
                   !LastName 
                .MoveNext 
             Loop 
     
          Next idxLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Dieses Beispiel veranschaulicht die **Seek**-Methode, indem dem Benutzer erlaubt wird, nach einem Produkt anhand einer ID-Nummer zu suchen.

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Im folgenden Beispiel wird gezeigt, wie Sie mithilfe der Seek-Methode einen Datensatz in einer verknüpften Tabelle finden.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
