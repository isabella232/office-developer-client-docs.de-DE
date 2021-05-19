---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434018"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die MAPI aufruft, um eine Ereignisbenachrichtigung zu senden. Diese Rückruffunktion kann nur verwendet werden, wenn sie in ein Advise Sink-Objekt gepackt wird, das durch Aufrufen der [HrAllocAdviseSink-Funktion erstellt](hrallocadvisesink.md) wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
|Definierte Funktion, die von:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameter

 _lpvContext_
  
> [in] Zeiger auf einen beliebigen Wert, der an die Rückruffunktion übergeben wird, wenn MAPI ihn aufruft. Dieser Wert kann eine Adresse darstellen, die für die Clientanwendung oder den Dienstanbieter von Bedeutung ist. Normalerweise stellt der  _lpvContext-Parameter_ für C++-Code einen Zeiger auf ein C++-Objekt dar. 
    
 _cNotification_
  
> [in] Anzahl der Ereignisbenachrichtigungen im Array, das durch den  _lpNotifications-Parameter angegeben_ wird. 
    
 _lpNotifications_
  
> [out] Zeiger auf den Speicherort, an dem diese Funktion ein Array von [NOTIFICATION-Strukturen](notification.md) schreibt, das die Ereignisbenachrichtigungen enthält. 
    
## <a name="return-value"></a>Rückgabewert

Der Satz gültiger Rückgabewerte für den PROTOTYP der **NOTIFCALLBACK-Funktion** hängt davon ab, ob die Funktion von einer Clientanwendung oder einem Dienstanbieter implementiert wird. Clients sollten immer S_OK. Anbieter können entweder S_OK oder CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Hinweise

CALLBACK_DISCONTINUE ist ein gültiger Rückgabewert nur für synchrone Rückruffunktionen. es fordert die MAPI auf, die Verarbeitung der Rückrufe für diese Benachrichtigung sofort zu beenden. Wenn CALLBACK_DISCONTINUE zurückgegeben wird, legt MAPI den _lpUlFlags-Parameter_ auf NOTIFY_CANCELED fest, wenn er von [IMAPISupport::Notify zurückgegeben wird.](imapisupport-notify.md) 
  
Es folgen Einschränkungen, was eine synchrone Rückruffunktion tun kann:
  
- Es kann nicht dazu führen, dass eine weitere synchrone Benachrichtigung generiert wird.
    
- Es kann keine Benutzeroberfläche angezeigt werden.
    
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

