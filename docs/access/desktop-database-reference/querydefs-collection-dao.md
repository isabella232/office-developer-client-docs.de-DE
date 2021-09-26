---
title: QueryDefs-Auflistung (DAO)
TOCTitle: QueryDefs Collection
ms:assetid: 6178c3a6-8301-16bf-4657-0fb113de0a36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194892(v=office.15)
ms:contentKeyID: 48545215
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 740b128ce246c108f283489f8e2e172c12eb868c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568607"
---
# <a name="querydefs-collection-dao"></a>QueryDefs-Auflistung (DAO)

**Gilt für**: Access 2013, Office 2013 

Eine **QueryDefs**-Auflistung enthält alle **QueryDef**-Objekte eines **Database**-Objekts in einer Datenbank eines Microsoft Access-Datenbankmoduls.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie zum Erstellen eines neuen **QueryDef**-Objekts die Methode **CreateQueryDef**. Wenn Sie in einem Microsoft Access-Arbeitsbereich eine Zeichenfolge für das „name“-Argument angeben, oder wenn Sie die **Name**-Eigenschaft des neuen **QueryDef**-Objekts explizit auf eine Zeichenfolge festlegen, deren Länge nicht Null (0) ist, erstellen Sie ein dauerhaftes **QueryDef**-Objekt, das automatisch an die **QueryDefs**-Sammlung angefügt und auf dem Datenträger gespeichert wird. Wenn Sie eine Zeichenfolge der Länge Null (0) als „name“-Argument eingeben, oder die **Name**-Eigenschaft explizit auf eine Zeichenfolge der Länge Null (0) festlegen, ist das Ergebnis ein temporäres **QueryDef**-Objekt.

Verwenden Sie eine der folgenden Syntaxformen, um auf ein **QueryDef**-Objekt in einer Auflistung anhand seiner Ordnungszahl oder seiner Einstellung der **Name**-Eigenschaft zu verweisen:

**QueryDefs**(0)

**QueryDefs**("name")

**QueryDefs**\!\[name\]

Auf temporäre **QueryDef**-Objekte können Sie nur anhand der Objektvariablen verweisen, die Sie diesen zugewiesen haben.

## <a name="example"></a>Beispiel

Mit diesem Beispiel wird ein neues **QueryDef**-Objekt erstellt, das an die **QueryDefs**-Auflistung des **Database**-Objekts der Northwind-Datenbank angehängt wird. Anschließend werden die **QueryDefs**-Auflistung und die **Properties**-Auflistung des neuen **QueryDef**-Objekts aufgeführt.

```vb
    Sub QueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfNew As QueryDef 
       Dim qdfLoop As QueryDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new QueryDef object. Because it has a  
       ' name, it is automatically appended to the  
       ' QueryDefs collection. 
       Set qdfNew = dbsNorthwind.CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
     
       With dbsNorthwind 
          Debug.Print .QueryDefs.Count & _ 
             " QueryDefs in " & .Name 
     
          ' Enumerate QueryDefs collection. 
          For Each qdfLoop In .QueryDefs 
             Debug.Print "  " & qdfLoop.Name 
          Next qdfLoop 
     
          With qdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new  
             ' QueryDef object. 
             For Each prpLoop In .Properties 
                On Error Resume Next 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
                On Error Goto 0 
             Next prpLoop 
          End With 
     
          ' Delete new QueryDef because this is a  
          ' demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**. The GetrstTemp function is required for this procedure to run.

```vb
    Sub CreateQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim qdfNew As QueryDef 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
          ' Create temporary QueryDef. 
          Set qdfTemp = .CreateQueryDef("", _ 
             "SELECT * FROM Employees") 
          ' Open Recordset and print report. 
          GetrstTemp qdfTemp 
          ' Create permanent QueryDef. 
          Set qdfNew = .CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
          ' Open Recordset and print report. 
          GetrstTemp qdfNew 
          ' Delete new QueryDef because this is a demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
     
    Function GetrstTemp(qdfTemp As QueryDef) 
     
       Dim rstTemp As Recordset 
     
       With qdfTemp 
          Debug.Print .Name 
          Debug.Print "  " & .SQL 
          ' Open Recordset from QueryDef. 
          Set rstTemp = .OpenRecordset(dbOpenSnapshot) 
     
          With rstTemp 
             ' Populate Recordset and print number of records. 
             .MoveLast 
             Debug.Print "  Number of records = " & _ 
                .RecordCount 
             Debug.Print 
             .Close 
          End With 
     
       End With 
     
    End Function 
```

<br/>

The following example shows how to execute a parameter query. The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer Parameterabfrage basiert.

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

