---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0d773b5b9392c5a32ff07bc20ecdd7a1a24cb578
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576114"
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
  
> [in] Eine Verbindungsnummer, die die abzubrechende Registrierung darstellt. Der  _ulConnection-Parameter_ sollte einen Wert enthalten, der von einem vorherigen Aufruf der [IAddrBook::Advise-Methode](iaddrbook-advise.md) zurückgegeben wird. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung wurde erfolgreich abgebrochen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clients rufen die **Unadvise-Methode** auf, um den Empfang von Benachrichtigungen über Änderungen an einem bestimmten Adressbucheintrag zu beenden. Wenn eine Benachrichtigungsregistrierung abgebrochen wird, gibt der Adressbuchanbieter seinen Zeiger auf die Empfehlungssenke des Anrufers frei. Die Veröffentlichung kann jedoch während des **Unadvise-Aufrufs** oder zu einem späteren Zeitpunkt erfolgen, wenn ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) aufruft. Wenn eine Benachrichtigung ausgeführt wird, wird die Veröffentlichung verzögert, bis die **OnNotify-Methode** zurückgegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

