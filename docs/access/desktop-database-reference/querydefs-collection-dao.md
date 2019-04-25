---
title: QueryDefs-Auflistung (DAO)
TOCTitle: QueryDefs Collection
ms:assetid: 6178c3a6-8301-16bf-4657-0fb113de0a36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194892(v=office.15)
ms:contentKeyID: 48545215
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 3543d882e0584c35c88a5475032d9fe5505f516c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303234"
---
# <a name="querydefs-collection-dao"></a><span data-ttu-id="7c0fe-102">QueryDefs-Auflistung (DAO)</span><span class="sxs-lookup"><span data-stu-id="7c0fe-102">QueryDefs Collection (DAO)</span></span>

<span data-ttu-id="7c0fe-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c0fe-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="7c0fe-104">Eine **QueryDefs**-Auflistung enthält alle **QueryDef**-Objekte eines **Database**-Objekts in einer Datenbank eines Microsoft Access-Datenbankmoduls.</span><span class="sxs-lookup"><span data-stu-id="7c0fe-104">A **QueryDefs** collection contains all **QueryDef** objects of a **Database** object in a Microsoft Access database engine database.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c0fe-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c0fe-105">Remarks</span></span>

<span data-ttu-id="7c0fe-106">Um ein neues **QueryDef**-Objekt zu erstellen, verwenden Sie die **CreateQueryDef**-Methode.</span><span class="sxs-lookup"><span data-stu-id="7c0fe-106">To create a new **QueryDef** object, use the **CreateQueryDef** method.</span></span> <span data-ttu-id="7c0fe-107">Wenn Sie in einem Microsoft Access-Arbeitsbereich eine Zeichenfolge für das name-Argument eingeben oder die **Name**-Eigenschaft des neuen **QueryDef**-Objekts explizit auf eine Zeichenfolge festlegen, deren Länge nicht null ist, erstellen Sie ein permanentes **QueryDef**-Objekt, das automatisch an die **QueryDefs**-Auflistung angehängt und auf dem Datenträger gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="7c0fe-107">In a Microsoft Access workspace, if you supply a string for the  name argument or if you explicitly set the **Name** property of the new **QueryDef** object to a non-zero-length string, you will create a permanent **QueryDef** that will automatically be appended to the **QueryDefs** collection and saved to disk.</span></span> <span data-ttu-id="7c0fe-108">Wenn Sie eine Zeichenfolge der Länge null als name-Argument eingeben oder die **Name**-Eigenschaft explizit auf eine Zeichenfolge der Länge null festlegen, führt dies zu einem temporären **QueryDef**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7c0fe-108">Supplying a zero-length string as the  name argument or explicitly setting the **Name** property to a zero-length string will result in a temporary **QueryDef** object.</span></span>

<span data-ttu-id="7c0fe-109">Verwenden Sie eine der folgenden Syntaxformen, um auf ein **QueryDef**-Objekt in einer Auflistung anhand seiner Ordnungszahl oder seiner Einstellung der **Name**-Eigenschaft zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="7c0fe-109">To refer to a **QueryDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="7c0fe-110">**QueryDefs**(0)</span><span class="sxs-lookup"><span data-stu-id="7c0fe-110">**QueryDefs**(0)</span></span>

<span data-ttu-id="7c0fe-111">**QueryDefs**("name")</span><span class="sxs-lookup"><span data-stu-id="7c0fe-111">**QueryDefs**("name")</span></span>

<span data-ttu-id="7c0fe-112">**QueryDefs**\!\[name\]</span><span class="sxs-lookup"><span data-stu-id="7c0fe-112">**QueryDefs**\!\[name\]</span></span>

<span data-ttu-id="7c0fe-113">Auf temporäre **QueryDef**-Objekte können Sie nur anhand der Objektvariablen verweisen, die Sie diesen zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="7c0fe-113">You can refer to temporary **QueryDef** objects only by the object variables that you have assigned to them.</span></span>

## <a name="example"></a><span data-ttu-id="7c0fe-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7c0fe-114">Example</span></span>

<span data-ttu-id="7c0fe-p102">Mit diesem Beispiel wird ein neues **QueryDef**-Objekt erstellt, das an die **QueryDefs**-Auflistung des **Database**-Objekts der Northwind-Datenbank angehängt wird. Anschließend werden die **QueryDefs**-Auflistung und die **Properties**-Auflistung des neuen **QueryDef**-Objekts aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c0fe-p102">This example creates a new **QueryDef** object and appends it to the **QueryDefs** collection of the Northwind **Database** object. It then enumerates the **QueryDefs** collection and the **Properties** collection of the new **QueryDef**.</span></span>

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

<span data-ttu-id="7c0fe-117">In diesem Beispiel wird die **CreateQueryDef**-Methode verwendet, um ein temporäres und ein dauerhaftes **QueryDef**-Objekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7c0fe-117">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**.</span></span> <span data-ttu-id="7c0fe-118">Die GetrstTemp-Funktion wird zur Ausführung dieses Verfahrens benötigt.</span><span class="sxs-lookup"><span data-stu-id="7c0fe-118">The GetrstTemp function is required for this procedure to run.</span></span>

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

Im folgenden Beispiel wird gezeigt, wie eine Parameterabfrage ausgeführt wird. <span data-ttu-id="7c0fe-120">Die Parameters-Auflistung wird verwendet, um den Organization-Parameter der myActionQuery-Abfrage festzulegen, bevor die Abfrage ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c0fe-120">The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

<span data-ttu-id="7c0fe-121">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="7c0fe-121">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="7c0fe-122">Das folgende Beispiel zeigt das Öffnen eines Recordset, das auf einer Parameterabfrage basiert.</span><span class="sxs-lookup"><span data-stu-id="7c0fe-122">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

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

