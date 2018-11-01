---
title: Recordset.CancelUpdate Method (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0112d094829753f5b012de80245f93fef3a2a472
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880355"
---
# <a name="recordsetcancelupdate-method-dao"></a><span data-ttu-id="b2f11-102">Recordset.CancelUpdate Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="b2f11-102">Recordset.CancelUpdate Method (DAO)</span></span>


<span data-ttu-id="b2f11-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2f11-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2f11-104">Alle ausstehenden Aktualisierungen für ein **[Recordset](recordset-object-dao.md)** -Objekt werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b2f11-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f11-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2f11-105">Syntax</span></span>

<span data-ttu-id="b2f11-106">*Ausdruck* . CancelUpdate (***UpdateType***)</span><span class="sxs-lookup"><span data-stu-id="b2f11-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="b2f11-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2f11-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b2f11-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2f11-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2f11-109">Name</span><span class="sxs-lookup"><span data-stu-id="b2f11-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b2f11-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="b2f11-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b2f11-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b2f11-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b2f11-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2f11-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2f11-113">UpdateType</span><span class="sxs-lookup"><span data-stu-id="b2f11-113">UpdateType</span></span></p></td>
<td><p><span data-ttu-id="b2f11-114">Optional</span><span class="sxs-lookup"><span data-stu-id="b2f11-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="b2f11-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="b2f11-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="b2f11-116">Legen Sie auf einen der Werte <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="b2f11-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="b2f11-117">Die Werte <EM>DbUpdateRegular</EM> und <EM>DbUpdateBatch</EM> sind nur gültig, wenn Batchaktualisierungen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b2f11-117">The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></P>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b2f11-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2f11-118">Remarks</span></span>

<span data-ttu-id="b2f11-p101">Mit der **CancelUpdate**-Methode können Sie alle ausstehenden Aktualisierungen abbrechen, die aus einer **[Edit](recordset-edit-method-dao.md)** - oder **[AddNew](recordset-addnew-method-dao.md)** -Operation stammen. Wenn ein Benutzer z. B. die **Edit**- oder **AddNew**-Methode aufruft, ohne vorher die **Update**-Methode aufgerufen zu haben, werden durch die **CancelUpdate**-Methode alle Änderungen abgebrochen, die nach dem Aufrufen von **Edit** oder **AddNew** vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="b2f11-p101">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** operation. For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="b2f11-121">Überprüfen Sie die **[EditMode](recordset-editmode-property-dao.md)** -Eigenschaft des **Recordset**-Objekts, um zu ermitteln, ob eine Operation aussteht, die abgebrochen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2f11-121">Check the **[EditMode](recordset-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b2f11-122">[!HINWEIS] Die Verwendung der <STRONG>CancelUpdate</STRONG>-Methode hat dieselbe Wirkung wie das Verschieben zu einem anderen Datensatz, ohne die <STRONG><A href="recordset-update-method-dao.md">Update</A></STRONG> -Methode zu verwenden. Der einzige Unterschied besteht darin, dass der aktuelle Datensatz nicht geändert wird und dass verschiedene Eigenschaften nicht aktualisiert werden, z. B. <STRONG><A href="recordset-bof-property-dao.md">BOF</A></STRONG> und <STRONG><A href="recordset-eof-property-dao.md">EOF</A></STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b2f11-122">Using the <STRONG>CancelUpdate</STRONG> method has the same effect as moving to another record without using the <STRONG><A href="recordset-update-method-dao.md">Update</A></STRONG> method, except that the current record doesn't change, and various properties, such as <STRONG><A href="recordset-bof-property-dao.md">BOF</A></STRONG> and <STRONG><A href="recordset-eof-property-dao.md">EOF</A></STRONG>, aren't updated.</span></span></P>



## <a name="example"></a><span data-ttu-id="b2f11-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b2f11-123">Example</span></span>

<span data-ttu-id="b2f11-124">Dieses Beispiel zeigt, wie die Methoden **CancelUpdate** und **AddNew** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="b2f11-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

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

<span data-ttu-id="b2f11-125">Dieses Beispiel zeigt, wie die Methoden **CancelUpdate** und **Edit** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="b2f11-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

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

