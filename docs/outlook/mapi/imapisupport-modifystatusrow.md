---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 06a5c9de5c0ce4c0f936791086a731a55510a124
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592143"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ändert die Statustabelle durch eine neue Zeile hinzufügen oder Ändern einer vorhandenen Zeile.
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _cValues_
  
> [in] Die Anzahl der Eigenschaften in die neue oder geänderte Status Tabellenzeile enthalten sein. 
    
 _lpColumnVals_
  
> [in] Ein Zeiger auf ein Array der Eigenschaftswerte, die beschreiben die Eigenschaften als Spalten in der neuen oder geänderten Status Tabellenzeile eingeschlossen werden sollen.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie Informationen, die die Status Tabellenzeile definieren verarbeitet wird. Das folgende Flag kann festgelegt werden:
    
STATUSROW_UPDATE 
  
> Weist das MAPI zum Zusammenführen der Eigenschaften im Array auf den _LpColumnVals_ mit einer vorhandenen Tabelle Statuszeile, statt die Daten in eine neue Zeile enthalten. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Statustabelle wurde erfolgreich aktualisiert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::ModifyStatusRow** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert. Dienstanbieter rufen **ModifyStatusRow** Sie bei der Anmeldung, um die Statustabelle eine Zeile hinzuzufügen und zu anderen Zeiten während der Sitzung auf die Zeile zu aktualisieren. **ModifyStatusRow** bietet MAPI die erforderlichen Informationen für die Statustabelle zu erstellen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie das STATUSROW_UPDATE-Flag beim Aufruf **ModifyStatusRow** so ändern Sie die Eigenschaften in Ihrer vorhandenen Status Tabellenzeile. Auf diese Weise informiert MAPI an, dass nur die Spalten, die geändert wird im _LpColumnVals_ -Parameter übergeben werden. 
  
Clients können die Informationen in der Tabelle "Status" verwenden, den Zugriff auf Ihr Statusobjekt. 
  
Eine vollständige Liste der Spalten, die in der Statuszeile Tabelle aufgenommen werden sollen, finden Sie unter [Statustabellen](status-tables.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

