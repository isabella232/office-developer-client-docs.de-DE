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
  
Benachrichtigungen, die zuvor mit einem Aufruf der [IABLogon::Advise-Methode eingerichtet wurden,](iablogon-advise.md) werden abgebrochen. 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Verbindungsnummer, die einer aktiven Benachrichtigungsregistrierung zugeordnet ist. Ein vorheriger Aufruf von **Advise** muss den Wert von _ulConnection zurückgegeben haben._
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungsregistrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>Hinweise

MAPI ruft die **Unadvise-Methode** auf, um eine Benachrichtigungsregistrierung für ein Container-, Messagingbenutzer- oder Verteilerlistenobjekt abbricht. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ihre Implementierung von **Unadvise** hängt davon ab, ob Sie Benachrichtigungen mithilfe von MAPI oder manuell unterstützen. Wenn MAPI Ihren Support bietet, rufen Sie die [IMAPISupport::Unsubscribe-Methode](imapisupport-unsubscribe.md) auf, um die Registrierung abbricht. Wenn ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der Ratensenke aufruft, kann er verzögert werden, bis **OnNotify** zurückgegeben wurde. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). Informationen zur Verwendung der [IMAPISupport : IUnknown-Methoden](imapisupportiunknown.md) zur Unterstützung von Benachrichtigungen finden Sie unter [Supporting Event Notification](supporting-event-notification.md).
  
## <a name="see-also"></a>Siehe auch



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

