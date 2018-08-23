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
ms.openlocfilehash: 33287d8ac6b1faeba8b8746a95850f6fd1c37462
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579487"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine Registrierung für Benachrichtigungen mit einem Formular Viewer zuvor durch Aufrufen von [IMAPIForm::Advise](imapiform-advise.md)hergestellt werden abgebrochen.
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Eine Verbindungsnummer, die identifiziert die benachrichtigungsregistrierung abgebrochen werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Registrierung wurde abgebrochen.
    
E_INVALIDARG 
  
> Die Nummer der _UlConnection_ -Parameter übergebenen stellt keine Registrierung ein gültiges dar. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Formular Viewer rufen Sie die **IMAPIForm::Unadvise** -Methode, um eine Registrierung für Benachrichtigung abzubrechen, das sie zuerst die **IMAPIForm::Advise** -Methode festgelegt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Verwerfen der Zeiger, den Sie zur Ansicht des Formulars-Viewers halten advise-Empfänger durch seine [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode aufrufen. Im allgemeinen **Release** aufgerufen wird während des Anrufs **Unadvise** . Wenn ein anderer Thread aufruft, eine der Methoden [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) ist für die Ansicht advise-Empfänger jedoch **Release** -Aufruf Verzögerung, bis die **IMAPIViewAdviseSink** -Methode zurückgibt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

