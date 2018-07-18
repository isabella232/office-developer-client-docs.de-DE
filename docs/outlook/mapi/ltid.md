---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4a60e2fe3a58e1d696ae9645e03ce8dde5340d9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792909"
---
# <a name="ltid"></a>LTID

  
  
**Betrifft**: Outlook 
  
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

