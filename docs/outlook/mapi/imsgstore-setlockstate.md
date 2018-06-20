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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a4e924489f2ec656f473f28407d528e9c2ddda5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792628"
---
# <a name="imsgstoresetlockstate"></a>IMsgStore::SetLockState

  
  
**Betrifft**: Outlook 
  
Sperrt oder entsperrt eine Nachricht. Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Ein Zeiger auf die Nachricht zu sperren oder entsperren.
    
 _ulLockState_
  
> [in] Ein Wert, der angibt, ob die Nachricht gesperrt oder entsperrt werden soll. Einer der folgenden Werte ist gültig:
    
MSG_LOCKED 
  
> Die Nachricht sollte gesperrt werden. 
    
MSG_UNLOCKED 
  
> Die Nachricht muss aufgehoben werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Sperrstatus der Nachricht wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::SetLockState** -Methode sperrt oder entsperrt eine Nachricht. **SetLockState** kann nur durch die MAPI-Warteschlange aufgerufen werden, während sie die Nachricht gesendet hat. 
  
In der Regel, wenn die Warteschlange MAPI **SetLockState** So sperren Sie eine Nachricht aufruft, sperrt er nur die älteste Nachricht (d. h., die nächste Nachricht in der Warteschlange für die MAPI-Warteschlange senden). Wenn der ältesten Nachrichten in der Warteschlange darauf, dass eines Transportdienstes vorübergehend nicht verfügbar wartet, und die nächste Nachricht in der Warteschlange ein anderen Transportdienstes verwendet, kann die MAPI-Warteschlange verarbeitet die Nachricht spätere beginnen. Verarbeitung beginnt durch das Sperren dieser Nachricht mithilfe von **SetLockState**.
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Nachdem die MAPI-Warteschlange mit der _UlLockState_ -Parameter auf MSG_LOCKED **SetLockState** aufgerufen, müssen Aufrufe an die [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) -Methode die Nachricht Übertragung abzubrechen fehl. 
  
Rufen Sie die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode in der Implementierung **SetLockState** , sodass alle Änderungen, die an die Nachricht vorgenommen wurden, bevor der Anruf **SetLockState** eingegangen gespeichert werden. 
  
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

