---
title: Recordset. BatchCollisionCount-Eigenschaft (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 9d166463-8313-c0f5-8389-5d5ad933eb33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198240(v=office.15)
ms:contentKeyID: 48546617
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101181
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d0c4af9744accd21a91dca2676a08cad3d1cc7e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300630"
---
# <a name="recordsetbatchcollisioncount-property-dao"></a><span data-ttu-id="f2069-102">Recordset. BatchCollisionCount-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="f2069-102">Recordset.BatchCollisionCount property (DAO)</span></span>


<span data-ttu-id="f2069-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2069-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f2069-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2069-104">Syntax</span></span>

<span data-ttu-id="f2069-105">*Ausdruck* . BatchCollisionCount</span><span class="sxs-lookup"><span data-stu-id="f2069-105">*expression* .BatchCollisionCount</span></span>

<span data-ttu-id="f2069-106">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2069-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2069-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2069-107">Remarks</span></span>

<span data-ttu-id="f2069-p101">Diese Eigenschaft gibt die Anzahl von Datensätzen an, bei denen Konflikte oder andere Fehler beim letzten Versuch einer Batchaktualisierung auftraten. Der Wert dieser Eigenschaft entspricht der Anzahl von Textmarken in der **[BatchCollisions](recordset-batchcollisions-property-dao.md)** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f2069-p101">This property indicates how many records encountered collisions or otherwise failed to update during the last batch update attempt. The value of this property corresponds to the number of bookmarks in the **[BatchCollisions](recordset-batchcollisions-property-dao.md)** property.</span></span>

<span data-ttu-id="f2069-110">Wenn Sie die **[Bookmark](recordset-object-dao.md)** -Eigenschaft des aktiven **[Recordset](recordset-bookmark-property-dao.md)** -Objekts auf Textmarkenwerte im **BatchCollisions**-Array festlegen, können Sie zu jedem Datensatz wechseln, bei dem die letzte **[Update](recordset-update-method-dao.md)** -Batchoperation nicht abgeschlossen werden konnte.</span><span class="sxs-lookup"><span data-stu-id="f2069-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch **[Update](recordset-update-method-dao.md)** operation.</span></span>

<span data-ttu-id="f2069-p102">After the collision records are corrected, a batch-mode **Update** method can be called again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, because they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span><span class="sxs-lookup"><span data-stu-id="f2069-p102">After the collision records are corrected, a batch-mode **Update** method can be called again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, because they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

## <a name="example"></a><span data-ttu-id="f2069-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f2069-115">Example</span></span>

<span data-ttu-id="f2069-116">In diesem Beispiel wird mithilfe der **BatchCollisionCount**-Eigenschaft und der **Update**-Methode die Batchaktualisierung veranschaulicht. Konflikte werden durch das Erzwingen der Batchaktualisierung gelöst.</span><span class="sxs-lookup"><span data-stu-id="f2069-116">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

