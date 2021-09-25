---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 79137939ef6f40704804e5a3499c36cc2271c7fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630530"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Schließt einen Nachrichtenspeicheranbieter in geordneter Reihenfolge.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in] Reserviert; muss ein Zeiger auf Null sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

MAPI ruft die **IMSProvider::Shutdown-Methode** direkt vor der Freigabe des Nachrichtenspeicheranbieterobjekts auf. MAPI gibt alle Anmeldeobjekte für einen Anbieter frei, bevor **das Herunterfahren** für diesen Anbieter aufgerufen wird. 
  
## <a name="see-also"></a>Siehe auch



[IMSProvider : IUnknown](imsprovideriunknown.md)

