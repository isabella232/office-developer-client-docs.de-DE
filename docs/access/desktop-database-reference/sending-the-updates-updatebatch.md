---
title: 'Senden von Updates: UpdateBatch'
TOCTitle: 'Sending the updates: UpdateBatch'
ms:assetid: a840b9a7-7ccd-9c31-7951-8921dadf381e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249778(v=office.15)
ms:contentKeyID: 48546898
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca97f3ec2cbddfae4d62a72e5e6148a57abb4325
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718980"
---
# <a name="sending-the-updates-updatebatch"></a><span data-ttu-id="fa60a-102">Senden von Updates: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="fa60a-102">Sending the updates: UpdateBatch</span></span>


<span data-ttu-id="fa60a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa60a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="sending-the-updates-updatebatch-method"></a><span data-ttu-id="fa60a-104">Senden der Aktualisierungen: UpdateBatch-Methode</span><span class="sxs-lookup"><span data-stu-id="fa60a-104">Sending the Updates: UpdateBatch Method</span></span>

<span data-ttu-id="fa60a-p101">Mit dem folgenden Code wird ein **Recordset** -Objekt im Batchmodus geöffnet, indem die **LockType** -Eigenschaft auf **adLockBatchOptimistic** und die **CursorLocation** auf **adUseClient** festgelegt wird. Zwei neue Datensätze werden hinzugefügt, und der Wert eines Felds in einem vorhandenen Datensatz wird geändert, wobei die ursprünglichen Werte gespeichert werden. Anschließend wird **UpdateBatch** aufgerufen, um die Änderungen an die Datenquelle zurückzusenden.</span><span class="sxs-lookup"><span data-stu-id="fa60a-p101">The following code opens a **Recordset** in batch mode by setting the **LockType** property to **adLockBatchOptimistic** and the **CursorLocation** to **adUseClient**. It adds two new records and changes the value of a field in an existing record, saving the original values, and then calls **UpdateBatch** to send the changes back to the data source.</span></span>

```vb 
 
'BeginBatchUpdate 
    strSQL = "SELECT ShipperId, CompanyName, Phone FROM Shippers" 
                  
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
     
    ' Change value of Phone field for first record in Recordset, saving value 
    ' for later restoration. 
    intId = objRs1("ShipperId") 
    strPhone = objRs1("Phone") 
     
    objRs1("Phone") = "(111) 555-1111" 
     
    'Add two new records 
    For i = 0 To 1 
        objRs1.AddNew 
        objRs1(1) = "New Shipper #" & CStr((i + 1)) 
        objRs1(2) = "(nnn) 555-" & i & i & i & i 
    Next i 
     
    ' Send the updates 
    objRs1.UpdateBatch 
'EndBatchUpdate 
```

<span data-ttu-id="fa60a-107">Wenn Sie den aktuellen Datensatz bearbeiten oder beim Aufrufen der **UpdateBatch** -Methode einen neuen Datensatz hinzufügen, ruft ADO automatisch die **Update** -Methode auf, um ausstehende Änderungen am aktuellen Datensatz zu speichern, bevor die Batchänderungen an den Anbieter übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="fa60a-107">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

