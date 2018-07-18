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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf72e6f182f67861f909e21f0ec1871d76617974
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19792022"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**Betrifft**: Outlook 
  
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
    
## <a name="remarks"></a>Bemerkungen

Clients aufrufen die **Unadvise** -Methode zum Empfangen von Benachrichtigungen zu Änderungen an einer bestimmten Adressbuch Adresseintrag beenden. Wenn ein benachrichtigungsregistrierung abgebrochen wird, der Adressbuchdateien Anbieter Versionen der Zeiger auf den Anrufer der advise-Empfänger. Die Version kann jedoch während des Anrufs **Unadvise** oder zu einem späteren Zeitpunkt, auftreten, wenn ein anderer Thread ist die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufruft. Wenn eine Benachrichtigung ausgeführt wird, wird die Version verzögert, bis die **OnNotify** -Methode zurückgibt. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

