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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 75607550f1d6085a670ad997238994400e08f7bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792876"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**Betrifft**: Outlook 
  
Gibt an, dass das System im Leerlauf, der Adressbuchhierarchie niedriger Priorität Operationen aktivieren.
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die MAPI-Warteschlange ruft in regelmäßigen Abständen die **IXPLogon::Idle** -Methode, wenn Zeiten angefordert, wenn das System ist, indem das Flag XP_LOGON_SP im Aufruf der [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) -Methode, die die aktuelle Sitzung geöffnet übergeben im Leerlauf. Bisweilen, wenn das System im Leerlauf befindet, kann der Adressbuchhierarchie Hintergrundvorgängen ausgeführt werden, die nicht richtig sind bei anderen anrufen oder, die in regelmäßigen Abständen auftreten, müssen. 
  
## <a name="see-also"></a>Siehe auch



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

