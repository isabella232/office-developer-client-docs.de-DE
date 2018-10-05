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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397891"
---
# <a name="imapisessionunadvise"></a>IMAPISession::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der Methode [IMAPISession::Advise](imapisession-advise.md) eingerichtet. 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Eine Verbindung Zahl mit einer aktiven benachrichtigungsregistrierung verknüpft ist. Der Wert der _UlConnection_ muss durch einen vorherigen Aufruf von **IMAPISession::Advise**zurückgegeben wurde, haben.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISession::Unadvise** -Methode hebt die Registrierung ein für die Benachrichtigung. **Unadvise** -Versionen der Zeiger auf des Anrufers advise-Empfänger, die sie in der **Advise** -Aufruf für die Registrierung verwendet erhalten. 
  
Im Allgemeinen ruft **Unadvise** Advise-Empfänger [IUnknown](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode während des Anrufs **Unadvise** . Wenn ein anderer Thread wird gerade Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufrufen, wird jedoch **Release** -Aufruf verzögert, bis die **OnNotify** -Methode zurückgibt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Advise](imapisession-advise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

