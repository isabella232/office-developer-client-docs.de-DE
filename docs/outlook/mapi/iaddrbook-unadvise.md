---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e06f78317a1e98d47a37cb7059042b254567fe8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573684"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Benachrichtigungsregistrierung eines für einen Adresseintrag Adressbuch zuvor eingerichtet werden abgebrochen.
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Eine Verbindung Zahl, die die Registrierung abgebrochen werden darstellt. Der Parameter _UlConnection_ sollte einen von einem vorherigen Aufruf der [IAddrBook::Advise](iaddrbook-advise.md) -Methode zurückgegebenen Wert enthalten. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Registrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clients aufrufen die **Unadvise** -Methode zum Empfangen von Benachrichtigungen zu Änderungen an einer bestimmten Adressbuch Adresseintrag beenden. Wenn ein benachrichtigungsregistrierung abgebrochen wird, der Adressbuchdateien Anbieter Versionen der Zeiger auf den Anrufer der advise-Empfänger. Die Version kann jedoch während des Anrufs **Unadvise** oder zu einem späteren Zeitpunkt, auftreten, wenn ein anderer Thread ist die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufruft. Wenn eine Benachrichtigung ausgeführt wird, wird die Version verzögert, bis die **OnNotify** -Methode zurückgibt. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

