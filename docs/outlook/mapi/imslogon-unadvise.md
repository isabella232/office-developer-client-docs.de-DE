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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9172d4956e78ac31cd15d69e70d05c127a474ca5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387634"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Entfernt ein Objekt Anmeldungsseite für Benachrichtigung über Message Store Änderungen, die zuvor durch einen Aufruf an die [IMSLogon::Advise](imslogon-advise.md) -Methode festgelegt. 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Anzahl der Registrierung Verbindung durch einen Aufruf von **IMSLogon::Advise**zurückgegeben.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Nachricht von nachrichtenspeicheranbietern implementierte die **IMSLogon::Unadvise** -Methode, um den Zeiger auf den im Parameter _LpAdviseSink_ im vorherigen Aufruf **IMSLogon::Advise**, wodurch Stornieren einer benachrichtigungs übergeben Advise-Empfängerobjekt freigeben Registrierung. Im Rahmen des Zeigers auf das Empfängerobjekt Advise verwerfen wird das Objekt [IUnknown](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode aufgerufen. Im allgemeinen **Release** aufgerufen wird während des Anrufs **Unadvise** . Ist ein anderer Thread die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für das Empfängerobjekt Advise aufruft, wird jedoch **Release** -Aufruf verzögert, bis die **OnNotify** -Methode zurückgibt. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

