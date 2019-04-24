---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f85b662b7fe710c66a2e69dd3cd3db22e3283ddb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309723"
---
# <a name="imsgstoreunadvise"></a>IMsgStore::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMsgStore:: Advise](imsgstore-advise.md) -Methode eingerichtet wurden. 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> in Die Verbindungsnummer, die mit einer aktiven Benachrichtigungs Registrierung verknüpft ist. Der Wert von _ulConnection_ muss von einem vorherigen Aufruf der **IMsgStore:: Advise** -Methode zurückgegeben worden sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore:: Unadvise** -Methode bricht eine Registrierung für die Benachrichtigung ab. **Unadvise** gibt den Zeiger auf die Advise-Senke des Anrufers frei, die er im für die Registrierung verwendeten **Advise** -Aufruf erhalten hat. 
  
Im allgemeinen **** ruft Unadvise während des Unadvise-Aufrufs die [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode der Advise-Senke auf. **** Wenn jedoch ein anderer Thread gerade die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode der Advise-Senke aufruft, wird der **Freigabe** Aufruf verzögert, bis **** die OnNotify-Methode zurückgegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

