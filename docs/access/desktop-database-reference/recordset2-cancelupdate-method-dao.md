---
title: Recordset2.CancelUpdate-Methode (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: f741dec1-b9a4-506e-74ec-2bc309b0918e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836907(v=office.15)
ms:contentKeyID: 48548761
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 90378dc61d12485a290bbd7857d026a46cd9da96
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721374"
---
# <a name="recordset2cancelupdate-method-dao"></a><span data-ttu-id="60bb2-102">Recordset2.CancelUpdate-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="60bb2-102">Recordset2.CancelUpdate method (DAO)</span></span>

<span data-ttu-id="60bb2-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60bb2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60bb2-104">Alle ausstehenden Aktualisierungen für ein **[Recordset](recordset-object-dao.md)** -Objekt werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="60bb2-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="60bb2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60bb2-105">Syntax</span></span>

<span data-ttu-id="60bb2-106">*Ausdruck* . CancelUpdate (***UpdateType***)</span><span class="sxs-lookup"><span data-stu-id="60bb2-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="60bb2-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="60bb2-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="60bb2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="60bb2-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60bb2-109">Name</span><span class="sxs-lookup"><span data-stu-id="60bb2-109">Name</span></span></p></th>
<th><p><span data-ttu-id="60bb2-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="60bb2-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="60bb2-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="60bb2-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="60bb2-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60bb2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60bb2-113"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="60bb2-113"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="60bb2-114">Optional</span><span class="sxs-lookup"><span data-stu-id="60bb2-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="60bb2-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="60bb2-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="60bb2-116">Legen Sie auf einen der Werte <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="60bb2-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p><p><span data-ttu-id="60bb2-117"><strong>Hinweis</strong>: die Werte <EM>DbUpdateRegular</EM> und <EM>DbUpdateBatch</EM> sind nur gültig, wenn Batchaktualisierungen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="60bb2-117"><strong>NOTE</strong>: The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="60bb2-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60bb2-118">Remarks</span></span>

<span data-ttu-id="60bb2-p101">Mit der **CancelUpdate**-Methode können Sie alle ausstehenden Aktualisierungen abbrechen, die aus einer **[Edit](recordset2-edit-method-dao.md)** - oder **[AddNew](recordset2-addnew-method-dao.md)** -Operation stammen. Wenn ein Benutzer z. B. die **Edit**- oder **AddNew**-Methode aufruft, ohne vorher die **Update**-Methode aufgerufen zu haben, werden durch die **CancelUpdate**-Methode alle Änderungen abgebrochen, die nach dem Aufrufen von **Edit** oder **AddNew** vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="60bb2-p101">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset2-edit-method-dao.md)** or **[AddNew](recordset2-addnew-method-dao.md)** operation. For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="60bb2-121">Überprüfen Sie die **[EditMode](recordset2-editmode-property-dao.md)** -Eigenschaft des **Recordset**-Objekts, um zu ermitteln, ob eine Operation aussteht, die abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="60bb2-121">Check the **[EditMode](recordset2-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="60bb2-122">[!HINWEIS] Die Verwendung der **CancelUpdate**-Methode hat dieselbe Wirkung wie das Verschieben zu einem anderen Datensatz, ohne die **[Update](recordset2-update-method-dao.md)** -Methode zu verwenden. Der einzige Unterschied besteht darin, dass der aktuelle Datensatz nicht geändert wird und dass verschiedene Eigenschaften nicht aktualisiert werden, z. B. **[BOF](recordset2-bof-property-dao.md)** und **[EOF](recordset2-eof-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="60bb2-122">Using the **CancelUpdate** method has the same effect as moving to another record without using the **[Update](recordset2-update-method-dao.md)** method, except that the current record doesn't change, and various properties, such as **[BOF](recordset2-bof-property-dao.md)** and **[EOF](recordset2-eof-property-dao.md)**, aren't updated.</span></span>

## <a name="example"></a><span data-ttu-id="60bb2-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="60bb2-123">Example</span></span>

<span data-ttu-id="60bb2-124">Dieses Beispiel zeigt, wie die Methoden **CancelUpdate** und **AddNew** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="60bb2-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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

<span data-ttu-id="60bb2-125">Dieses Beispiel zeigt, wie die Methoden **CancelUpdate** und **Edit** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="60bb2-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

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

