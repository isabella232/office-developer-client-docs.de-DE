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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348748"
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
  
> in Ein Zeiger auf die Nachricht zum Sperren oder entsperren.
    
 _ulLockState_
  
> in Ein Wert, der angibt, ob die Nachricht gesperrt oder entsperrt werden soll. Einer der folgenden Werte ist gültig:
    
MSG_LOCKED 
  
> Die Nachricht sollte gesperrt sein. 
    
MSG_UNLOCKED 
  
> Die Nachricht sollte entsperrt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Sperrstatus der Nachricht wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMsgStore:: SetLockState** -Methode wird eine Nachricht gesperrt oder aufgehoben. **SetLockState** kann nur vom MAPI-Spooler aufgerufen werden, wenn die Nachricht gesendet wird. 
  
Wenn der MAPI-Spooler **SetLockState** zum Sperren einer Nachricht aufruft, sperrt er in der Regel nur die älteste Nachricht (also die nächste Nachricht, die in der Warteschlange für den zu sendenden MAPI-Spooler steht). Wenn die älteste Nachricht in der Warteschlange auf einen vorübergehend nicht verfügbaren Transportanbieter wartet und die nächste Nachricht in der Warteschlange einen anderen Transportanbieter verwendet, kann der MAPI-Spooler mit der Verarbeitung der späteren Nachricht beginnen. Die Verarbeitung wird gestartet, indem diese Nachricht mithilfe von **SetLockState**gesperrt wird.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Nachdem der MAPI-Spooler **SetLockState** aufgerufen hat, wobei der Parameter _ulLockState_ auf MSG_LOCKED festgelegt ist, müssen Aufrufe an die [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) -Methode zum Abbrechen der Nachrichtenübertragung fehlschlagen. 
  
Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Nachricht in der **SetLockState** -Implementierung auf, sodass alle Änderungen, die an der Nachricht vorgenommen wurden, bevor der **SetLockState** -Aufruf empfangen wurde, gespeichert werden. 
  
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

