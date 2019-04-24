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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328791"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigt den Formular Betrachter darüber, dass eine neue oder eine vorhandene Nachricht in ein Formular geladen wurde.
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung wurde erfolgreich ausgeführt.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIViewAdviseSink:: OnNewMessage** -Methode immer dann auf, wenn eine Nachricht in einem Formular mit der [IPersistMessage:: InitNew](ipersistmessage-initnew.md) -oder [IPersistMessage:: Laden](ipersistmessage-load.md) -Methode geladen wird. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Geben Sie den aktiven Zeiger auf das Form-Objekt frei, da es nicht mehr auf die Nachricht zeigt, die der Viewer zuvor angezeigt hat. 
  
Weitere Informationen zu Formular Benachrichtigungen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

