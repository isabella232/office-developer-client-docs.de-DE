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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317276"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Entfernt die Registrierung eines Objekts zur Benachrichtigung über Nachrichtenspeicheränderungen, die zuvor mithilfe eines Aufrufs der [IMSLogon::Advise-Methode erstellt](imslogon-advise.md) wurden. 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Nummer der Registrierungsverbindung, die von einem Aufruf von **IMSLogon::Advise zurückgegeben wird.**
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Nachrichtenspeicheranbieter implementieren die **IMSLogon::Unadvise-Methode,** um den Zeiger auf das im  _lpAdviseSink-Parameter_ im vorherigen Aufruf von **IMSLogon::Advise** übergebene Advise-Sink-Objekt frei zu geben, wodurch eine Benachrichtigungsregistrierung abgebrochen wird. Im Rahmen des Verwerfens des Zeigers auf das advise-Sink-Objekt wird die [IUnknown::Release-Methode des](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) Objekts aufgerufen. Im Allgemeinen **wird Release** während des **Unadvise-Aufrufs** aufgerufen. Wenn jedoch ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für das Advise Sink-Objekt aufruft, wird der **Release-Aufruf** verzögert, bis die **OnNotify-Methode** zurückgegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

