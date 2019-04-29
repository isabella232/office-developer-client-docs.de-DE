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
ms.openlocfilehash: 2ea877c9328279322de0f15e5755096e74819425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419436"
---
# <a name="ltid"></a>LTID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Generische Langzeit-ID eines Objekts in einem Outlook-Speicher.
  
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
  
- Out Die GUID des Servers, der das Objekt erstellt hat.
    
 _globcnt_
  
- Out Eine eindeutige 6-Byte-Zahl, die das Objekt innerhalb des Outlook-Speichers identifiziert.
    
 _wLevel_
  
- Out Die Hierarchieebene der Eintrags-ID für einen öffentlichen Exchange-Ordner.
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[FEID](feid.md)

