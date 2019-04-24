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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357197"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Schließt einen Transportanbieter ordnungsgemäß ab.
  
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
  
> Der Aufruf konnte beim Herunterfahren des Transportanbieters ausgeführt werden.
    
## <a name="remarks"></a>Bemerkungen

Die MAPI-Warteschlange ruft die **IXPProvider:: Shutdown** -Methode auf, bevor ein Transportanbieter Objekt freigegeben wird. Vor dem Aufrufen von **Shutdown**gibt MAPI alle Anmeldeobjekte für einen Anbieter frei.
  
## <a name="see-also"></a>Siehe auch



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

