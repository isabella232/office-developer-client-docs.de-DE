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
ms.openlocfilehash: 2aa1aca2816b8f0e148d35d1fcec761f621a2239
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579445"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Benachrichtigt dem Formular-Viewer, dass die aktuelle Nachricht an die MAPI-Warteschlange gesendet wurde.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Ein Form-Objekt ruft die **IMAPIViewAdviseSink::OnSubmitted** -Methode auf, nachdem ein Aufruf von [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) erfolgreich zurückgegeben hat. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Nachdem **OnSubmitted** aufgerufen wurde, können Sie auf der Annahme fortfahren, dass die Nachricht wurde aktualisiert. Aktualisieren Sie Ihre Windows, um alle Änderungen, die aufgetreten sind. 
  
Weitere Informationen zum Formular Benachrichtigungen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

