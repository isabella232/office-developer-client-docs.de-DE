---
title: Filtern nach aktualisierten Datensätzen
TOCTitle: Filtering for Updated Records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 54183ddff6cfb3f3648bc367588aa49dc17a13fe
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867755"
---
# <a name="filtering-for-updated-records"></a><span data-ttu-id="32db6-102">Filtern nach aktualisierten Datensätzen</span><span class="sxs-lookup"><span data-stu-id="32db6-102">Filtering for Updated Records</span></span>


<span data-ttu-id="32db6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="32db6-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="filtering-for-updated-records"></a><span data-ttu-id="32db6-104">Filtering for Updated Records</span><span class="sxs-lookup"><span data-stu-id="32db6-104">Filtering for Updated Records</span></span>

<span data-ttu-id="32db6-p101">Bevor Sie **UpdateBatch** aufrufen, können Sie mit der **Filter** -Eigenschaft des **Recordset** -Objekts nur die Datensätze anzeigen, die geändert wurden, seit das **Recordset** -Objekt zuletzt geöffnet wurde oder seit **UpdateBatch** zuletzt aufgerufen wurde. Legen Sie dazu, wie im Folgenden dargestellt, **Filter** auf **adFilterPendingRecords** fest, um zu bestimmen, wie viele Datensätze aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="32db6-p101">Before you call **UpdateBatch**, you can use the **Recordset** **Filter** property to view only those records which have been changed since the **Recordset** was opened or the last call to **UpdateBatch**. To do this, set **Filter** equal to **adFilterPendingRecords** to determine how many records will be updated, as shown below.</span></span>

<span data-ttu-id="32db6-107">Dieses Beispiel erweitert das vorherige **UpdateBatch** -Beispiel, indem das **Recordset** -Objekt direkt vor dem Aufruf von **UpdateBatch** gefiltert wird und dem Benutzer die Datensätze angezeigt werden, die geändert werden, und der Benutzer die Möglichkeit zum Abbrechen der Aktualisierung erhält (mithilfe der **CancelBatch** -Methode).</span><span class="sxs-lookup"><span data-stu-id="32db6-107">This example extends the previous **UpdateBatch** example by filtering the **Recordset** just before calling the **UpdateBatch**, showing the user which records will change and allowing her to cancel the update (using the **CancelBatch** method).</span></span>

```vb 
 
'BeginFilterAffected 
    objRs1.Filter = adFilterPendingRecords 
    objRs1.MoveFirst 
     
    strMsg = "The following " & objRs1.RecordCount & " values will " & _ 
             "be updated. Do you wish to proceed?" 
    While Not objRs1.EOF 
        strMsg = strMsg & vbCrLf & objRs1(0) & vbTab & objRs1(1) & vbTab & _ 
                 objRs1(2) & vbCrLf 
        objRs1.MoveNext 
    Wend 
     
    blnResp = MsgBox(strMsg, vbYesNo, "Proceed with Update?") 
    If blnResp = True Then 
        objRs1.UpdateBatch 
    Else 
        objRs1.CancelBatch 
    End If 
'EndFilterAffected 
```

