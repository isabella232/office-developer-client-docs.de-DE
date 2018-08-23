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
ms.openlocfilehash: 12aa8b79e38320d9767a6c333cb0197ea5669862
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578012"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Die MAPI-Warteschlange ruft in regelmäßigen Abständen die **IXPLogon::Idle** -Methode, wenn Zeiten angefordert, wenn das System ist, indem das Flag XP_LOGON_SP im Aufruf der [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) -Methode, die die aktuelle Sitzung geöffnet übergeben im Leerlauf. Bisweilen, wenn das System im Leerlauf befindet, kann der Adressbuchhierarchie Hintergrundvorgängen ausgeführt werden, die nicht richtig sind bei anderen anrufen oder, die in regelmäßigen Abständen auftreten, müssen. 
  
## <a name="see-also"></a>Siehe auch



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

