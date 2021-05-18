---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 770ceb7af98f5271baad65043e013feb353d231a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329470"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht eine Registrierung für Benachrichtigungen bei einer zuvor durch Aufrufen von [IMAPIForm::Advise](imapiform-advise.md)eingerichteten Formularanzeige ab.
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Eine Verbindungsnummer, die die Benachrichtigungsregistrierung identifiziert, die abgebrochen werden soll.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung wurde abgebrochen.
    
E_INVALIDARG 
  
> Die im  _ulConnection-Parameter übergebene_ Verbindungsnummer stellt keine gültige Registrierung dar. 
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIForm::Unadvise-Methode** auf, um eine Registrierung für Benachrichtigungen abbricht, die sie zuerst durch Aufrufen der **IMAPIForm::Advise-Methode eingerichtet** haben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Verwerfen Sie den Zeiger, den Sie an der Ansichtsanzeige der Formularanzeige halten, indem Sie die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufrufen. Im Allgemeinen **wird Release** während des **Unadvise-Aufrufs** aufgerufen. Wenn jedoch ein anderer Thread eine der [IMAPIViewAdviseSink-Methoden](imapiviewadvisesinkiunknown.md) für die Ansichtssenke aufruft, verzögern Sie den **Release-Aufruf,** bis die **IMAPIViewAdviseSink-Methode** zurückgegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

