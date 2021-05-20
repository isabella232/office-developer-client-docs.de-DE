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
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436153"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bricht eine Benachrichtigungsregistrierung ab, die zuvor für einen Adressbucheintrag eingerichtet wurde.
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Eine Verbindungsnummer, die die zu kündigende Registrierung darstellt. Der  _ulConnection-Parameter_ sollte einen Wert enthalten, der durch einen vorherigen Aufruf der [IAddrBook::Advise-Methode zurückgegeben](iaddrbook-advise.md) wurde. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>Hinweise

Clients rufen die **Unadvise-Methode** auf, um den Empfang von Benachrichtigungen über Änderungen an einem bestimmten Adressbucheintrag zu beenden. Wenn eine Benachrichtigungsregistrierung abgebrochen wird, gibt der Adressbuchanbieter seinen Zeiger auf die Ratgebersenke des Anrufers frei. Die Veröffentlichung kann jedoch während des **Unadvise-Aufrufs** oder zu einem späteren Zeitpunkt auftreten, wenn ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) aufruft. Wenn eine Benachrichtigung ausgeführt wird, wird die Veröffentlichung verzögert, bis die **OnNotify-Methode zurückgegeben** wird. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

