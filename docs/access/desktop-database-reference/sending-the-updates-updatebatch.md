---
title: 'Senden der Aktualisierungen: UpdateBatch'
TOCTitle: 'Sending the updates: UpdateBatch'
ms:assetid: a840b9a7-7ccd-9c31-7951-8921dadf381e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249778(v=office.15)
ms:contentKeyID: 48546898
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7da0320bf42d1a1720bccfe8bf9e3843a2bb94f5
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946937"
---
# <a name="sending-the-updates-updatebatch"></a>Senden der Aktualisierungen: UpdateBatch


**Betrifft**: Access 2013, Office 2013

## <a name="sending-the-updates-updatebatch-method"></a>Senden der Aktualisierungen: UpdateBatch-Methode

Mit dem folgenden Code wird ein **Recordset** -Objekt im Batchmodus geöffnet, indem die **LockType** -Eigenschaft auf **adLockBatchOptimistic** und die **CursorLocation** auf **adUseClient** festgelegt wird. Zwei neue Datensätze werden hinzugefügt, und der Wert eines Felds in einem vorhandenen Datensatz wird geändert, wobei die ursprünglichen Werte gespeichert werden. Anschließend wird **UpdateBatch** aufgerufen, um die Änderungen an die Datenquelle zurückzusenden.

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

Wenn Sie den aktuellen Datensatz bearbeiten oder beim Aufrufen der **UpdateBatch** -Methode einen neuen Datensatz hinzufügen, ruft ADO automatisch die **Update** -Methode auf, um ausstehende Änderungen am aktuellen Datensatz zu speichern, bevor die Batchänderungen an den Anbieter übertragen werden.

