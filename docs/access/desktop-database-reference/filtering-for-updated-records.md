---
title: Filtern nach aktualisierten Datensätzen
TOCTitle: Filtering for updated records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 791cbbd16eef7baf95fd51ab8624a04dc687166b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292398"
---
# <a name="filtering-for-updated-records"></a>Filtern nach aktualisierten Datensätzen

**Gilt für**: Access 2013, Office 2013

## <a name="filtering-for-updated-records"></a>Filtern nach aktualisierten Datensätzen

Bevor Sie **UpdateBatch** aufrufen, können Sie mit der **Filter** -Eigenschaft des **Recordset** -Objekts nur die Datensätze anzeigen, die geändert wurden, seit das **Recordset** -Objekt zuletzt geöffnet wurde oder seit **UpdateBatch** zuletzt aufgerufen wurde. Legen Sie dazu, wie im Folgenden dargestellt, **Filter** auf **adFilterPendingRecords** fest, um zu bestimmen, wie viele Datensätze aktualisiert werden.

Dieses Beispiel erweitert das vorherige **UpdateBatch** -Beispiel, indem das **Recordset** -Objekt direkt vor dem Aufruf von **UpdateBatch** gefiltert wird und dem Benutzer die Datensätze angezeigt werden, die geändert werden, und der Benutzer die Möglichkeit zum Abbrechen der Aktualisierung erhält (mithilfe der **CancelBatch** -Methode).

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

