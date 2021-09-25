---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: edc80ce468325d820c00e4822cb207836c58e436
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561481"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Meldet sich von einem Nachrichtenspeicheranbieter ab. 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in] Reserviert; muss ein Zeiger auf Null sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Nachrichtenspeicheranbieter implementieren die **IMSLogon::Logoff-Methode,** um einen Nachrichtenspeicheranbieter zu schließen. **IMSLogon::Logoff** wird in den folgenden Situationen aufgerufen: 
  
- Während sich die MAPI nach einem Aufruf der [IMAPISession::Logoff-Methode](imapisession-logoff.md) von einem Client abmeldet. 
    
- Während sich die MAPI von einem Nachrichtenspeicheranbieter abmeldet. In diesem Fall wird **IMSLogon::Logoff** als Teil der MAPI-Verarbeitung der [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) des Supportobjekts aufgerufen, das der Nachrichtenspeicheranbieter erstellt, während ein [IMsgStore::StoreLogoff-](imsgstore-storelogoff.md) oder **IUnknown::Release-Methodenaufruf** für ein Nachrichtenspeicherobjekt verarbeitet wird. 
    
## <a name="see-also"></a>Siehe auch



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

