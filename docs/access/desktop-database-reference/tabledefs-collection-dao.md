---
title: TableDefs-Sammlung (DAO)
TOCTitle: TableDefs Collection
ms:assetid: a2986b02-0437-d6ac-7bbb-c43f5225c3fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820997(v=office.15)
ms:contentKeyID: 48546766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f16f44b57a690aa58efdff9b00341df5023c293f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314175"
---
# <a name="tabledefs-collection-dao"></a>TableDefs-Sammlung (DAO)

**Gilt für:** Access 2013 | Office 2013

Eine **TableDefs**-Sammlung enthält alle gespeicherten **TableDef**-Objekte in einer Datenbank (nur Microsoft Access-Arbeitsbereiche).

## <a name="remarks"></a>Hinweise

Sie bearbeiten eine Tabellendefinition anhand eines **TableDef**-Objekts und seiner Methoden und Eigenschaften.

Die Standardsammlung eines **Datenbank**objekts ist die **TableDefs**-Sammlung.

Um auf ein **TableDef**-Objekt in einer Auflistung durch die Ordnungszahl oder die Einstellung der **Name**-Eigenschaft zu verweisen, verwenden Sie eine der folgenden Syntaxformen:

**TableDefs**(0)

**TableDefs**("name")

**TableDefs**\!\[name\]

**Links zur Verfügung gestellt von: ** [UtterAccess](https://www.utteraccess.com)-Community. UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.

  - [Re-Linker Multi-Backends](https://www.utteraccess.com/wiki/index.php/re-linker_multi-backends)

  - [Swap/Relink Between LIVE, TEST and LOCAL Data (Tausch/Neuverlinkung zwischen LIVE-, TEXT- und LOCAL-Daten)](https://www.utteraccess.com/forum/swap-relink-live-test-t1328573.html)

## <a name="example"></a>Beispiel

Dieses Beispiel erstellt ein neues **TableDef**-Objekt und hängt es an die **TableDefs**-Auflistung des Northwind-Datenbankobjekts an. Dann zählt es die **TableDefs**-Auflistung und die **Properties**-Auflistung des neuen **TableDef**-Objekts auf.

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

Dieses Beispiel erstellt ein neues **TableDef**-Objekt in der Northwind-Datenbank.

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



