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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f5d253d0306e55699fbe5b9c9decf8c3242867fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792887"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Betrifft**: Outlook 
  
In einer bestimmten Reihenfolge eines Transportdienstes wird geschlossen.
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Anruf in der Adressbuchhierarchie heruntergefahren war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Die MAPI-Warteschlange Ruft die **IXPProvider::Shutdown** -Methode unmittelbar vor der Freigabe ein Transport-Anbieter-Objekts. Vor dem **Herunterfahren**aufrufen, gibt MAPI alle Logon-Objekten für einen Anbieter frei.
  
## <a name="see-also"></a>Siehe auch



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider: IUnknown](ixpprovideriunknown.md)

