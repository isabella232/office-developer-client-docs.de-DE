---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: aeeed580fbe7048f8539fb561e3446ef5c6095bf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566598"
---
# <a name="skey"></a>SKEY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Quellschlüssel für ein Outlook Element.
  
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

