---
title: TableDefs-Auflistung (DAO)
TOCTitle: TableDefs Collection
ms:assetid: a2986b02-0437-d6ac-7bbb-c43f5225c3fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820997(v=office.15)
ms:contentKeyID: 48546766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f16f44b57a690aa58efdff9b00341df5023c293f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702880"
---
# <a name="tabledefs-collection-dao"></a><span data-ttu-id="d071d-102">TableDefs-Auflistung (DAO)</span><span class="sxs-lookup"><span data-stu-id="d071d-102">TableDefs collection (DAO)</span></span>

<span data-ttu-id="d071d-103">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d071d-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="d071d-104">Eine **TableDefs** -Sammlung enthält alle gespeicherten **TableDef** -Objekte in einer Datenbank (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="d071d-104">A **TableDefs** collection contains all stored **TableDef** objects in a database (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="d071d-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d071d-105">Remarks</span></span>

<span data-ttu-id="d071d-106">Sie bearbeiten eine Tabellendefinition anhand eines **TableDef** -Objekts und seiner Methoden und Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d071d-106">You manipulate a table definition using a **TableDef** object and its methods and properties.</span></span>

<span data-ttu-id="d071d-107">Die Standardsammlung eines **Datenbank** objekts ist die **TableDefs** -Sammlung.</span><span class="sxs-lookup"><span data-stu-id="d071d-107">The default collection of a **Database** object is the **TableDefs** collection.</span></span>

<span data-ttu-id="d071d-108">Verwenden Sie eines der folgenden Syntaxformate, um auf ein **TableDef** -Objekt in einer Sammlung nach seiner Ordnungszahl oder der **Name** -Eigenschafteneinstellung zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="d071d-108">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="d071d-109">**TableDefs**(0)</span><span class="sxs-lookup"><span data-stu-id="d071d-109">**TableDefs**(0)</span></span>

<span data-ttu-id="d071d-110">**TableDefs** ("Name")</span><span class="sxs-lookup"><span data-stu-id="d071d-110">**TableDefs**("name")</span></span>

<span data-ttu-id="d071d-111">**TableDefs**\!\[Namen\]</span><span class="sxs-lookup"><span data-stu-id="d071d-111">**TableDefs**\!\[name\]</span></span>

<span data-ttu-id="d071d-112">**Links bereitgestellt werden, von** der Community [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="d071d-112">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="d071d-113">UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.</span><span class="sxs-lookup"><span data-stu-id="d071d-113">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

  - [<span data-ttu-id="d071d-114">Re-Linker Multi-Backends</span><span class="sxs-lookup"><span data-stu-id="d071d-114">Re-Linker Multi-Backends</span></span>](https://www.utteraccess.com/wiki/index.php/re-linker_multi-backends)

  - [<span data-ttu-id="d071d-115">Swap/Relink Between LIVE, TEST and LOCAL Data (Tausch/Neuverlinkung zwischen LIVE-, TEXT- und LOCAL-Daten)</span><span class="sxs-lookup"><span data-stu-id="d071d-115">Swap/Relink Between LIVE, TEST and LOCAL Data</span></span>](https://www.utteraccess.com/forum/swap-relink-live-test-t1328573.html)

## <a name="example"></a><span data-ttu-id="d071d-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d071d-116">Example</span></span>

<span data-ttu-id="d071d-p102">Dieses Beispiel erstellt ein neues **TableDef** -Objekt und hängt es an die **TableDefs** -Auflistung des Northwind-Datenbankobjekts an. Dann zählt es die **TableDefs** -Auflistung und die **Properties** -Auflistung des neuen **TableDef** -Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="d071d-p102">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object. It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

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

<span data-ttu-id="d071d-119">Dieses Beispiel erstellt ein neues **TableDef** -Objekt in der Northwind-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d071d-119">This example creates a new **TableDef** object in the Northwind database.</span></span>

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



