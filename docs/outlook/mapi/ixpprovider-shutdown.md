---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 54e587ef23c9b121d4b9dc57bd68ebdad5ec38f3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584199"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Schließt einen Transportanbieter in geordneter Reihenfolge.
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf konnte den Transportanbieter herunterfahren.
    
## <a name="remarks"></a>HinwBemerkungeneise

Der MAPI-Spooler ruft die **IXPProvider::Shutdown-Methode** direkt vor der Freigabe eines Transportanbieterobjekts auf. Vor dem Aufrufen **des Herunterfahrens** gibt MAPI alle Anmeldeobjekte für einen Anbieter frei.
  
## <a name="see-also"></a>Siehe auch



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

