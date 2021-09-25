---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6c0765e2764eced086f2de5c326449919d96b3fc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571661"
---
# <a name="imsgstoreunadvise"></a>IMsgStore::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMsgStore::Advise-Methode](imsgstore-advise.md) eingerichtet wurden. 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Verbindungsnummer, die einer aktiven Benachrichtigungsregistrierung zugeordnet ist. Der Wert von  _ulConnection_ muss durch einen vorherigen Aufruf der **IMsgStore::Advise-Methode** zurückgegeben worden sein. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgStore::Unadvise-Methode** bricht eine Registrierung für Benachrichtigungen ab. **Unadvise** gibt den Zeiger auf die Empfehlungssenke des Anrufers frei, die er im Für die Registrierung verwendeten **"Advise"-Anruf** erhalten hat. 
  
Im Allgemeinen ruft **"Unadvise"** während des **Aufrufs "Unadvise"** die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) der Empfehlungssenke auf. Wenn jedoch ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) der Empfehlungssenke aufruft, wird der **Release-Aufruf** verzögert, bis die **OnNotify-Methode** zurückgegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

