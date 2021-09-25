---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2321489893d8f085931d4dcb61e4688750c9a8ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621017"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht eine Registrierung für Benachrichtigungen mit einer Zuvor eingerichteten Formularanzeige durch Aufrufen von [IMAPIForm::Advise](imapiform-advise.md)ab.
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Eine Verbindungsnummer, die die Benachrichtigungsregistrierung angibt, die abgebrochen werden soll.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung wurde abgebrochen.
    
E_INVALIDARG 
  
> Die im  _ulConnection-Parameter_ übergebene Verbindungsnummer stellt keine gültige Registrierung dar. 
    
## <a name="remarks"></a>Bemerkungen

Formularviewer rufen die **IMAPIForm::Unadvise-Methode** auf, um eine Registrierung für eine Benachrichtigung abzubrechen, die sie zuerst erstellt haben, indem sie die **IMAPIForm::Advise-Methode** aufrufen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Verwerfen Sie den Zeiger, den Sie in der Ansicht des Formularviewers halten, indem Sie die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufrufen. Im Allgemeinen wird **"Release"** während des **Unadvise-Aufrufs** aufgerufen. Wenn jedoch ein anderer Thread gerade dabei ist, eine der [IMAPIViewAdviseSink-Methoden](imapiviewadvisesinkiunknown.md) für die Ansichts-Empfehlungssenke aufzurufen, verzögern Sie den **Release-Aufruf,** bis die **IMAPIViewAdviseSink-Methode** zurückgegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

