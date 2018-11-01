---
title: Recordset2.Index Property (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 897fa6fc41657f1291a726a7ac86b2c6d579abee
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885864"
---
# <a name="recordset2index-property-dao"></a>Recordset2.Index Property (DAO)


**Betrifft**: Access 2013, Office 2013

Legt einen Wert fest, der den Namen des aktuellen **[Index](index-object-dao.md)** -Objekts in einem **[Recordset](recordset-object-dao.md)** -Objekt vom Typ "Tabelle" angibt, oder gibt einen solchen Wert zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . Index

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Hinweise

Datensätze in Basistabellen werden nicht in einer bestimmten Reihenfolge gespeichert. Durch Festlegen der **Index** -Eigenschaft wird die Reihenfolge der von der Datenbank zurückgegebenen Datensätze geändert. Auf die Speicherreihenfolge der Datensätze hat dies keine Auswirkungen.

Das angegebene **Index** -Objekt muss bereits definiert sein. Wenn Sie die **Index** -Eigenschaft auf ein **Index** -Objekt festlegen, das nicht vorhanden ist, oder wenn die **Index** -Eigenschaft nicht festgelegt ist, tritt bei Verwendung der **[Seek](recordset2-seek-method-dao.md)** -Methode ein abfangbarer Fehler auf.

Untersuchen Sie die **Indexes** -Sammlung eines **TableDef** -Objekts, um zu bestimmen, welche **Index** -Objekte für **Recordset** -Objekte vom Typ "Tabelle" zur Verfügung stehen, die aus diesem **TableDef** -Objekt erstellt werden.

Sie können einen neuen Index für die Tabelle erstellen, indem Sie ein neues **Index** -Objekt erstellen, die zugehörigen Eigenschaften festlegen, es an die **Indexes** -Sammlung des zugrunde liegenden **TableDef** -Objekts anfügen und anschließend das **Recordset** -Objekt erneut öffnen.

Datensätze, die von einem **Recordset** -Objekt vom Typ "Tabelle" zurückgegeben werden, können nur nach den Indizes angeordnet werden, die für das zugrunde liegende **TableDef** -Objekt definiert sind. Um Datensätze in einer anderen Reihenfolge zu sortieren, können Sie mithilfe einer SQL-Anweisung mit einer ORDER BY-Klausel einer Dynaset, Snapshot oder vorwärts Typ **Recordset** -Objekt öffnen.


> [!NOTE]
> <UL>
> <LI>
> <P>Sie brauchen keine Indizes für Tabellen zu erstellen. Bei großen, nicht-indizierten Tabellen kann der Zugriff auf einen spezifischen Datensatz oder die Erstellung eines <STRONG>Recordset</STRONG>-Objekts einige Zeit in Anspruch nehmen. Andererseits werden Aktualisierungs-, Anhänge- und Löschvorgänge durch das Erstellen zu vieler Indizes verlangsamt, da alle Indizes automatisch aktualisiert werden.</P>
> <LI>
> <P>Datensätze, die aus Tabellen ohne Indizes eingelesen werden, werden in einer unbestimmten Reihenfolge zurückgegeben.</P>
> <LI>
> <P>Die <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> -Eigenschaft der einzelnen <STRONG><A href="field-object-dao.md">Field</A></STRONG> -Objekte im <STRONG>Index</STRONG>-Objekt legt die Reihenfolge der Datensätze fest und bestimmt daher die für den betreffenden Index zu verwendenden Zugriffsverfahren.</P>
> <LI>
> <P>Mithilfe eines eindeutigen Indexes wird die Suche nach Datensätzen optimiert.</P>
> <LI>
> <P>Indizes haben keinen Einfluss auf die physikalische Reihenfolge einer Basistabelle. Indizes beeinflussen nur, wie ein Recordset-Objekt des Typs Tabelle auf Datensätze zugreift, wenn ein bestimmter Index gewählt wird oder ein Recordset-Objekt geöffnet wird.</P></LI></UL>



## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Index** -Eigenschaft verwendet, um verschiedene Datensatzreihenfolgen für ein **Recordset** vom Typ "Tabelle" festzulegen.

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset2 
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

Dieses Beispiel veranschaulicht die **Seek** -Methode, indem dem Benutzer erlaubt wird, anhand einer ID-Nummer nach einem Produkt zu suchen.

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset2 
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
