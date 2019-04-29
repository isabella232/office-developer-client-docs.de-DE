---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ebde06d0d22320ecb5edb633cf8d04aaeec2a841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433983"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigt den Formular Betrachter darüber, dass die aktuelle Nachricht an den MAPI-Spooler übermittelt wurde.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung wurde erfolgreich ausgeführt.
    
## <a name="remarks"></a>Bemerkungen

Ein Form-Objekt ruft die **IMAPIViewAdviseSink:: onsubmitted** -Methode nach einem Aufruf von [IMAPIMessageSite:: SubmitMessage](imapimessagesite-submitmessage.md) wurde erfolgreich zurückgegeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Nachdem **onsubmitted** aufgerufen wurde, können Sie davon ausgehen, dass die Nachricht aktualisiert wurde. Aktualisieren Sie Ihre Fenster, um alle aufgetretenen Änderungen widerzuspiegeln. 
  
Weitere Informationen zu Formular Benachrichtigungen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

