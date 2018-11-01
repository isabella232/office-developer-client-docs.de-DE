---
title: TableDef-Objekt (DAO)
TOCTitle: TableDef Object
ms:assetid: 715146b6-c62a-abff-28ee-e6bbe3c08adf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195790(v=office.15)
ms:contentKeyID: 48545582
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e1e03cfcd1aeebc8fdfaf4287e53020a0bc8688
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881272"
---
# <a name="tabledef-object-dao"></a>TableDef-Objekt (DAO)

**Betrifft**: Access 2013, Office 2013

Ein **TableDef** -Objekt stellt die gespeicherte Definition einer Basistabelle oder einer verknüpften Tabelle dar (nur Microsoft Access-Arbeitsbereiche).

## <a name="remarks"></a>Hinweise

Sie ändern eine Tabellendefinition mithilfe eines **TableDef** -Objekts sowie seiner Methoden und Eigenschaften. Folgendes ist zum Beispiel möglich:

- Untersuchen Sie das Feld und die Indexstruktur einer lokalen, verknüpften oder externen Tabelle in einer Datenbank.

- Verwenden Sie die **Connect** - und **SourceTableName** -Eigenschaften, um Informationen zu verknüpften Tabellen festzulegen oder zurückzugeben, und verwenden Sie die **RefreshLink** -Methode, um Verbindungen zu verknüpften Tabellen zu aktualisieren.

- Verwenden Sie die **ValidationRule** - und **ValidationText** -Eigenschaften, um Überprüfungsbedingungen festzulegen oder zurückzugeben.

- Verwenden Sie die **OpenRecordset** -Methode, um eine – Tabelle, Dynaset, dynamisch, Snapshot oder Vorwärts – **Recordset** -Objekt vom Typ, basierend auf der Tabellendefinition erstellen.

Für Basistabellen enthält die **RecordCount** -Eigenschaft die Anzahl der Datensätze in der angegebenen Datenbanktabelle. Für verknüpfte Tabellen wird die Einstellung der **RecordCount** -Eigenschaft immer – 1.

Um ein neues **TableDef** -Objekt zu erstellen, verwenden Sie die **[CreateTableDef](database-createtabledef-method-dao.md)** -Methode.

### <a name="to-add-a-field-to-a-table"></a>So fügen Sie einer Tabelle ein Feld hinzu

1.  Stellen Sie sicher, dass alle **[Recordset](recordset-object-dao.md)** -Objekte, die auf der Tabelle basieren, geschlossen sind.

2.  Verwenden Sie die **CreateField** -Methode, um eine **Field** -Objektvariable zu erstellen, und legen Sie ihre Eigenschaften fest.

3.  Verwenden Sie die **Append** -Methode, um das **Field** -Objekt zur **Fields** -Auflistung des **TableDef** -Objekts hinzuzufügen.

Sie können ein **Field** -Objekt aus einer **TableDefs** -Auflistung löschen, wenn ihm keine Indizes zugewiesen sind. Die Daten des Felds gehen aber verloren.

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a>So erstellen Sie eine Tabelle, die für neue Datensätze in einer Datenbank bereit ist

1.  Verwenden Sie die **CreateTableDef** -Methode, um ein **TableDef** -Objekt zu erstellen.

2.  Legen Sie seine Eigenschaften fest.

3.  Verwenden Sie für jedes Feld in der Tabelle die **CreateField** -Methode, um eine **Field** -Objektvariable zu erstellen, und legen Sie ihre Eigenschaften fest.

4.  Verwenden Sie die **Append** -Methode, um die Felder zur **Fields** -Auflistung des **TableDef** -Objekts hinzuzufügen.

5.  Verwenden Sie die **Append** -Methode, um das neue **TableDef** -Objekt zur **TableDefs** -Auflistung des **Database** -Objekts hinzuzufügen.

Eine verknüpfte Tabelle ist durch die **SourceTableName** - und **Connect** -Eigenschaften des **TableDef** -Objekts mit der Datenbank verbunden.

### <a name="to-link-a-table-to-a-database"></a>So verknüpfen Sie eine Tabelle mit einer Datenbank

1.  Verwenden Sie die **CreateTableDef** -Methode, um ein **TableDef** -Objekt zu erstellen.

2.  Legen Sie die **Connect** - und **SourceTableName** -Eigenschaften (und optional die **Attributes** -Eigenschaft) fest.

3.  Verwenden Sie die **Append** -Methode, um es der **TableDefs** -Auflistung eines **Database** -Objekts hinzuzufügen.

Um auf ein **TableDef** -Objekt in einer Auflistung durch die Ordnungszahl oder die Einstellung der **Name** -Eigenschaft zu verweisen, verwenden Sie eine der folgenden Syntaxformen:

**TableDefs**(0)

**TableDefs** ("Name")

**TableDefs**\!\[Namen\]

## <a name="example"></a>Beispiel

Dieses Beispiel erstellt ein neues **TableDef** -Objekt und hängt es an die **TableDefs** -Auflistung des Northwind-Datenbankobjekts an. Dann zählt es die **TableDefs** -Auflistung und die **Properties** -Auflistung des neuen **TableDef** -Objekts auf.

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

Dieses Beispiel erstellt ein neues **TableDef** -Objekt in der Northwind-Datenbank.

```vb 
Sub CreateTableDefX() 
 
   Dim dbsNorthwind As Database 
   Dim tdfNew As TableDef 
   Dim prpLoop As Property 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
   ' Create a new TableDef object. 
   Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
 
   With tdfNew 
      ' Create fields and append them to the new TableDef  
      ' object. This must be done before appending the  
      ' TableDef object to the TableDefs collection of the  
      ' Northwind database. 
      .Fields.Append .CreateField("FirstName", dbText) 
      .Fields.Append .CreateField("LastName", dbText) 
      .Fields.Append .CreateField("Phone", dbText) 
      .Fields.Append .CreateField("Notes", dbMemo) 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "before appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
      ' Append the new TableDef object to the Northwind  
      ' database. 
      dbsNorthwind.TableDefs.Append tdfNew 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "after appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
```

<br/>

Im folgenden Beispiel wird veranschaulicht, wie Sie ein berechnetes Feld erstellen. Die CreateField-Methode erstellt ein Feld namens **FullName**. Die Expression-Eigenschaft wird dann auf den Ausdruck festgelegt, der den Wert des Felds berechnet.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```
