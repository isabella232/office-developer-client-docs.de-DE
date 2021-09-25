---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: de450ddef3990f788f3e92ac39b15345aa3adf62
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630565"
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
  
> Die Benachrichtigung war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIViewAdviseSink::OnNewMessage-Methode auf,** wenn eine Nachricht in einem Formular mithilfe der [IPersistMessage::InitNew-](ipersistmessage-initnew.md) oder [IPersistMessage::Load-Methode](ipersistmessage-load.md) geladen wird. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Geben Sie den aktiven Zeiger auf das Formularobjekt frei, da er nicht mehr auf die Nachricht zeigt, die ihr Viewer zuvor angezeigt hat. 
  
Weitere Informationen zu Formularbenachrichtigungen finden Sie unter [Senden und Empfangen von Formularbenachrichtigungen.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>Siehe auch



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

