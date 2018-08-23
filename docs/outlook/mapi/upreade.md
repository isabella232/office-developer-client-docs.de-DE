---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fd593b68ef7ca25b1f8ceec613786cdbdd03fd76
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579074"
---
# <a name="upreade"></a>UPREADE

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erweiterte Informationen zum Hochladen eines Elements Zustand "gelesen" während der [Upload lesen Status Zustand](upload-read-status-state.md).
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>Elemente

_ulFlags_
  
>  [Out] / [in] Flags, um das entsprechende Verhalten beim Hochladen zu bestimmen. 
    
  - UPR_ASSOC
    
    - [out] Element ausgeblendet ist.
    
  - UPR_READ
    
    - [out] Der schreibgeschützte Status des Elements wurde geändert.
    
  - UPR_OK
    
    - [in] Der Upload war erfolgreich. Der Client legt dies nach dem Hochladen von Informationen an den Server.
    
  - UPR_COMMIT
    
    - [in] Hochladen des lesen Status des Elements jetzt, anstatt zu warten, bis zum Ende der [Tabelle Zustand hochladen](upload-table-state.md) zur Stapelverarbeitung mehr als ein Element. 
    
_SKEY_
  
> [out] Quellschlüssel des Elements.
    
## <a name="see-also"></a>Siehe auch

- [Informationen über die Replikations-API](about-the-replication-api.md)
- [Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
- [MAPI-Konstanten](mapi-constants.md)
- [UPREAD](upread.md)

