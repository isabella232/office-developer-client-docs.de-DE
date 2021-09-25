---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 19292d41e04b4a80d69ce68a1961c1deacbfde71
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625427"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ändert die Statustabelle, indem eine neue Zeile hinzugefügt oder eine vorhandene Zeile geändert wird.
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _cValues_
  
> [in] Die Anzahl der Eigenschaften, die in der neuen oder geänderten Statustabellenzeile enthalten sein sollen. 
    
 _lpColumnVals_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftswerten, die die Eigenschaften beschreiben, die als Spalten in der neuen oder geänderten Statustabellenzeile eingeschlossen werden sollen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie Informationen, die die Statustabellenzeile definieren, verarbeitet werden. Das folgende Kennzeichen kann festgelegt werden:
    
STATUSROW_UPDATE 
  
> Weist die MAPI an, die Eigenschaften in dem Array zusammenzuführen, auf das von  _lpColumnVals_ mit einer vorhandenen Statustabellenzeile und nicht in einer neuen Zeile verwiesen wird. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Statustabelle wurde erfolgreich aktualisiert.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::ModifyStatusRow-Methode** wird für alle Dienstanbieter-Supportobjekte implementiert. Dienstanbieter rufen **ModifyStatusRow** bei der Anmeldung auf, um der Statustabelle eine Zeile hinzuzufügen, und zu anderen Zeiten während der Sitzung, um die Zeile zu aktualisieren. **ModifyStatusRow** stellt der MAPI die informationen bereit, die zum Erstellen der Statustabelle erforderlich sind. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie das flag STATUSROW_UPDATE fest, wenn Sie **ModifyStatusRow** aufrufen, um Änderungen an den Eigenschaften in der vorhandenen Statustabellenzeile vorzunehmen. Dadurch wird die MAPI darüber informiert, dass nur die geänderten Spalten im  _LpColumnVals-Parameter_ übergeben werden. 
  
Clients können die Informationen in der Statustabelle verwenden, um auf Ihr Statusobjekt zuzugreifen. 
  
Eine vollständige Liste der Spalten, die Sie in die Statustabellenzeile aufnehmen sollten, finden Sie unter [Statustabellen.](status-tables.md)
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

