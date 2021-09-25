---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c21c61f886a6fcc493a83e0af54f010090e2dd3e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561460"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Entfernt die Registrierung eines Objekts für die Benachrichtigung über Änderungen am Nachrichtenspeicher, die zuvor mithilfe eines Aufrufs der [IMSLogon::Advise-Methode](imslogon-advise.md) eingerichtet wurden. 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulConnection_
  
> [in] Die Nummer der Registrierungsverbindung, die von einem Aufruf von **IMSLogon::Advise** zurückgegeben wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Message store providers implement the **IMSLogon::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMSLogon::Advise**, thereby canceling a notification registration. Im Rahmen des Verwerfens des Zeigers auf das Advise-Senkenobjekt wird die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) des Objekts aufgerufen. Im Allgemeinen wird **"Release"** während des **Unadvise-Aufrufs** aufgerufen. Wenn jedoch ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) für das Advise-Senkenobjekt aufruft, wird der **Release-Aufruf** verzögert, bis die **OnNotify-Methode** zurückgegeben wird. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

