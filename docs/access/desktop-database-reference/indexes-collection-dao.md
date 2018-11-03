---
title: Indexes-Auflistung (DAO)
TOCTitle: Indexes Collection
ms:assetid: 26450e85-c79d-b12a-d760-dfc89c37f36c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191889(v=office.15)
ms:contentKeyID: 48543802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e38df07831e21a92afdf8106b6d8eb3844396cc
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936756"
---
# <a name="indexes-collection-dao"></a><span data-ttu-id="031dd-102">Indexes-Auflistung (DAO)</span><span class="sxs-lookup"><span data-stu-id="031dd-102">Indexes collection (DAO)</span></span>


<span data-ttu-id="031dd-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="031dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="031dd-104">Eine **Indexes**-Auflistung enthält alle gespeicherten **Index**-Objekte eines **TableDef**-Objekts (nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="031dd-104">An **Indexes** collection contains all the stored **Index** objects of a **TableDef** object (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="031dd-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="031dd-105">Remarks</span></span>

<span data-ttu-id="031dd-106">Wenn Sie ein Recordset-Objekt vom Typ Tabelle zugreifen, verwenden Sie das Objekt **Index** -Eigenschaft, um die Reihenfolge der Datensätze anzugeben.</span><span class="sxs-lookup"><span data-stu-id="031dd-106">When you access a table-type Recordset object, use the object's **Index** property to specify the order of records.</span></span> <span data-ttu-id="031dd-107">Festlegen Sie diese Eigenschaft auf die Einstellung der **Name** -Eigenschaft eines vorhandenen **Index** -Objekts in der **Indexes** -Auflistung des **[TableDef](tabledef-object-dao.md)** -Objekts zugrunde liegenden des **[Recordset](recordset-object-dao.md)** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="031dd-107">Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection of the **[TableDef](tabledef-object-dao.md)** object underlying the **[Recordset](recordset-object-dao.md)** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="031dd-108">[!HINWEIS] Sie können die Methode <STRONG>Append</STRONG> oder <STRONG>Delete</STRONG> nur für eine <STRONG>Indexes</STRONG>-Auflistung verwenden, wenn die Einstellung der <STRONG><A href="connection-updatable-property-dao.md">Updatable</A></STRONG> -Eigenschaft für das enthaltende <STRONG>TableDef</STRONG>-Objekt <STRONG>True</STRONG> lautet.</span><span class="sxs-lookup"><span data-stu-id="031dd-108">You can use the <STRONG>Append</STRONG> or <STRONG>Delete</STRONG> method on an <STRONG>Indexes</STRONG> collection only if the <STRONG><A href="connection-updatable-property-dao.md">Updatable</A></STRONG> property setting of the containing <STRONG>TableDef</STRONG> object is <STRONG>True</STRONG>.</span></span></P>



<span data-ttu-id="031dd-109">Nachdem Sie ein neues **Index**-Objekt erstellt haben, sollten Sie es mit der **Append**-Methode der **Indexes**-Auflistung des **TableDef**-Objekts hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="031dd-109">After you create a new **Index** object, you should use the **Append** method to add it to the **TableDef** object's **Indexes** collection.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="031dd-p102">Stellen Sie sicher, dass Ihre Daten mit den Attributen des neuen Indexes kompatibel sind. Wenn der Index eindeutige Werte erfordert, dürfen vorhandene Datensätze keine Duplikate enthalten. Wenn Duplikate vorhanden sind, kann das Microsoft Access-Datenbankmodul den Index nicht erstellen. Beim Versuch, die Append-Methode auf den neuen Index anzuwenden, tritt ein abfangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="031dd-p102">Make sure your data complies with the attributes of your new index. If your index requires unique values, make sure that there are no duplicates in existing data records. If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>



## <a name="example"></a><span data-ttu-id="031dd-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="031dd-113">Example</span></span>

<span data-ttu-id="031dd-p103">Dieses Beispiel erstellt ein neues Index-Objekt, fügt es der Indexes-Auflistung des TableDef-Objekts der Employees-Tabelle (Personal) an und führt die Indexes-Auflistung des TableDef-Objekts auf. Zuletzt listet es ein Recordset-Objekt auf, zuerst unter Verwendung des primären Index-Objekts und dann unter Verwendung des neuen Index-Objekts. Die IndexOutput-Prozedur ist zum Ausführen dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="031dd-p103">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**. Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**. The IndexOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="031dd-117">Dieses Beispiel verwendet die **CreateIndex** -Methode, um zwei neue **Index** -Objekte zu erstellen, und fügt sie dann der **Indexes** -Auflistung des **TableDef** -Objekts der Employees-Tabelle (Personal) an.</span><span class="sxs-lookup"><span data-stu-id="031dd-117">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object.</span></span> <span data-ttu-id="031dd-118">Klicken Sie dann der **Indexes** -Auflistung des **TableDef** -Objekts, der **Fields** -Auflistung der neuen **Index** -Objekte und der Properties-Auflistung der neuen **Index** -Objekte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="031dd-118">It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects.</span></span> <span data-ttu-id="031dd-119">Zum Ausführen dieser Prozedur ist die CreateIndexOutput-Funktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="031dd-119">The CreateIndexOutput function is required for this procedure to run.</span></span>

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
