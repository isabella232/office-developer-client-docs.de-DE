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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341265"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht die Zuständigkeit für das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMAPISupport:: subscribe](imapisupport-subscribe.md) -Methode eingerichtet wurden. 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> in Die ungleich NULL-Verbindungsnummer, die die Benachrichtigungs Registrierung darstellt, die zuvor über **IMAPISupport:: subscribe**eingerichtet wurde.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungs Registrierung wurde abgebrochen.
    
MAPI_E_NOT_FOUND 
  
> Die im _ulConnection_ -Parameter übergebene Verbindungsnummer ist nicht vorhanden. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: unsubscribe** -Methode wird für alle Support Objekte des Dienstanbieters implementiert. Dienstanbieter rufen das **Abonnement** ab, um eine zuvor von **subscribe**eingestellte Benachrichtigungs Registrierung abzubrechen. Kündigen Sie das **Abonnement** , indem Sie den Zeiger für die Advise-Senke freigeben, der im **subscribe** -Aufruf übergeben wurde. 
  
Im Allgemeinen wird die **IUnknown:: Release** -Methode der Advise-Senke **** während des unsubscribe-Aufrufs aufgerufen. Wenn jedoch ein anderer Thread die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode für das Advise-Senke-Objekt aufruft, wird der **Freigabe** Aufruf verzögert, bis **** die OnNotify-Methode zurückgegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

