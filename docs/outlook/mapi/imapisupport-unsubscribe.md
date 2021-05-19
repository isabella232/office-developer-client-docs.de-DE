---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f27da216b9c474aa31503917a6d3c7a74eab9c4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421214"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht die Verantwortung für das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMAPISupport::Subscribe-Methode eingerichtet](imapisupport-subscribe.md) wurden. 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Verbindungsnummer ungleich Null, die die Benachrichtigungsregistrierung darstellt, die zuvor über **IMAPISupport::Subscribe eingerichtet wurde.**
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungsregistrierung wurde abgebrochen.
    
MAPI_E_NOT_FOUND 
  
> Die im  _ulConnection-Parameter übergebene_ Verbindungsnummer ist nicht vorhanden. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::Unsubscribe-Methode** wird für alle Dienstanbieterunterstützungsobjekte implementiert. Dienstanbieter rufen **Unsubscribe auf,** um eine Benachrichtigungsregistrierung zu kündigen, die zuvor von **Subscribe eingerichtet wurde.** **Unsubscribe** bricht die Registrierung ab, indem der im Aufruf Abonnieren übergebene Hinweissenkenzeiger **loslassen** wird. 
  
Im Allgemeinen wird die **IUnknown::Release-Methode** der Ratensenke während des **Unsubscribe-Aufrufs** aufgerufen. Wenn jedoch ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für das Advise Sink-Objekt aufruft, wird der **Release-Aufruf** verzögert, bis die **OnNotify-Methode** zurückgegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

