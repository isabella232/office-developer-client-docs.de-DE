---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a293c86b2e695c32b8debaf0b3b96d7490677933
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625385"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht die Verantwortung für das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMAPISupport::Subscribe-Methode](imapisupport-subscribe.md) eingerichtet wurde. 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Nicht-Null-Verbindungsnummer, die die zuvor über **IMAPISupport::Subscribe** eingerichtete Benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungsregistrierung wurde abgebrochen.
    
MAPI_E_NOT_FOUND 
  
> Die im  _ulConnection-Parameter_ übergebene Verbindungsnummer ist nicht vorhanden. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::Unsubscribe-Methode** wird für alle Supportobjekte des Dienstanbieters implementiert. Dienstanbieter rufen **Unsubscribe** auf, um eine zuvor durch **Abonnieren** eingerichtete Benachrichtigungsregistrierung abzubrechen. **Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call. 
  
Im Allgemeinen wird die **IUnknown::Release-Methode** der Empfehlungssenke während des **Unsubscribe-Aufrufs** aufgerufen. Wenn jedoch ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für das Advise-Senkenobjekt aufruft, wird der **Release-Aufruf** verzögert, bis die **OnNotify-Methode** zurückgegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

