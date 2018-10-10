---
title: Recordset.BatchSize Property (DAO)
TOCTitle: BatchSize Property
ms:assetid: f03dc505-682f-4b60-62f2-1bd088d873c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836544(v=office.15)
ms:contentKeyID: 48548599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101179
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d67c87be0a3ffb7bc9d7b349746e397bb19a9c63
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475317"
---
# <a name="recordsetbatchsize-property-dao"></a><span data-ttu-id="827e7-102">Recordset.BatchSize Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="827e7-102">Recordset.BatchSize Property (DAO)</span></span>


<span data-ttu-id="827e7-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="827e7-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="827e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="827e7-104">Syntax</span></span>

<span data-ttu-id="827e7-105">*Ausdruck* . BatchSize</span><span class="sxs-lookup"><span data-stu-id="827e7-105">*expression* .BatchSize</span></span>

<span data-ttu-id="827e7-106">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="827e7-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="827e7-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="827e7-107">Remarks</span></span>

<span data-ttu-id="827e7-p101">Die **BatchSize**-Eigenschaft stellt die Batchgröße fest, die beim Senden von Anweisungen an den Server bei einer Batchaktualisierung verwendet wurde. Der Wert der Eigenschaft gibt die Anzahl der Anweisungen an, die in einem Befehlspuffer an den Server gesendet wurden. Standardmäßig werden in jedem Batch 15 Anweisungen an den Server gesendet. Diese Eigenschaft kann jederzeit geändert werden. Wenn ein Datenbankserver die Batchverarbeitung von Anweisungen nicht unterstützt, können Sie diese Eigenschaft auf 1 setzen, sodass jede Anweisung einzeln gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="827e7-p101">The **BatchSize** property determines the batch size used when sending statements to the server in a batch update. The value of the property determines the number of statements sent to the server in one command buffer. By default, 15 statements are sent to the server in each batch. This property can be changed at any time. If a database server doesn't support statement batching, you can set this property to 1, causing each statement to be sent separately.</span></span>

## <a name="example"></a><span data-ttu-id="827e7-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="827e7-113">Example</span></span>

<span data-ttu-id="827e7-114">In diesem Beispiel werden die Eigenschaften **BatchSize** und **UpdateOptions** verwendet, um Aspekte von Batchaktualisierungen für das angegebene Recordset-Objekt zu steuern.</span><span class="sxs-lookup"><span data-stu-id="827e7-114">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified Recordset object.</span></span>

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
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

