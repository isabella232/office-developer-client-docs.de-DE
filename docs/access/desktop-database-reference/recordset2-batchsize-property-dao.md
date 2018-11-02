---
title: Recordset2.BatchSize-Eigenschaft (DAO)
TOCTitle: BatchSize Property
ms:assetid: fa7f12f6-36c8-5aad-31d2-668cfe46f9f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837054(v=office.15)
ms:contentKeyID: 48548846
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d3ab4a22bc3c86e89addd07d3fabe7d5ce0e8bc3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921278"
---
# <a name="recordset2batchsize-property-dao"></a><span data-ttu-id="0094c-102">Recordset2.BatchSize-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="0094c-102">Recordset2.BatchSize property (DAO)</span></span>


<span data-ttu-id="0094c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0094c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="0094c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0094c-104">Syntax</span></span>

<span data-ttu-id="0094c-105">*Ausdruck* . BatchSize</span><span class="sxs-lookup"><span data-stu-id="0094c-105">*expression* .BatchSize</span></span>

<span data-ttu-id="0094c-106">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="0094c-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0094c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0094c-107">Remarks</span></span>

<span data-ttu-id="0094c-p101">Die **BatchSize**-Eigenschaft stellt die Batchgröße fest, die beim Senden von Anweisungen an den Server bei einer Batchaktualisierung verwendet wurde. Der Wert der Eigenschaft gibt die Anzahl der Anweisungen an, die in einem Befehlspuffer an den Server gesendet wurden. Standardmäßig werden in jedem Batch 15 Anweisungen an den Server gesendet. Diese Eigenschaft kann jederzeit geändert werden. Wenn ein Datenbankserver die Batchverarbeitung von Anweisungen nicht unterstützt, können Sie diese Eigenschaft auf 1 setzen, sodass jede Anweisung einzeln gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0094c-p101">The **BatchSize** property determines the batch size used when sending statements to the server in a batch update. The value of the property determines the number of statements sent to the server in one command buffer. By default, 15 statements are sent to the server in each batch. This property can be changed at any time. If a database server doesn't support statement batching, you can set this property to 1, causing each statement to be sent separately.</span></span>

## <a name="example"></a><span data-ttu-id="0094c-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0094c-113">Example</span></span>

<span data-ttu-id="0094c-114">In diesem Beispiel werden die Eigenschaften **BatchSize** und **UpdateOptions** verwendet, um Aspekte von Batchaktualisierungen für das angegebene Recordset-Objekt zu steuern.</span><span class="sxs-lookup"><span data-stu-id="0094c-114">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified Recordset object.</span></span>

```vb
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
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
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

