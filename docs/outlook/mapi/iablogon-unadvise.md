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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d9f69098f9c53e75dea6f485248d61d277e181c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791979"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**Betrifft**: Outlook 
  
Benachrichtigungen, die zuvor mit einem Aufruf der Methode [IABLogon::Advise](iablogon-advise.md) eingerichtet wurden, werden abgebrochen. 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Nummer eines aktiven benachrichtigungsregistrierung zugeordnet. Ein vorherigen Aufruf von **Advise** muss den Wert der _UlConnection_zurückgegeben haben.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die benachrichtigungsregistrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>Bemerkungen

MAPI-Aufrufen die **Unadvise** -Methode, um die benachrichtigungsregistrierung eines für einen Container abzubrechen messaging-Benutzer oder Verteilung List-Objekt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung von **Unadvise** hängt davon ab, ob Sie die Benachrichtigung mithilfe des MAPI-Hilfe oder manuell zu unterstützen. Wenn MAPI Ihrer unterstützt, rufen Sie die [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) -Methode, um die Registrierung abzubrechen. Ein anderer Thread wird gerade Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufrufen, kann verzögert werden, bis **OnNotify** zurückgegeben hat. 
  
Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md). Informationen zur Verwendung der [IMAPISupport: IUnknown](imapisupportiunknown.md) Methoden verwenden, um die Benachrichtigung, zu unterstützen, finden Sie unter [Ereignisbenachrichtigung unterstützen](supporting-event-notification.md).
  
## <a name="see-also"></a>Siehe auch



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

