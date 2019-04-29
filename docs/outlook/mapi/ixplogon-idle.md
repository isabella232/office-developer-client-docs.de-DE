---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ceca6a2dbe5f80f8a3499e509db8d5e6c35d72d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436048"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, dass das System im Leerlauf ist, sodass der Transportanbieter Vorgänge mit niedriger Priorität ausführen kann.
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Der MAPI-Spooler ruft in regelmäßigen Abständen die **IXPLogon:: idle** -Methode auf, wenn das System inaktiv ist, indem das XP_LOGON_SP-Flag im Aufruf an die [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) -Methode übergeben wird, die die aktuelle Sitzung geöffnet hat. Wenn sich das System im Leerlauf befindet, kann der Transportanbieter Hintergrundvorgänge ausführen, die während anderer Aufrufe nicht geeignet sind oder die regelmäßig erfolgen müssen. 
  
## <a name="see-also"></a>Siehe auch



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

