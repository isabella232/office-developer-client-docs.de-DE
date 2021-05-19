---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423629"
---
# <a name="imsgstoresetlockstate"></a>IMsgStore::SetLockState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sperrt oder entsperrt eine Nachricht. Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Ein Zeiger auf die Nachricht, die gesperrt oder entsperrt werden soll.
    
 _ulLockState_
  
> [in] Ein Wert, der angibt, ob die Nachricht gesperrt oder entsperrt werden soll. Einer der folgenden Werte ist gültig:
    
MSG_LOCKED 
  
> Die Nachricht sollte gesperrt werden. 
    
MSG_UNLOCKED 
  
> Die Nachricht sollte entsperrt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Sperrstatus der Nachricht wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::SetLockState-Methode** sperrt oder sperrt eine Nachricht. **SetLockState** kann nur vom MAPI-Spooler aufgerufen werden, während die Nachricht gesendet wird. 
  
Wenn der MAPI-Spooler **SetLockState** aufruft, um eine Nachricht zu sperren, sperrt er in der Regel nur die älteste Nachricht (d. h. die nächste Nachricht, die für den zu sendenden MAPI-Spooler in die Warteschlange eingereiht ist). Wenn die älteste Nachricht in der Warteschlange auf einen vorübergehend nicht verfügbaren Transportanbieter wartet und die nächste Nachricht in der Warteschlange einen anderen Transportanbieter verwendet, kann der MAPI-Spooler mit der Verarbeitung der späteren Nachricht beginnen. Die Verarbeitung beginnt, indem diese Nachricht mithilfe von **SetLockState gesperrt wird.**
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Nachdem der MAPI-Spooler **SetLockState** aufgerufen hat und der  _ulLockState-Parameter_ auf MSG_LOCKED festgelegt ist, müssen Aufrufe der [IMsgStore::AbortSubmit-Methode](imsgstore-abortsubmit.md) zum Abbrechen der Übertragung der Nachricht fehlschlagen. 
  
Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht in Ihrer **SetLockState-Implementierung** auf, damit alle Änderungen, die an der Nachricht vorgenommen wurden, bevor der **SetLockState-Aufruf** empfangen wurde, gespeichert werden. 
  
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

