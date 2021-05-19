---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6a6f8f9d675bee362b4a9f1c5b7fc544fa66d7b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419604"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigt die Formularanzeige, dass eine neue oder eine vorhandene Nachricht in einem Formular geladen wurde.
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung ist erfolgreich.
    
## <a name="remarks"></a>Hinweise

Formularobjekte rufen die **IMAPIViewAdviseSink::OnNewMessage-Methode** auf, wenn eine Nachricht in einem Formular mit der [IPersistMessage::InitNew-](ipersistmessage-initnew.md) oder [IPersistMessage::Load-Methode](ipersistmessage-load.md) geladen wird. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Lassen Sie den aktiven Zeiger auf das Formularobjekt los, da er nicht mehr auf die Nachricht verweist, die der Betrachter zuvor angezeigt hat. 
  
Weitere Informationen zu Formularbenachrichtigungen finden Sie unter Senden und Empfangen [von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

