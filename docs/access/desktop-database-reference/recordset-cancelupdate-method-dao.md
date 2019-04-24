---
title: Recordset. CancelUpdate-Methode (DAO)
TOCTitle: CancelUpdate method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5950154d8896678889af01254104a2ac0dfef4cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300679"
---
# <a name="recordsetcancelupdate-method-dao"></a><span data-ttu-id="6eedb-102">Recordset. CancelUpdate-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="6eedb-102">Recordset.CancelUpdate method (DAO)</span></span>

<span data-ttu-id="6eedb-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6eedb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6eedb-104">Bricht alle ausstehenden Aktualisierungen für ein **[Recordset](recordset-object-dao.md)** -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="6eedb-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eedb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6eedb-105">Syntax</span></span>

<span data-ttu-id="6eedb-106">*Ausdruck* . CancelUpdate (***UpdateType***)</span><span class="sxs-lookup"><span data-stu-id="6eedb-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="6eedb-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6eedb-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6eedb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6eedb-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6eedb-109">Name</span><span class="sxs-lookup"><span data-stu-id="6eedb-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6eedb-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="6eedb-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="6eedb-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6eedb-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="6eedb-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6eedb-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6eedb-113"><em>Aktualisierungstyp</em></span><span class="sxs-lookup"><span data-stu-id="6eedb-113"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="6eedb-114">Optional</span><span class="sxs-lookup"><span data-stu-id="6eedb-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="6eedb-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="6eedb-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="6eedb-116">Auf einen der <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> -Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6eedb-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p><p><span data-ttu-id="6eedb-117"><strong>Hinweis</strong>: die <EM>DbUpdateRegular</EM> -und <EM>dbUpdateBatch</EM> -Werte sind nur gültig, wenn die Batchaktualisierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6eedb-117"><strong>NOTE</strong>: The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6eedb-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6eedb-118">Remarks</span></span>

<span data-ttu-id="6eedb-p101">Mit der **CancelUpdate**-Methode können Sie alle ausstehenden Aktualisierungen abbrechen, die aus einer **[Edit](recordset-edit-method-dao.md)** - oder **[AddNew](recordset-addnew-method-dao.md)** -Operation stammen. Wenn ein Benutzer z. B. die **Edit**- oder **AddNew**-Methode aufruft, ohne vorher die **Update**-Methode aufgerufen zu haben, werden durch die **CancelUpdate**-Methode alle Änderungen abgebrochen, die nach dem Aufrufen von **Edit** oder **AddNew** vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="6eedb-p101">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** operation. For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="6eedb-121">Überprüfen Sie die **[EditMode](recordset-editmode-property-dao.md)** -Eigenschaft des **Recordset**-Objekts, um zu ermitteln, ob eine Operation aussteht, die abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6eedb-121">Check the **[EditMode](recordset-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="6eedb-122">[!HINWEIS] Die Verwendung der **CancelUpdate**-Methode hat dieselbe Wirkung wie das Verschieben zu einem anderen Datensatz, ohne die **[Update](recordset-update-method-dao.md)** -Methode zu verwenden. Der einzige Unterschied besteht darin, dass der aktuelle Datensatz nicht geändert wird und dass verschiedene Eigenschaften nicht aktualisiert werden, z. B. **[BOF](recordset-bof-property-dao.md)** und **[EOF](recordset-eof-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="6eedb-122">Using the **CancelUpdate** method has the same effect as moving to another record without using the **[Update](recordset-update-method-dao.md)** method, except that the current record doesn't change, and various properties, such as **[BOF](recordset-bof-property-dao.md)** and **[EOF](recordset-eof-property-dao.md)**, aren't updated.</span></span>


## <a name="example"></a><span data-ttu-id="6eedb-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6eedb-123">Example</span></span>

<span data-ttu-id="6eedb-124">Dieses Beispiel zeigt, wie die Methoden **CancelUpdate** und **AddNew** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="6eedb-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "Employees", dbOpenDynaset) 
     
       With rstEmployees 
          .AddNew 
          !FirstName = "Kimberly" 
          !LastName = "Bowen" 
          intCommand = MsgBox("Add new record for " & _ 
             !FirstName & " " & !LastName & "?", vbYesNo) 
          If intCommand = vbYes Then 
             .Update 
             MsgBox "Record added." 
             ' Delete new record because this is a  
             ' demonstration. 
             .Bookmark = .LastModified 
             .Delete 
          Else 
             .CancelUpdate 
             MsgBox "Record not added." 
          End If 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="6eedb-125">Dieses Beispiel zeigt, wie die Methoden **CancelUpdate** und **Edit** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="6eedb-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

```vb
Sub CancelUpdateX2() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim strFirst As String 
   Dim strLast As String 
   Dim intCommand As Integer 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
      "Employees", dbOpenDynaset) 
 
   With rstEmployees 
      strFirst = !FirstName 
      strLast = !LastName 
      .Edit 
      !FirstName = "Cora" 
      !LastName = "Edmonds" 
      intCommand = MsgBox("Replace current name with " & _ 
         !FirstName & " " & !LastName & "?", vbYesNo) 
      If intCommand = vbYes Then 
         .Update 
         MsgBox "Record modified." 
         ' Restore data because this is a demonstration. 
         .Bookmark = .LastModified 
         .Edit 
         !FirstName = strFirst 
         !LastName = strLast 
         .Update 
      Else 
         .CancelUpdate 
         MsgBox "Record not modified." 
      End If 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
 
```

