---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 62c18ac609547563ad0e98cbd914866e05888ac8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795823"
---
# <a name="uptble"></a>UPTBLE

**Betrifft**: Outlook 
  
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

## <a name="members"></a>Members

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

- [Über die API-Replikation](about-the-replication-api.md) 
- [Informationen zu den Replikationsstatus Computer](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

