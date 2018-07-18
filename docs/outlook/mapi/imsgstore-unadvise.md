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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 516de39d721c532c003775bd366a52ed8144ab88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792664"
---
# <a name="imsgstoreunadvise"></a>IMsgStore::Unadvise

  
  
**Betrifft**: Outlook 
  
Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der Methode [IMsgStore::Advise](imsgstore-advise.md) eingerichtet. 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Nummer eines aktiven benachrichtigungsregistrierung zugeordnet. Der Wert der _UlConnection_ muss von einem vorherigen Aufruf der **IMsgStore::Advise** -Methode zurückgegeben wurde, haben. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Registrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgStore::Unadvise** -Methode hebt die Registrierung ein für die Benachrichtigung. **Unadvise** -Versionen der Zeiger auf des Anrufers advise-Empfänger, die sie in der **Advise** -Aufruf für die Registrierung verwendet erhalten. 
  
Im Allgemeinen ruft **Unadvise** Advise-Empfänger [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode während des Anrufs **Unadvise** . Wenn ein anderer Thread wird gerade Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufrufen, wird jedoch **Release** -Aufruf verzögert, bis die **OnNotify** -Methode zurückgibt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

