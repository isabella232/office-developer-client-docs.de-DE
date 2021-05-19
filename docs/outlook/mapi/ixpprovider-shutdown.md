---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409692"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Schließt einen Transportanbieter in geordneter Weise.
  
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
  
> Durch den Aufruf konnte der Transportanbieter beendet werden.
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft die **IXPProvider::Shutdown-Methode** kurz vor der Veröffentlichung eines Transportanbieterobjekts auf. Vor dem **Aufrufen von Shutdown** gibt MAPI alle Anmeldeobjekte für einen Anbieter frei.
  
## <a name="see-also"></a>Siehe auch



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

