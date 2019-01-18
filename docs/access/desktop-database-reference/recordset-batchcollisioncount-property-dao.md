---
title: Recordset.BatchCollisionCount-Eigenschaft (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711938"
---
# <a name="recordsetbatchcollisioncount-property-dao"></a><span data-ttu-id="c32e1-102">Recordset.BatchCollisionCount-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="c32e1-102">Recordset.BatchCollisionCount property (DAO)</span></span>


<span data-ttu-id="c32e1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c32e1-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c32e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c32e1-104">Syntax</span></span>

<span data-ttu-id="c32e1-105">*Ausdruck* . BatchCollisionCount</span><span class="sxs-lookup"><span data-stu-id="c32e1-105">*expression* .BatchCollisionCount</span></span>

<span data-ttu-id="c32e1-106">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c32e1-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c32e1-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c32e1-107">Remarks</span></span>

<span data-ttu-id="c32e1-p101">Diese Eigenschaft gibt die Anzahl von Datensätzen an, bei denen Konflikte oder andere Fehler beim letzten Versuch einer Batchaktualisierung auftraten. Der Wert dieser Eigenschaft entspricht der Anzahl von Textmarken in der **[BatchCollisions](recordset-batchcollisions-property-dao.md)** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c32e1-p101">This property indicates how many records encountered collisions or otherwise failed to update during the last batch update attempt. The value of this property corresponds to the number of bookmarks in the **[BatchCollisions](recordset-batchcollisions-property-dao.md)** property.</span></span>

<span data-ttu-id="c32e1-110">Wenn Sie die **[Bookmark](recordset-object-dao.md)** -Eigenschaft des aktiven **[Recordset](recordset-bookmark-property-dao.md)** -Objekts auf Textmarkenwerte im **BatchCollisions**-Array festlegen, können Sie zu jedem Datensatz wechseln, bei dem die letzte **[Update](recordset-update-method-dao.md)** -Batchoperation nicht abgeschlossen werden konnte.</span><span class="sxs-lookup"><span data-stu-id="c32e1-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch **[Update](recordset-update-method-dao.md)** operation.</span></span>

<span data-ttu-id="c32e1-111">Nachdem die Datensätze, die einen Konflikt verursacht haben, korrigiert wurden, kann erneut eine **Update**-Methode im Batchmodus aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c32e1-111">After the collision records are corrected, a batch-mode **Update** method can be called again.</span></span> <span data-ttu-id="c32e1-112">DAO versucht eine weitere Batchaktualisierung, und die **BatchCollisions**-Eigenschaft spiegelt die Datensatzgruppe wider, die beim zweiten Versuch nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="c32e1-112">At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt.</span></span> <span data-ttu-id="c32e1-113">Alle Datensätze, die in der vorherigen Versuch erfolgreich abgeschlossen werden nicht in der aktuellen Versuch gesendet, da sie nun eine **[RecordStatus](recordset-recordstatus-property-dao.md)** -Eigenschaft der Wert DbRecordUnmodified aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c32e1-113">Any records that succeeded in the previous attempt are not sent in the current attempt, because they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified.</span></span> <span data-ttu-id="c32e1-114">Dieser Vorgang wird so lange fortgesetzt, bis keine Konflikte mehr auftreten oder bis Sie die Aktualisierung abbrechen und die Ergebnismenge schließen.</span><span class="sxs-lookup"><span data-stu-id="c32e1-114">This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

## <a name="example"></a><span data-ttu-id="c32e1-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c32e1-115">Example</span></span>

<span data-ttu-id="c32e1-116">Dieses Beispiel verwendet die **BatchCollisionCount**-Eigenschaft und die **Update**-Methode und zeigt eine Batchaktualisierung, bei der Konflikte durch Erzwingen der Aktualisierung gelöst werden.</span><span class="sxs-lookup"><span data-stu-id="c32e1-116">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

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

