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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2ec78331fd013777f001d39bd7e978a67abb5342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351198"
---
# <a name="imapiviewadvisesinkonsaved"></a>IMAPIViewAdviseSink::OnSaved

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigt den Formular Betrachter darüber, dass die aktuelle Nachricht in einem Formular gespeichert wurde.
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a>Parameter

Keine
  
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Ein Form-Objekt ruft die **IMAPIViewAdviseSink::** onsaved-Methode auf, nachdem die aktuelle Nachricht in einem Formular erfolgreich gespeichert wurde. Auf diese Weise können die Betrachter Ihre Fenster aktualisieren, um Änderungen an der Nachricht widerzuspiegeln. 
  
Weitere Informationen zu Formular Benachrichtigungen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

