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
ms.openlocfilehash: 2d9a58ff05bb0da07762b9eafddef7303e8b9bc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592605"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Die MAPI-Warteschlange Ruft die **IXPProvider::Shutdown** -Methode unmittelbar vor der Freigabe ein Transport-Anbieter-Objekts. Vor dem **Herunterfahren**aufrufen, gibt MAPI alle Logon-Objekten für einen Anbieter frei.
  
## <a name="see-also"></a>Siehe auch



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

