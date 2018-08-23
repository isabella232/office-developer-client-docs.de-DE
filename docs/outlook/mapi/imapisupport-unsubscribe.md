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
ms.openlocfilehash: 01ea05eb864c78f3ded39ca3ebc62578076b9d37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584660"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Hebt die Verantwortung für Benachrichtigungen gesendet werden, die zuvor mit einem Aufruf der [IMAPISupport::Subscribe](imapisupport-subscribe.md) -Methode festgelegt wurde. 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Zahl ungleich NULL Verbindung der zuvor über **IMAPISupport::Subscribe**hergestellt benachrichtigungsregistrierung zurück.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die benachrichtigungsregistrierung wurde abgebrochen.
    
MAPI_E_NOT_FOUND 
  
> Die Nummer im _UlConnection_ -Parameter übergeben, ist nicht vorhanden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::Unsubscribe** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert. Dienstanbieter rufen Sie **kündigen** , um eine zuvor vom **Subscribe**eingerichteten benachrichtigungsregistrierung abzubrechen. **Zum Abmelden** hebt die Registrierung durch den Anruf **Subscribe** übergebene Advise Empfängerzeiger freigeben. 
  
Im Allgemeinen der Advise-Empfänger **IUnknown** -Methode aufgerufen wird während des Anrufs **zum Abmelden** . Ist ein anderer Thread die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für das Empfängerobjekt Advise aufruft, wird jedoch **Release** -Aufruf verzögert, bis die **OnNotify** -Methode zurückgibt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

