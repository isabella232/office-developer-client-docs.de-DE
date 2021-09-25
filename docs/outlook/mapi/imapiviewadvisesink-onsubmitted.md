---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 67dac1246a2d01557ce2d6167f5f3eb32cb57a38
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592291"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigt die Formularanzeige, dass die aktuelle Nachricht an den MAPI-Spooler gesendet wurde.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Ein Formularobjekt ruft die **IMAPIViewAdviseSink::OnSubmitted-Methode auf,** nachdem ein Aufruf von [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) erfolgreich zurückgegeben wurde. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Nachdem **OnSubmitted** aufgerufen wurde, können Sie mit der Annahme fortfahren, dass die Nachricht aktualisiert wurde. Aktualisieren Sie Ihre Fenster, um alle aufgetretenen Änderungen widerzuspiegeln. 
  
Weitere Informationen zu Formularbenachrichtigungen finden Sie unter [Senden und Empfangen von Formularbenachrichtigungen.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

