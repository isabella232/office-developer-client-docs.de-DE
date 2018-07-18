---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 854e674002953c31c47d56096700dca582ce0a5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795819"
---
# <a name="upreade"></a>UPREADE

**Betrifft**: Outlook 
  
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

