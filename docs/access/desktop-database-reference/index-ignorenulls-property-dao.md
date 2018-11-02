---
title: Index.IgnoreNulls-Eigenschaft (DAO)
TOCTitle: IgnoreNulls Property
ms:assetid: f49f17b8-d7c1-18ab-07a8-e1be61488519
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836698(v=office.15)
ms:contentKeyID: 48548694
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052931
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4fd7d7e1335e7acd5bc9733d8c13f690be68d82b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926451"
---
# <a name="indexignorenulls-property-dao"></a><span data-ttu-id="4e637-102">Index.IgnoreNulls-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4e637-102">Index.IgnoreNulls property (DAO)</span></span>


<span data-ttu-id="4e637-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e637-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e637-104">Legt einen Wert fest, der angibt, ob Datensätze, deren Indexfelder Nullwerte enthalten, über Indexeinträge verfügen (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="4e637-104">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e637-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e637-105">Syntax</span></span>

<span data-ttu-id="4e637-106">*Ausdruck* . IgnoreNulls</span><span class="sxs-lookup"><span data-stu-id="4e637-106">*expression* .IgnoreNulls</span></span>

<span data-ttu-id="4e637-107">*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4e637-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e637-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e637-108">Remarks</span></span>

<span data-ttu-id="4e637-109">Ein neues **[Index](index-object-dao.md)** objekt, das noch nicht an eine Auflistung angehängt wurde, hat Lese-/Schreibzugriff auf diese Eigenschaft. Ein vorhandenes **Index**objekt in einer **[Indexes](indexes-collection-dao.md)** -Auflistung hat nur Lesezugriff auf die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4e637-109">This property is read/write for a new **[Index](index-object-dao.md)** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection.</span></span>

<span data-ttu-id="4e637-p101">Sie können einen Index für ein Feld definieren, um die Suche nach Datensätzen zu beschleunigen. Wenn Sie in einem indizierten Feld **null**-Einträge zulassen und erwarten, dass viele Einträge den Wert **null** haben, können Sie die **IgnoreNulls**-Eigenschaft für das **Index**-Objekt auf den Wert **True** festlegen, um den vom Index verwendeten Speicherplatz zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="4e637-p101">To speed up the process of searching for records, you can define an index for a field. If you allow **null** entries in an indexed field and expect many of the entries to be **null**, you can set the **IgnoreNulls** property for the **Index** object to **True** to reduce the amount of storage space that the index uses.</span></span>

<span data-ttu-id="4e637-112">Die Einstellungen der **IgnoreNulls**-Eigenschaft und der **[Required](field-required-property-dao.md)** -Eigenschaft legen gemeinsam fest, ob ein Datensatz mit einem **null**-Indexwert einen Indexeintrag hat.</span><span class="sxs-lookup"><span data-stu-id="4e637-112">The **IgnoreNulls** property setting and the **[Required](field-required-property-dao.md)** property setting together determine whether a record with a **null** index value has an index entry.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e637-113">IgnoreNulls-Wert</span><span class="sxs-lookup"><span data-stu-id="4e637-113">If IgnoreNulls is</span></span></p></th>
<th><p><span data-ttu-id="4e637-114">Required-Wert</span><span class="sxs-lookup"><span data-stu-id="4e637-114">And Required is</span></span></p></th>
<th><p><span data-ttu-id="4e637-115">Dann</span><span class="sxs-lookup"><span data-stu-id="4e637-115">Then</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e637-116">True</span><span class="sxs-lookup"><span data-stu-id="4e637-116">True</span></span></p></td>
<td><p><span data-ttu-id="4e637-117">False</span><span class="sxs-lookup"><span data-stu-id="4e637-117">False</span></span></p></td>
<td><p><span data-ttu-id="4e637-118">Im Indexfeld ist ein Nullwert erlaubt. Es wird kein Indexeintrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4e637-118">A null value is allowed in the index field; no index entry added.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e637-119">False</span><span class="sxs-lookup"><span data-stu-id="4e637-119">False</span></span></p></td>
<td><p><span data-ttu-id="4e637-120">False</span><span class="sxs-lookup"><span data-stu-id="4e637-120">False</span></span></p></td>
<td><p><span data-ttu-id="4e637-121">Im Indexfeld ist ein Nullwert erlaubt. Es wird ein Indexeintrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4e637-121">A null value is allowed in the index field; index entry added.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e637-122">True oder False</span><span class="sxs-lookup"><span data-stu-id="4e637-122">True or False</span></span></p></td>
<td><p><span data-ttu-id="4e637-123">True</span><span class="sxs-lookup"><span data-stu-id="4e637-123">True</span></span></p></td>
<td><p><span data-ttu-id="4e637-124">Im Indexfeld ist kein Nullwert erlaubt. Es wird kein Indexeintrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4e637-124">A null value isn't allowed in the index field; no index entry added.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="4e637-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4e637-125">Example</span></span>

<span data-ttu-id="4e637-126">In diesem Beispiel wird die **IgnoreNulls**-Eigenschaft eines neuen **Index**-Objekts basierend auf der Benutzereingabe auf **True** oder **False** gesetzt. Anschließend werden die Auswirkungen auf ein **Recordset**-Objekt mit einem Datensatz gezeigt, dessen Schlüsselfeld einen **Null**-Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="4e637-126">This example sets the **IgnoreNulls** property of a new **Index** to **True** or **False** based on user input, and then demonstrates the effect on a **Recordset** with a record whose key field contains a **Null** value.</span></span>

```vb
    Sub IgnoreNullsX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create a new Index object. 
     Set idxNew = .CreateIndex("NewIndex") 
     idxNew.Fields.Append idxNew.CreateField("Country") 
     
     ' Set the IgnoreNulls property of the new Index object 
     ' based on the user's input. 
     Select Case MsgBox("Set IgnoreNulls to True?", _ 
     vbYesNoCancel) 
     Case vbYes 
     idxNew.IgnoreNulls = True 
     Case vbNo 
     idxNew.IgnoreNulls = False 
     Case Else 
     dbsNorthwind.Close 
     End 
     End Select 
     
     ' Append the new Index object to the Indexes 
     ' collection of the Employees table. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     End With 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Use the new index to set the order of the records. 
     .Index = idxNew.Name 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IgnoreNulls = " & idxNew.IgnoreNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IgnoreNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Index = "" 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Index because this is a demonstration. 
     tdfEmployees.Indexes.Delete idxNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
