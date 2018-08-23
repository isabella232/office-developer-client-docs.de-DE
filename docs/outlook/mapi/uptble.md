---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b2523c149d98dacf9ad321a4a443382a39753fd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592339"
---
# <a name="uptble"></a>UPTBLE

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ausführliche Informationen zum Hochladen der Inhalt eines Ordners während der [Tabelle Zustand hochladen](upload-table-state.md)enthält.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a>Elemente

 _iEntMod_
  
>  [out] Index zum Nachverfolgen die _cEntMod_ Anzahl der neuen oder geänderten Elemente hochladen. 
    
 _cEntMod_
  
>  [out] Anzahl der neuen oder geänderten Elemente im Ordner. 
    
 _iEntRead_
  
>  [out] Indizieren Sie, um nachzuverfolgen, die Anzahl der _cEntRead_ Elemente lesen hochladen. 
    
 _cEntRead_
  
>  [out] Anzahl der gelesenen Elemente im Ordner. 
    
 _iEntDel_
  
>  [out] Index zum Nachverfolgen die Anzahl der _cEntDel_ hochladen gelöschte Elemente. 
    
 _cEntDel_
  
>  [out] Anzahl der gelöschten Elemente im Ordner. 
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md) 
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

