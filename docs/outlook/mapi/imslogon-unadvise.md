---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 34c15ca4f7d81eeeee71fb0cb7e31085c75e5492
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792701"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**Betrifft**: Outlook 
  
Entfernt ein Objekt Anmeldungsseite für Benachrichtigung über Message Store Änderungen, die zuvor durch einen Aufruf an die [IMSLogon::Advise](imslogon-advise.md) -Methode festgelegt. 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Anzahl der Registrierung Verbindung durch einen Aufruf von **IMSLogon::Advise**zurückgegeben.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Nachricht von nachrichtenspeicheranbietern implementierte die **IMSLogon::Unadvise** -Methode, um den Zeiger auf den im Parameter _LpAdviseSink_ im vorherigen Aufruf **IMSLogon::Advise**, wodurch Stornieren einer benachrichtigungs übergeben Advise-Empfängerobjekt freigeben Registrierung. Im Rahmen des Zeigers auf das Empfängerobjekt Advise verwerfen wird das Objekt [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode aufgerufen. Im allgemeinen **Release** aufgerufen wird während des Anrufs **Unadvise** . Ist ein anderer Thread die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für das Empfängerobjekt Advise aufruft, wird jedoch **Release** -Aufruf verzögert, bis die **OnNotify** -Methode zurückgibt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

