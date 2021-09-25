---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f1cfafc1236f2347527efd9022c4484dffee229
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614038"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht Benachrichtigungen ab, die zuvor mit einem Aufruf der [IABLogon::Advise-Methode](iablogon-advise.md) eingerichtet wurden. 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Verbindungsnummer, die einer aktiven Benachrichtigungsregistrierung zugeordnet ist. Ein vorheriger Aufruf von **Advise** muss den Wert von  _ulConnection_ zurückgegeben haben.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungsregistrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>Bemerkungen

MAPI ruft die **Unadvise-Methode** auf, um eine Benachrichtigungsregistrierung für ein Container-, Messagingbenutzer- oder Verteilerlistenobjekt abzubrechen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung von **"Unadvise"** hängt davon ab, ob Sie Benachrichtigungen mit der MAPI-Hilfe oder manuell unterstützen. Wenn MAPI Ihren Support bereitstellt, rufen Sie die [IMAPISupport::Unsubscribe-Methode](imapisupport-unsubscribe.md) auf, um die Registrierung abzubrechen. Wenn ein anderer Thread gerade dabei ist, die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der Empfehlungssenke aufzurufen, kann dies verzögert werden, bis **OnNotify** zurückgegeben wurde. 
  
Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI.](event-notification-in-mapi.md) Informationen zur Verwendung der [IMAPISupport : IUnknown-Methoden](imapisupportiunknown.md) zur Unterstützung von Benachrichtigungen finden Sie unter ["Unterstützende Ereignisbenachrichtigung".](supporting-event-notification.md)
  
## <a name="see-also"></a>Siehe auch



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

