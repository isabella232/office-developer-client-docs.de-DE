---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348874"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Protokolliert einen Nachrichtenspeicheranbieter. 
  
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
    
## <a name="remarks"></a>Hinweise

Nachrichtenspeicheranbieter implementieren die **IMSLogon::Logoff-Methode** zum gewaltsamen Herunterfahren eines Nachrichtenspeicheranbieters. **IMSLogon::Logoff** wird in den folgenden Situationen aufgerufen: 
  
- Während MAPI einen Client nach einem Aufruf der [IMAPISession::Logoff-Methode](imapisession-logoff.md) abmeldet. 
    
- Während MAPI einen Nachrichtenspeicheranbieter abmeldet. In diesem Fall wird **IMSLogon::Logoff** als Teil der MAPI-Verarbeitung der [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) des Supportobjekts aufgerufen, das der Nachrichtenspeicheranbieter erstellt, während er einen [IMsgStore::StoreLogoff-](imsgstore-storelogoff.md) oder **IUnknown::Release-Methodenaufruf** für ein Nachrichtenspeicherobjekt verarbeitet. 
    
## <a name="see-also"></a>Siehe auch



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

