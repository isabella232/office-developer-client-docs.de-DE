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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316642"
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
  
> in Die Anzahl der Eigenschaften, die in die neue oder geänderte Statustabellen Zeile eingeschlossen werden sollen. 
    
 _lpColumnVals_
  
> in Ein Zeiger auf ein Array von Eigenschaftswerten, die die Eigenschaften beschreiben, die als Spalten in die neue oder geänderte Statustabellen Zeile eingeschlossen werden sollen.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie Informationen, die die Statustabellen Zeile definieren, verarbeitet werden. Das folgende Flag kann festgelegt werden:
    
STATUSROW_UPDATE 
  
> Weist MAPI an, die Eigenschaften, die im Array enthalten sind, von _lpColumnVals_ mit einer vorhandenen Statustabellen Zeile anstatt in einer neuen Zeile zusammenzuführen. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Statustabelle wurde erfolgreich aktualisiert.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: ModifyStatusRow** -Methode wird für alle Support Objekte des Dienstanbieters implementiert. Dienstanbieter rufen **ModifyStatusRow** bei der Anmeldung auf, um der Statustabelle und zu anderen Zeiten während der Sitzung eine Zeile hinzuzufügen, um die Zeile zu aktualisieren. **ModifyStatusRow** bietet MAPI die zum Erstellen der Statustabelle erforderlichen Informationen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Legen Sie das STATUSROW_UPDATE-Flag fest, wenn Sie **ModifyStatusRow** aufrufen, um Änderungen an den Eigenschaften in der vorhandenen Statustabellen Zeile vorzunehmen. Auf diese Weise wird MAPI darüber informiert, dass nur die geänderten Spalten an den _lpColumnVals_ -Parameter übergeben werden. 
  
Clients können die Informationen in der Statustabelle verwenden, um auf Ihr Status-Objekt zuzugreifen. 
  
Eine vollständige Liste der Spalten, die Sie in die Statustabellen Zeile aufnehmen sollten, finden Sie unter [Statustabellen](status-tables.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport: IUnknown](imapisupportiunknown.md)

