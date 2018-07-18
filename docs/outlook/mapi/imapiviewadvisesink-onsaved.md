---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0f9aa5d508afeaf5933c50763e1e42832ae4e3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792495"
---
# <a name="imapiviewadvisesinkonsaved"></a>IMAPIViewAdviseSink::OnSaved

  
  
**Betrifft**: Outlook 
  
Benachrichtigt den Formular-Viewer, den die aktuelle Nachricht in einem Formular gespeichert wurde.
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Ein Form-Objekt ruft die **IMAPIViewAdviseSink::OnSaved** -Methode auf, nachdem die aktuelle Nachricht in einem Formular erfolgreich gespeichert wurde. Dadurch werden Zuschauer zu ihren Windows Änderungen an der Nachricht entsprechend aktualisieren. 
  
Weitere Informationen zum Formular Benachrichtigungen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

