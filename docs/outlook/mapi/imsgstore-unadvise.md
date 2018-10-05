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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398017"
---
# <a name="imsgstoreunadvise"></a>IMsgStore::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der Methode [IMsgStore::Advise](imsgstore-advise.md) eingerichtet. 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Nummer eines aktiven benachrichtigungsregistrierung zugeordnet. Der Wert der _UlConnection_ muss von einem vorherigen Aufruf der **IMsgStore::Advise** -Methode zurückgegeben wurde, haben. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::Unadvise** -Methode hebt die Registrierung ein für die Benachrichtigung. **Unadvise** -Versionen der Zeiger auf des Anrufers advise-Empfänger, die sie in der **Advise** -Aufruf für die Registrierung verwendet erhalten. 
  
Im Allgemeinen ruft **Unadvise** Advise-Empfänger [IUnknown](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode während des Anrufs **Unadvise** . Wenn ein anderer Thread wird gerade Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufrufen, wird jedoch **Release** -Aufruf verzögert, bis die **OnNotify** -Methode zurückgibt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

