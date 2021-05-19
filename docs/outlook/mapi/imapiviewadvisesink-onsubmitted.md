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
  
Benachrichtigt die Formularanzeige, dass die aktuelle Nachricht an den MAPI-Spooler übermittelt wurde.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung ist erfolgreich.
    
## <a name="remarks"></a>Hinweise

Ein Formularobjekt ruft die **IMAPIViewAdviseSink::OnSubmitted-Methode** auf, nachdem ein Aufruf von [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) erfolgreich zurückgegeben wurde. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Nachdem **OnSubmitted** aufgerufen wurde, können Sie davon ausgehen, dass die Nachricht aktualisiert wurde. Aktualisieren Sie Ihre Fenster, um alle aufgetretenen Änderungen widerspiegeln zu können. 
  
Weitere Informationen zu Formularbenachrichtigungen finden Sie unter Senden und Empfangen [von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

