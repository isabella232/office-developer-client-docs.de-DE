---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424077"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht Benachrichtigungen ab, die zuvor mit einem Aufruf der [IABLogon:: Advise](iablogon-advise.md) -Methode eingerichtet wurden. 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> in Die Verbindungsnummer, die mit einer aktiven Benachrichtigungs Registrierung verknüpft ist. Ein vorheriger Anruf an **Advise** muss den Wert von _ulConnection_zurückgegeben haben.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungs Registrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>Bemerkungen

MAPI Ruft die **Unadvise** -Methode auf, um eine Benachrichtigungs Registrierung für ein Container-, Messaging-oder Verteilerlistenobjekt abzubrechen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung von **Unadvise** hängt davon ab, ob Sie die Benachrichtigung mit der MAPI-Hilfe oder manuell unterstützen. Wenn MAPI ihre Unterstützung bereitstellt, rufen Sie die [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md) -Methode auf, um die Registrierung abzubrechen. Wenn in einem anderen Thread die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode der Advise-Senke aufgerufen wird, kann Sie verzögert werden **** , bis OnNotify zurückgegeben wurde. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). Informationen zur Verwendung der [IMAPISupport: IUnknown](imapisupportiunknown.md) -Methoden zur Unterstützung von Benachrichtigungen finden Sie unter [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md).
  
## <a name="see-also"></a>Siehe auch



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

