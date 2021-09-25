---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d7a3b61760b21ee34d5726e9a321fd418c55d7ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613751"
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
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Der MAPI-Spooler ruft in regelmäßigen Abständen die **IXPLogon::Idle-Methode** auf, wenn dies angefordert wird, während sich das System im Leerlauf befindet, indem das flag XP_LOGON_SP im Aufruf an die [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) übergeben wird, die die aktuelle Sitzung geöffnet hat. In Zeiten, in denen sich das System im Leerlauf befindet, kann der Transportanbieter Hintergrundvorgänge ausführen, die bei anderen Aufrufen nicht geeignet sind oder regelmäßig ausgeführt werden müssen. 
  
## <a name="see-also"></a>Siehe auch



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

