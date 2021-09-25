---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: af7fbea1e9e6ef6be8da08a296c85e3124d7800a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556378"
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
  
> Die Nachricht sollte gesperrt sein. 
    
MSG_UNLOCKED 
  
> Die Nachricht sollte entsperrt sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Sperrstatus der Nachricht wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgStore::SetLockState-Methode** sperrt oder entsperrt eine Nachricht. **SetLockState** kann nur vom MAPI-Spooler aufgerufen werden, während die Nachricht gesendet wird. 
  
Wenn der MAPI-Spooler **SetLockState** aufruft, um eine Nachricht zu sperren, wird in der Regel nur die älteste Nachricht gesperrt (d. a. die nächste Nachricht, die für den MAPI-Spooler in die Warteschlange eingereiht wird, die gesendet werden soll). Wenn die älteste Nachricht in der Warteschlange auf einen vorübergehend nicht verfügbaren Transportanbieter wartet und die nächste Nachricht in der Warteschlange einen anderen Transportanbieter verwendet, kann der MAPI-Spooler mit der Verarbeitung der späteren Nachricht beginnen. Sie beginnt mit der Verarbeitung, indem diese Nachricht mithilfe von **SetLockState** gesperrt wird.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Nachdem der MAPI-Spooler **SetLockState** aufgerufen hat und der  _ulLockState-Parameter_ auf MSG_LOCKED festgelegt ist, müssen Aufrufe der [IMsgStore::AbortSubmit-Methode](imsgstore-abortsubmit.md) zum Abbrechen der Übertragung der Nachricht fehlschlagen. 
  
Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht in Der **SetLockState-Implementierung** auf, damit alle Änderungen, die an der Nachricht vorgenommen wurden, bevor der **SetLockState-Aufruf** empfangen wurde, gespeichert werden. 
  
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

