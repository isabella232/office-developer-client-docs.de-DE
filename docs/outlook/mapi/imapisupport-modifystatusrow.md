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
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417161"
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
  
> [in] Die Anzahl der Eigenschaften, die in der Zeile neue oder geänderte Statustabelle enthalten sein sollen. 
    
 _lpColumnVals_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftswerten, die die Eigenschaften beschreiben, die als Spalten in der Zeile neue oder geänderte Statustabelle enthalten sein sollen.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie Informationen verarbeitet werden, die die Statustabelle definieren. Das folgende Flag kann festgelegt werden:
    
STATUSROW_UPDATE 
  
> Weist MAPI an, die Eigenschaften im Array zusammenführen, auf die  _von lpColumnVals_ verwiesen wird, mit einer vorhandenen Statustabelleszeile, anstatt in einer neuen Zeile. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Statustabelle wurde erfolgreich aktualisiert.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::ModifyStatusRow-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert. Dienstanbieter rufen **ModifyStatusRow** zur Anmeldezeit auf, um der Statustabelle und zu anderen Zeiten während der Sitzung eine Zeile hinzuzufügen, um die Zeile zu aktualisieren. **ModifyStatusRow** stellt MAPI die informationen zur Verfügung, die zum Erstellen der Statustabelle erforderlich sind. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie das STATUSROW_UPDATE, wenn Sie **ModifyStatusRow aufrufen,** um Änderungen an den Eigenschaften in der vorhandenen Statustabelle vorzunehmen. Dadurch wird MAPI darüber informiert, dass nur die geänderten Spalten im  _lpColumnVals-Parameter übergeben_ werden. 
  
Clients können die Informationen in der Statustabelle verwenden, um auf Ihr Statusobjekt zu zugreifen. 
  
Eine vollständige Liste der Spalten, die Sie in ihre Statustabellenzeile einschließen sollten, finden Sie unter [Status Tables](status-tables.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

