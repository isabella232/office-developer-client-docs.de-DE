---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 26b08535d81cb961ed0ace70ea227316b30cd526
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573460"
---
# <a name="skey"></a>SKEY

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Source-Schlüssel für ein Outlook-Element.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a>Elemente

 _guid_
  
> GUID des Servers, der das Objekt erstellt.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[UPDELE](updele.md)
  
[UPMSG](upmsg.md)
  
[UPREADE](upreade.md)

