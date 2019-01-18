---
title: TableDef.CreateIndex-Methode (DAO)
TOCTitle: CreateIndex Method
ms:assetid: 857b25c1-01fa-b926-0c74-7105e71b7505
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196791(v=office.15)
ms:contentKeyID: 48546062
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052970
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: baa82b659cc2260d4a003c644b2d03d6c897fd21
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706234"
---
# <a name="tabledefcreateindex-method-dao"></a><span data-ttu-id="9e5f0-102">TableDef.CreateIndex-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="9e5f0-102">TableDef.CreateIndex method (DAO)</span></span>

<span data-ttu-id="9e5f0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e5f0-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="9e5f0-p101">Erstellt ein neues **[Index](index-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="9e5f0-p101">Creates a new **[Index](index-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="9e5f0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e5f0-106">Syntax</span></span>

<span data-ttu-id="9e5f0-107">*Ausdruck* . CreateIndex (***Name***)</span><span class="sxs-lookup"><span data-stu-id="9e5f0-107">*expression* .CreateIndex(***Name***)</span></span>

<span data-ttu-id="9e5f0-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9e5f0-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e5f0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e5f0-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e5f0-110">Name</span><span class="sxs-lookup"><span data-stu-id="9e5f0-110">Name</span></span></p></th>
<th><p><span data-ttu-id="9e5f0-111">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="9e5f0-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="9e5f0-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9e5f0-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="9e5f0-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e5f0-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e5f0-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="9e5f0-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="9e5f0-115">Optional</span><span class="sxs-lookup"><span data-stu-id="9e5f0-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="9e5f0-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9e5f0-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9e5f0-p102">Ein <strong>String</strong> -Objekt, mit dem das neue <strong>Index</strong> -Objekt eindeutig benannt wird. Weitere Informationen zu gültigen <strong>Index</strong> -Namen erhalten Sie unter der <strong>Name</strong> -Eigenschaft.  </span><span class="sxs-lookup"><span data-stu-id="9e5f0-p102">A <strong>String</strong> that uniquely names the new <strong>Index</strong> object. See the <strong>Name</strong> property for details on valid <strong>Index</strong> names.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="9e5f0-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e5f0-119">Return value</span></span>

<span data-ttu-id="9e5f0-120">Index</span><span class="sxs-lookup"><span data-stu-id="9e5f0-120">Index</span></span>

## <a name="remarks"></a><span data-ttu-id="9e5f0-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e5f0-121">Remarks</span></span>

<span data-ttu-id="9e5f0-122">Mit der **CreateIndex** -Methode können Sie ein neues **Index** -Objekt für ein **TableDef** -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e5f0-122">You can use the **CreateIndex** method to create a new **Index** object for a **TableDef** object.</span></span> <span data-ttu-id="9e5f0-123">Wenn Sie Teil des optionalen weglassen, wenn Sie die **CreateIndex**verwenden, können Sie eine geeignete Zuweisung verwenden, um festzulegen, oder die **Name** -Eigenschaft zurückzusetzen, bevor Sie das neue Objekt an eine Auflistung anfügen.</span><span class="sxs-lookup"><span data-stu-id="9e5f0-123">If you omit the optional name part when you use **CreateIndex**, you can use an appropriate assignment statement to set or reset the **Name** property before you append the new object to a collection.</span></span> <span data-ttu-id="9e5f0-124">Ob Sie nach dem Anfügen des Objekts dessen **Name** -Eigenschaft festlegen können, hängt davon ab, welcher Objekttyp die **Indexes** -Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="9e5f0-124">After you append the object, you may or may not be able to set its **Name** property, depending on the type of object that contains the **Indexes** collection.</span></span> <span data-ttu-id="9e5f0-125">Weitere Informationen finden Sie im Thema zur **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9e5f0-125">See the **Name** property topic for more details.</span></span>

<span data-ttu-id="9e5f0-126">Wenn Name auf ein Objekt, das bereits ein Element der Auflistung ist bezieht, tritt ein Laufzeitfehler auf, wenn Sie die **[Append](fields-append-method-dao.md)** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e5f0-126">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="9e5f0-127">Wenn Sie ein **Index** -Objekt aus einer Auflistung entfernen möchten, verwenden Sie die **[Delete](fields-delete-method-dao.md)** -Methode für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="9e5f0-127">To remove an **Index** object from a collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="9e5f0-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9e5f0-128">Example</span></span>

<span data-ttu-id="9e5f0-p104">Dieses Beispiel verwendet die **CreateIndex** -Methode, um zwei neue **Index** -Objekte zu erstellen, und fügt sie dann der **Indexes** -Auflistung des **TableDef** -Objekts der Employees-Tabelle (Personal) an. Anschließend führt es die Indexes-Auflistung des **TableDef** -Objekts, die **Fields** -Auflistung des neuen **Index** -Objekts und die Properties-Auflistung des neuen **Index** -Objekts auf. Zum Ausführen dieser Prozedur ist die CreateIndexOutput-Funktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e5f0-p104">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the Indexes collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

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
