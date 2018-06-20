---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f4ece0662b72047b785b03f3134c96fac48c219a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795567"
---
# <a name="skey"></a>SKEY

  
  
**Betrifft**: Outlook 
  
Source-Schlüssel für ein Outlook-Element.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a>Members

 _guid_
  
> GUID des Servers, der das Objekt erstellt.
    
## <a name="see-also"></a>Siehe auch



[Über die API-Replikation](about-the-replication-api.md)
  
[Informationen zu den Replikationsstatus Computer](about-the-replication-state-machine.md)
  
[UPDELE](updele.md)
  
[UPMSG](upmsg.md)
  
[UPREADE](upreade.md)

