---
title: IMAPISessionUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Unadvise
api_type:
- COM
ms.assetid: 5e608cb0-808d-4418-8521-71dcbce8cdff
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335702"
---
# <a name="imapisessionunadvise"></a>IMAPISession::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMAPISession::Advise-Methode eingerichtet](imapisession-advise.md) wurden. 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Eine Verbindungsnummer, die einer aktiven Benachrichtigungsregistrierung zugeordnet ist. Der Wert von _ulConnection_ muss von einem vorherigen Aufruf von **IMAPISession::Advise zurückgegeben worden sein.**
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::Unadvise-Methode** bricht eine Registrierung zur Benachrichtigung ab. **Unadvise** gibt seinen Zeiger auf die Ratensenke des Anrufers frei, die er im Zur Registrierung verwendeten **Anruf "Raten"** erhalten hat. 
  
Im Allgemeinen **ruft Unadvise** die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) der Ratensenke während des **Unadvise-Aufrufs** auf. Wenn jedoch ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der Ratensenke aufruft, wird der **Release-Aufruf** verzögert, bis die **OnNotify-Methode** zurückgegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Advise](imapisession-advise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

