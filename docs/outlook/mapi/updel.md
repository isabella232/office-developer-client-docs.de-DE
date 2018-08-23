---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 057a1ff38ed3809ce03bce8f820f1d16eea7fb46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581125"
---
# <a name="updel"></a>UPDEL

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Informationen für Elemente, die in einem lokalen Speicher gelöscht wurden. Diese Informationen werden während der [Upload löschen Status Zustand](upload-delete-status-state.md)verwendet.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Elemente

 _pupde_
  
>  [out] Vektor [UPDELE](updele.md) Einträge. 
    
 _cEnt_
  
> [out] Anzahl der Einträge in *Pupde* . 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)

