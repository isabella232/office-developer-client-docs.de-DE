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
  
Gibt an, dass sich das System im Leerlauf befindet, sodass der Transportanbieter Vorgänge mit niedriger Priorität ausführen kann.
  
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
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Der MAPI-Spooler ruft die **IXPLogon::Idle-Methode** regelmäßig auf, wenn dies angefordert wird, wenn das System im Leerlauf ist, indem das flag XP_LOGON_SP im Aufruf der [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) übergeben wird, die die aktuelle Sitzung geöffnet hat. In Zeiten, in denen sich das System im Leerlauf befindet, kann der Transportanbieter Hintergrundvorgänge ausführen, die bei anderen Anrufen nicht geeignet sind oder regelmäßig ausgeführt werden müssen. 
  
## <a name="see-also"></a>Siehe auch



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

