---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29dd2e3b47d0f43df7824274d2fdcc4f7f16eeb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569855"
---
# <a name="ltid"></a>LTID

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Generische lange Ausdrucks-ID eines Objekts in einem Outlook-Speicher.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a>Elemente

 _guid_
  
- [out] Die GUID des Servers, der das Objekt erstellt.
    
 _globcnt_
  
- [out] Eine 6-Byte eindeutige Zahl, die das Objekt in der Outlook-Speicher angibt.
    
 _wLevel_
  
- [out] Die Ebene der die Eintrags-ID für einen bevorzugten öffentlichen Exchange-Ordner.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[FEID](feid.md)

